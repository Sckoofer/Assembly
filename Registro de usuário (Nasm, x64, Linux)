
section .data
	texto db "Mostre o nome do usuário: ",0
	tamanho_texto equ $ - texto

	texto2 db 10,"Mostre a idade do usuário: ",0
	tamanho_texto2 equ $ - texto2
	
	Pos_texto db  "O nome  é: ",0
	Pos_textoTam equ $ - Pos_texto
	
	Pos_texto2 db "O idade é: ",0
	Pos_texto2Tam equ $ - Pos_texto2
	
	Menu_Texto db "Digite 1 para escrever o  nome ",10,0
	TamMenuOpc1 equ $ - Menu_Texto
	Menu_Texto2 db "Digite 2 para escrever a idade",10,"->",0
	TamMenuOpc2 equ $ - Menu_Texto2
	
	Pula_linha db 10,10,0
	pl equ $ - Pula_linha
	
	
section .bss
	
	menu_opcao: resb 2
	entrada_nome: resb 6
	entrada_idade: resb 3
	
section .text
	global _start
	global _Apresentacao
	global _Recebe_Nome
	global _Recebe_Idade


_start:

	mov rax, 1
	mov rdi, 1
	mov rsi, Menu_Texto
	mov rdx, TamMenuOpc1
	syscall
	
	mov rax, 1
	mov rdi, 1
	mov rsi, Menu_Texto2
	mov rdx, TamMenuOpc2
	syscall
	
	mov rax, 0
	mov rdi, 0
	mov rsi, menu_opcao
	mov rdx, 2
	syscall
	

	mov al, [menu_opcao]
	sub al, '0'
	cmp  al, 1
	je _Recebe_Nome
	call _Apresentacao
		
	cmp  al, 2
	je _Recebe_Idade
	call _Apresentacao
	

	mov rax, 1
	mov rdi, 1
	mov rsi, Menu_Texto
	mov rdx, TamMenuOpc1
	syscall
	
	call _Apresentacao
	

	

	
_Recebe_Nome:

	mov rax, 1
	mov rdi, 1
	mov rsi, texto
	mov rdx, tamanho_texto
	syscall
	
	mov rax, 0
	mov rdi, 0
	mov rsi, entrada_nome
	mov rdx, 6
	syscall
	
	ret
	
	
_Recebe_Idade:

	mov rax, 1
	mov rdi, 1
	mov rsi, texto2
	mov rdx, tamanho_texto2
	syscall
	
	mov rax, 0
	mov rdi, 0
	mov rsi, entrada_idade
	mov rdx, 2
	syscall
	
	ret

_Apresentacao:
	
	mov rax, 1
	mov rdi, 1
	mov rsi, Pula_linha
	mov rdx, pl
	syscall
	
	mov rax, 1
	mov rdi, 1
	mov rsi, Pos_texto
	mov rdx, Pos_textoTam
	syscall
	
	mov rax, 1
	mov rdi, 1
	mov rsi, entrada_nome
	mov rdx, 15
	syscall

	mov rax, 1
	mov rdi, 1
	mov rsi, Pula_linha
	mov rdx, pl
	syscall

	mov rax, 1
	mov rdi, 1
	mov rsi, Pos_texto2
	mov rdx, Pos_texto2Tam
	syscall
	
	mov rax, 1
	mov rdi, 1
	mov rsi, entrada_idade
	mov rdx, 2
	syscall
	
	mov rax, 1
	mov rdi, 1
	mov rsi, Pula_linha
	mov rdx, pl
	syscall

	mov rax, 60
	mov rdi, 0
	syscall
	
	ret
	


	
