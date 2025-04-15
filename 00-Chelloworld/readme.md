#CONSIGNAS TP0
## Entorno de Desarrollo
- A. El compilador seleccionado es MinGW
- B. La version del compilador es la 14.2.0
- C. La version de C es C17

## Verificion del estandar C
Para verficar el estandar C soportado se probo el siguiente codigo 
```
#include <stdio.h>

int main()
{
    if( __STDC__ )
    {
        printf("The C version is at least C89\n");
#ifdef __STDC_VERSION__
    printf("C standard version: %lu\n",__STDC_VERSION__);
#endif
    }
    else
    {
        printf("Somehow you got ahold of K&R C. Neat!\n");
    }

    return(0);
}
```
