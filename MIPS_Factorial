.data
	message: .asciiz "The Factorial of 1 to 10 Is:"
	message2: .asciiz "\n "
.text

  .globl main
  
	main:
	
	li $v0, 4
	la $a0, message
	syscall
	
	addi $t0, $zero, 1
	addi $t1, $zero, 1
	addi $t2, $zero, 10
	
	jal loop
	
	li $v0, 10
	syscall
	
  .globl loop
	
	loop:
	
	bgt $t1, $t2, end
	
	mul $t0, $t0, $t1
	
	li $v0, 4
	la $a0, message2
	syscall
	
	li $v0, 1
	move $a0, $t0
	syscall
	
	addi $t1, $t1, 1
	j loop
	
	end:
	jr $ra
