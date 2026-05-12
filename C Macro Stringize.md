
``` c macro.c
#include <stdio.h>
#define xstr(x) #x
#define str(x) xstr(x)

int main(void)
{
	puts("The magic number is " str(68) );
	return 0;
}
```
Output:
`The magic number is 68`
