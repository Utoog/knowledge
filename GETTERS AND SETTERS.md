
in headers:
``` c
#define GETTER_U8(VAR) uint8_t get_##VAR(void);
#define GETTER_U32(VAR) uint32_t get_##VAR(void);
#define SETTER_U8(VAR) uint8_t set_##VAR(uint8_t value);
#define ADDER(VAR) void ##VAR##_add(void);
```

in sources:
```c
#undef GETTER_U8
#undef GETTER_U32
#undef SETTER_U8
#undef ADDER

#define GETTER_U8(VAR) \
uint8_t get_##VAR(void) \
{ \
    return prv_vars.VAR; \
}

#define GETTER_U32(VAR) \
uint32_t get_##VAR(void) \
{ \
    return prv_vars.VAR; \
}

#define SETTER_U8(VAR) \
uint8_t set_##VAR(uint8_t value) \
{ \
    return prv_vars.VAR = value; \
}

#define ADDER(VAR) \
void ##VAR##_add(void) \
{ \
    prv_vars.VAR++; \
}
```

in s:
``` c
#define SETVAR(VAR) vars.VAR = get_##VAR();
```
