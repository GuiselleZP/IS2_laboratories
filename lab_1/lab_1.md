# Laboratorio 1 - Git

* **Nombre del profesor:** Sebastian David Moreno Bernal
* **Fecha límite:** Viernes 27 de Marzo de 2020.
* **Presentado por:** Guiselle Tatiana Zambrano Penagos

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

### Juggling Commits 2

* **Comandos utilizados:**

	```
	git checkout HEAD~2
	git cherry-pick c2
	git checkout HEAD~1
	git cherry-pick c2'
	git cherry-pick c3
	git branch -f master c3'
	```
* **Screenshot:**
	
	![Juggling commits 2](./images/N4_02.png)\

### Git Tags 

* **Comandos utilizados:**

	```
	git tag v0 c1
	git tag v1 c2
	git checkout c2
	```
* **Screenshot:**
	
	![Tags](./images/N4_03.png)\

### Git Describe 

* **Comandos utilizados:**

	```
	git describe c2
	git describe c4
	git describe c6
	git describe c1
	git describe c3
	```
* **Screenshot:**
	
	![describe](./images/N4_04.png)\

## Advanced Topics

### Rebasing Multiple Branches

* **Comandos utilizados:**

	```
	git rebase master bugFix
	git rebase bugFix side~2
	git rebase HEAD side~1
	git rebase HEAD side
	git rebase side another
	git branch -f master another
	```
* **Screenshot:**
	
	![rebasing](./images/N5_00.png)\


	```
	```
### Specifying Parents

* **Comandos utilizados:**

	```
	git branch -f bugWork HEAD~^2~
	```
* **Screenshot:**

	![specific parents](./images/N5_01.png)\

### Branch Spaghetti

* **Comandos utilizados:**

	```
	git checkout one
	git cherry-pick c4
	git cherry-pick c3
	git cherry-pick c2
	git checkout two
	git cherry-pick c5
	git cherry-pick c4'
	git cherry-pick c3'
	git cherry-pick c2'
	git branch -f three c2
	```
* **Screenshot:**

	![Branch spaghetti](./images/N5_02.png)\

## Push & Pull -- Git Remotes!

### Our Command to create remotes

* **Comandos utilizados:**

	```
	git clone
	```
* **Screenshot:**

	![git clone](./images/N6_00.png)\

### Git Remote Branches 

* **Comandos utilizados:**

	```
	git commit
	git checkout o/master
	git commit
	```
* **Screenshot:**

	![remote branches](./images/N6_01.png)\

### Git Fetch

* **Comandos utilizados:**

	```
	git fetch
	```
* **Screenshot:**

	![git fetch](./images/N6_02.png)\

### Git Pull

* **Comandos utilizados:**

	```
	git pull
	```
* **Screenshot:**

	![git pull](./images/N6_03.png)\

### Simulating Collaboration

* **Comandos utilizados:**

	```
	git commit
	git commit
	git clone
	git branch -f master c1
	git commit
	git pull
	```
* **Screenshot:**

	![Simulating Collaboration](./images/N6_04.png)\

### git push

* **Comandos utilizados:**

	```
	git commit
	git commit
	git push
	```
* **Screenshot:**

	![git push](./images/N6_05.png)\

### Diverged Work

* **Comandos utilizados:**

	```
	git clone
	git fakeTeamwork
	git commit
	git pull --rebase
	git push
	git fakeTeamwork
	```
* **Screenshot:**

	![Diverged Work](./images/N6_06.png)\

### Remote Rejacted

* **Comandos utilizados:**

	```
	git reset --hard o/master
	git checkout -b feature c2
	git push origin feature
	```
* **Screenshot:**

	![Remotes Rejacted](./images/N6_07.png)\

## To origin and Beyoun -- Advanced Git Remotes!

### Merging feature branches

* **Comandos utilizados:**

	```
	git fetch
	git rebase o/master side1
	git rebase side1 side2
	git rebase side2 side3
	git rebase side3 master
	git push
	```
* **Screenshot:**

	![Merging feature branches](./images/N7_00.png)\

### Why no merge?

* **Comandos utilizados:**

	```
	git checkout master
	git pull
	git merge side1
	git merge side2
	git merge side3
	git push
	```
* **Screenshot:**

	![why no merge](./images/N7_01.png)\

### Remote-Tracking branches

* **Comandos utilizados:**

	```
	git checkout -b side o/master
	git commit
	git pull --rebase
	git push
	```
* **Screenshot:**

	![remote-tracking](./images/N7_02.png)\

### Push Arguments

* **Comandos utilizados:**

	```
	git push origin master
	git push origin foo
	```
* **Screenshot:**

	![push arguments](./images/N7_03.png)\

### <place> argument details

* **Comandos utilizados:**

	```
	git push origin master^:foo
	git push origin foo:master
	```
* **Screenshot:**

	![argument details](./images/N7_04.png)\

### Git fetch arguments

* **Comandos utilizados:**

	```
	git fetch origin master~1:foo
	git fetch origin foo:master
	git checkout foo
	git merge master
	```
* **Screenshot:**

	![fetch arguments](./images/N7_05.png)\

### Oddites of <surce>

* **Comandos utilizados:**

	```
	git push origin :foo
	git fetch origin :bar
	```
* **Screenshot:**

	![oddites](./images/N7_06.png)\

### Git pull arguments

* **Comandos utilizados:**

	```
	git pull origin bar:foo
	git pull origin master:side
	```
* **Screenshot:**

	![pull arguments](./images/N7_07.png)\

