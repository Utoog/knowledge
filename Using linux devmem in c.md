
https://bakhi.github.io/devmem/
``` c
int mem_fd = open("/dev/mem", O_RDWR | O_SYNC);
void *map_base = mmap(NULL,
			PAGE_SIZE,
			PROT_READ | PROT_WRITE,
			MAP_SHARED,
			mem_fd,
			phys_addr);	// phys_addr should be page-aligned.	
// check if map_base != MAP_FAILED
void *virt_addr = (char *)map_base + offset_in_page;

if (is_read) {
    read_result = *(volatile uint64_t*)virt_addr;
} else {	// write
    *(volatile uint64_t*)virt_addr = write_value;
}

unmap(map_base, PAGE_SIZE);
```



