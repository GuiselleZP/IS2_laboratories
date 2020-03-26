# Laboratorio 1 - Git

* **Nombre del profesor:** Sebastian David Moreno Bernal
* **Fecha límite:** Viernes 27 de Marzo de 2020.
* **Nombre del estudiante:** Guiselle Tatiana Zambrano Penagos

## Introduction Sequence

### Git Commits

* **Comandos utilizados:**

	```
	git commit
	git commit
	```
* **Screenshot:**
	
	![git commits](./images/N1_00.png)\

### Git Branches

* **Comandos utilizados:**

	```
	git checkout -b bugFix
	```
* **Screenshot:**
	
	![git branch and checkout](./images/N1_01.png)\

### Branches and Merging

* **Comandos utilizados:**

	```
	git checkout -b bugFix
	git commit
	git checkout master
	git commit
	git merge bugFix
	```
* **Screenshot:**
	
	![branches and merging](./images/N1_02.png)\

### Git Rebase

* **Comandos utilizados:**

	```
	git checkout -b bugFix
	git commit
	git checkout master
	git commit
	git checkout bugFix
	git rebase master	
	```
* **Screenshot:**
	
	![](./images/N1_03.png)\

## Ramping Up
### Moving around in Git

* **Comandos utilizados:**

	```
	git checkout C4
	```
* **Screenshot:**
	
	![](./images/N1_04.png)\

### Relative Refs

* **Comandos utilizados:**

	```
	git checkout bugFix
	git checkout HEAD^
	```
* **Screenshot:**
	
	![relatie refs](./images/N2_00.png)\

### The "~" operator

* **Comandos utilizados:**

	```
	git checkout master
	git checkout HEAD~2
	git branch -f master c6
	git branch -f bugFix HEAD^
	```
* **Screenshot:**
	
	![operador ~](./images/N2_01.png)\

### Reversing Changes in Git

* **Comandos utilizados:**

	```
	git reset HEAD^
	git checkout pushed
	git revert HEAD
	```
* **Screenshot:**
	
	![reversing changes](./images/N2_02.png)\

## Moving Work Around

### Git Cherry-pick 

* **Comandos utilizados:**

	```
	git cherry-pick c3 c4 c7
	```
* **Screenshot:**
	
	![cherry-pick](./images/N3_00.png)\

### Git Interactive Rebase

* **Comandos utilizados:**

	```
	git rebase -i HEAD~4
	# c3, c5, c4
	```
* **Screenshot:**
	
	![Interactive Rebase](./images/N3_01.png)\

## A Mixed Bag

### Locally stacked commits

* **Comandos utilizados:**

	```
	git checkout master
	git cherry-pick c4
	```
* **Screenshot:**
	
	![locally stacked commits](./images/N4_00.png)\

### Juggling Commits

* **Comandos utilizados:**

	```
	git rebase -i HEAD~2
	git rebase -i HEAD~1
	git rebase -i HEAD~2
	git branch -f master c3'''
	```
* **Screenshot:**
	
	![juggling commits](./images/N4_01.png)\

### 

* **Comandos utilizados:**

	```
	```
* **Screenshot:**
	
	![](./images/N1_00.png)\

### 

* **Comandos utilizados:**

	```
	```
* **Screenshot:**
	
	![](./images/N1_00.png)\

### 

* **Comandos utilizados:**

	```
	```
* **Screenshot:**
	
	![](./images/N1_00.png)\

### 

* **Comandos utilizados:**

	```
	```
* **Screenshot:**
	
	![](./images/N1_00.png)\


	```
	```
