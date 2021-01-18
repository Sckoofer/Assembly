;A palavra-chave push faz uma cópia do conteúdo da memória
;e armazena na stack.

;A palavra-chave pop busca aquele valor armazenado na stack
;e devolve para aquele que mandou armazenar


section .data
	campo db "  ",10
	tamanho equ $ - campo
section .text
	global _start:
_start:

	;antes do push
	mov rbx, 48
	mov [campo], rbx
	mov rax, 1
	mov rdi, 1
	mov rsi, campo
	mov rdx, tamanho
	syscall
	
	
	push rbx
	
	;resultado sem usar pop
	mov rbx, 49
	mov [campo], rbx
	mov rax, 1
	mov rdi, 1
	mov rsi, campo
	mov rdx, tamanho
	syscall
	
	;resultado com pop
	
	pop r15 ;não precisa ser um pop aplicado ao mesmo espaço
		;de memória que foi usado para fazer o push,
		;pode usar outro se quiser, não tem problema.
	mov [campo], r15
	mov rax, 1
	mov rdi, 1
	mov rsi, campo
	mov rdx, tamanho
	syscall
	
	
	mov rax, 60
	mov rdi, 1
	syscall
