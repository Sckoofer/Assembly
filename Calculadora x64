section .data
	bem_vindo db "Chega ae",10,10,0
	Cgh equ $ - bem_vindo
	Entrada_1 db "Digite um número: ",0
	Enter_1 equ $ - Entrada_1
	Entrada_2 db "Digite outro número: ",0
	Enter_2 equ $ - Entrada_2
	
	A_som db "1) A soma entre esses dois valores é: ",0
	summ equ $ - A_som
	
	A_sub db "2) A subtracao entre esses dois valores é: ",0
	subb equ $ - A_sub
	
	A_mul db "3) A multiplicacao entre esses dois valores é: ",0
	mull equ  $ - A_mul
	
	A_div db "4) A divisao entre esses dois valores é: ",0
	divv equ $ - A_div
	
	Pula_linha db 10,10,0
	num_lin equ $ - Pula_linha
section .bss
	Num_1: resb 2
	Num_2: resb 2
	Resultado: resb 2
section .text
	global _start
_start:
	mov rax, 1
	mov rdi, 1
	mov rsi, bem_vindo
	mov rdx, Cgh
	syscall
	
	mov rax, 1
	mov rdi, 1
	mov rsi, Entrada_1
	mov rdx, Enter_1
	syscall
	
	mov rax, 0
	mov rdi, 0
	mov rsi, Num_1
	mov rdx, 2
	syscall

	mov rax, 1
	mov rdi, 1
	mov rsi, Entrada_2
	mov rdx, Enter_2
	syscall
	
	mov rax, 0
	mov rdi, 0
	mov rsi, Num_2
	mov rdx, 2
	syscall
	
_Somar:

	mov rax, 1
	mov rdi, 1
	mov rsi, A_som
	mov rdx, summ
	syscall
	
	mov al, [Num_1]
	mov bl, [Num_2]
	
	;converte da tabela ASCII
	sub al, '0'
	sub bl, '0'
	
	;somar
	add al,bl
	
	;converte para a tabela ASCII
	add al, '0'
	
	mov [Resultado],al
	
	mov rax, 1
	mov rdi, 1
	mov rsi, Resultado
	mov rdx, 2
	syscall
	
	mov rax, 1
	mov rdi, 1
	mov rsi, Pula_linha
	mov rdx, num_lin
	syscall
	
_Subtrair:
	mov byte [Resultado], 0
	mov rax, 1
	mov rdi, 1
	mov rsi, A_sub
	mov rdx, subb
	syscall
	
	mov al, [Num_1]
	mov bl, [Num_2]
	
	;converte da tabela ASCII
	sub al, '0'
	sub bl, '0'
	
	;subtrair
	sub al,bl
	
	;converte para a tabela ASCII
	add al, '0'
	
	mov [Resultado],al
	
	mov rax, 1
	mov rdi, 1
	mov rsi, Resultado
	mov rdx, 2
	syscall
	
	mov rax, 1
	mov rdi, 1
	mov rsi, Pula_linha
	mov rdx, num_lin
	syscall
	
_Multiplicar:

	mov rax, 1
	mov rdi, 1
	mov rsi, A_mul
	mov rdx, mull
	syscall
	
	mov al, [Num_1]
	mov bl, [Num_2]
	
	;converte da tabela ASCII
	sub al, '0'
	sub bl, '0'
	
	;multiplicar
	mul bl
	
	;converte para a tabela ASCII
	add al, '0'
	
	mov [Resultado],al
	
	mov rax, 1
	mov rdi, 1
	mov rsi, Resultado
	mov rdx, 2
	syscall
	
	mov rax, 1
	mov rdi, 1
	mov rsi, Pula_linha
	mov rdx, num_lin
	syscall

_Dividir:

	mov rax, 1
	mov rdi, 1
	mov rsi, A_div
	mov rdx, divv
	syscall
	
	mov al, [Num_1]
	mov bl, [Num_2]
	
	;converte da tabela ASCII
	sub al, '0'
	sub bl, '0'
	
	;multiplicar
	div bl
	
	;converte para a tabela ASCII
	add al, '0'
	
	mov [Resultado],al
	
	mov rax, 1
	mov rdi, 1
	mov rsi, Resultado
	mov rdx, 2
	syscall
	
	mov rax, 1
	mov rdi, 1
	mov rsi, Pula_linha
	mov rdx, num_lin
	syscall


	mov rax, 60
	mov rdi, 0
	syscall
	
