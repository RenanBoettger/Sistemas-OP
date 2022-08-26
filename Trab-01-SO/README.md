@echo off
cls
:menu
cls

date /t
  
## Menu 
```
echo            MENU DE TAREFAS
echo  +++++++++++++++++++++++++++++++++++
echo * 1. Fazer Backup                  *
echo * 2. Escanear Disco Local          *
echo * 3. Sair                          * 
echo * 4. Versao do Sistema             * 
echo * 5. Help                          * 
echo  +++++++++++++++++++++++++++++++++++
```

##opcao
```
set /p opcao= Escolha uma opcao: 
echo ------------------------------
if %opcao% equ 1 goto opcao1
if %opcao% equ 2 goto opcao2
if %opcao% equ 3 goto opcao3
if %opcao% equ 4 goto opcao4
if %opcao% equ 5 goto opcao5
```

## Relizar Backup
```
:opcao1
cls
xcopy "C:\origem" "D:\destino" /e/h/s/y/d
echo +++++++++++++++++++++++++++++++++++
echo *      Backup concluido           *
echo +++++++++++++++++++++++++++++++++++
pause
goto menu
```

## Escanear Disco
```
:opcao2
cls
echo +++++++++++++++++++++++++++++++++++
echo *     Escaneamento de disco       *
echo +++++++++++++++++++++++++++++++++++
chkdsk c:
pause
goto menu
```

## Sair do programa
```
:opcao3
cls
exit
```

## Versão do programa
```
:opcao4
echo +++++++++++++++++++++++++++++++++++++++++++++++
echo * 0.0 *
echo +++++++++++++++++++++++++++++++++++++++++++++++
pause
goto menu
```

## Descrição (help)
```
:opcao5
echo +++++++++++++++++++++++++++++++++++++++++++++++
echo * Opcao 1 - Limpeza da lixeira                                 *
echo * Opcao 2 - Backup na pasta deseja                             *
echo * Opcao 3 - Scaneamento do disco rigido                        *
echo * Opcao 4 - Fechar o sistema                                   *
echo * Opcao 5 - Versão do sistema caso deseja saber                *
echo * Opcao 6 - Lista de comandos                                  *
echo +++++++++++++++++++++++++++++++++++++++++++++++
pause
goto menu
```
