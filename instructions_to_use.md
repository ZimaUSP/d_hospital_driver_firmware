Você vai precisar instalar:
* GCC;
* Make;
* ARM-GCC;
* STM32CubeMX;
* STM32CubeProgrammer.

# Instruções para instalar - Windows

### GCC e Make
No Windows, instale o [MSYS2](https://www.msys2.org/) e siga as instruções da página de download.
Após realizar todos os passos da página, podemos instalar pacotes pelo terminal do MSYS2, usando o comando:

```bash
pacman -S <pacote1> <pacote2> ... <pacoteN>
```

Assim, para instalar o que é necessário para o copilar os codigos driver basta utilizar o comando:

```bash
pacman -S gcc make
```
Após isso, é preciso colocar a pasta do msys2 nas variáveis de ambiente do Windows. Para isso, faça:
1. Pesquise variáveis de ambiente e clique em "Editar as variáveis de ambiente do sistema". Ou, vá para Painel de Controle > Sistema e Segurança > Sistema > Configurações avançadas do sistema.
2. Na janela que abriu, clique em "Variáveis de ambiente".
3. Na parte de "Variáveis do sistema", encontra a variável Path, selecione-a e clique em "Editar".
4. Clique em "Novo".
5. Digite o caminho para os executáveis MSYS2 (normalmente C:\msys64\usr\bin).
6. Mova o caminho para cima no PATH, deixando no primeiro lugar.
7. Clique em "OK".

Agora abra o Prompt de Comando (não o MSYS2, o prompt de comando normal do Windows) para testar se os pacotes foram instalados corretamente.
Para testar se gcc foi instalado corretamente, digite:

```bash
gcc -v
```

Algo parecido com isso deve aparecer no seu prompt de comando (não o MSYS2, o prompt de comando normal do Windows):

```
GNU Make 4.2.1
Built for x86_64-pc-msys
Copyright (C) 1988-2016 Free Software Foundation, Inc.
License GPLv3+: GNU GPL version 3 or later <http://gnu.org/licenses/gpl.html>
This is free software: you are free to change and redistribute it.
There is NO WARRANTY, to the extent permitted by law.
```


Algo parecido com isso deve aparecer no seu prompt de comando:

```
Using built-in specs.
COLLECT_GCC=gcc
COLLECT_LTO_WRAPPER=/usr/lib/gcc/x86_64-pc-msys/6.4.0/lto-wrapper.exe
Target: x86_64-pc-msys
Configured with: /msys_scripts/gcc/src/gcc-6.4.0/configure --build=x86_64-pc-msys --prefix=/usr --libexecdir=/usr/lib --enable-bootstrap --enable-shared --enable-shared-libgcc --enable-static --enable-version-specific-runtime-libs --with-arch=x86-64 --with-tune=generic --disable-multilib --enable-__cxa_atexit --with-dwarf2 --enable-languages=c,c++,fortran,lto --enable-graphite --enable-threads=posix --enable-libatomic --enable-libcilkrts --enable-libgomp --enable-libitm --enable-libquadmath --enable-libquadmath-support --enable-libssp --disable-win32-registry --disable-symvers --with-gnu-ld --with-gnu-as --disable-isl-version-check --enable-checking=release --without-libiconv-prefix --without-libintl-prefix --with-system-zlib --enable-linker-build-id --with-default-libstdcxx-abi=gcc4-compatible
Thread model: posix
gcc version 6.4.0 (GCC)
```