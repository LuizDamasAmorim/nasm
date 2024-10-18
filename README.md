# Estudo de comandos NASM 

<p align="center">
<img src="https://seeklogo.com/images/N/netwide-assembler-nasm-logo-EC5B1109AC-seeklogo.com.png" width=100 height=100>
</p>

## primeiros coamandos

* Programa hello world

```Assembly
global _start

    section .text
    _start:
        mov rax,1                       ;Prepara o sistema para fazer a escrita de um texto
        mov rdi,1                       ;Preparar a saida do texto na tela
        mov rsi,mensagem                ;Imprimir ou exibir a mensagem na tela
        mov rdx,13                      ;Quantidade de caracteres
        syscall                         ;Chama o sistema para preparar a saida
        mov rax,60                      ;Chamada para a saida do sistema
        xor rdi,rdi                     ;Executar a saida do sistema
        syscall                         ;Invocar o sistema operacional para fechar


        section .data
        mensagem: db 'Hello,word' ,10   ;O valor 10 representa a quebra de linha 

```

