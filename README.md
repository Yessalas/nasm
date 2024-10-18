# Estudos de comandos NASM
## priimeiros comandos

* Pragrama hello world

```Assembly
global_start

    section .text
    _start:
        mov rax,1       ;prepara o sistema para a escrita de um texto
        mov rdi,1       ;prepara a saida do teto na tela
        mov rsi,mensagem ;exibir a mensagem na tela
        mov rdx,13      ;quantidade de caracteres
        syscall         ;chama o sistema para preparar a saida
        mov rax,60      ;chamada para a saida do sistema
        xor rdi, rdi    ; executar a saida do sistema
        syscall         ; chama o sistema opracional para fechar

        section .data
        mensagem:db' Hello Word',10 ; O valor 10 representa a quebra de linha
        
```