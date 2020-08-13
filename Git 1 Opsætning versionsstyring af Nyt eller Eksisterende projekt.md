# Git 1: Opsætning versionsstyring af Nyt eller Eksisterende projekt.



Nogen værktøjer frameworks med mere opretter nu-om-dage selv **.gitignore** fil og laver selv **git init** , hvis dette er tilfældet spring direkte til **Step 4** 

Du kan tjekke om den nuværende mappe du står i allerede er tracket af git vha:

```bash
git status
```

Hvis den siger "fatal: not a git repository (or any of the parent directories): git" -- så skal du starte fra step 1.



### Step 1 - Lav en ny mappe til dit projekt.

```bash
mkdir "%userprofile%\Desktop\mit-nye-projekt"
```



### Step 2 - Initialiser mappen med Git. (efter dette vil git tracke filerne i mappen)

```bash
cd "%userprofile%\Desktop\mit-nye-projekt"
git init
```



### Step 3 - Tilføj  .gitignore og README.md

Din .gitignore skal indeholde filer/mapper som git ikke skal versionsstyre. 

Din README.md er en mark-down fil som beskriver projektet, GitHub viser dette på forsiden af dit repository.

```bash
echo ".DS_Store" > .gitignore
echo "# Mit Nye Projekt" > README.md
```



### Step 4 - Stage ændrede filer (dvs. de kommer med på næste commit.)

* Hvis du er sprunget direkte til Step 4 med en eksisterende mappe er .gitignore og README.md nok allerede tilføjet anvend istedet her **git add .** (HUSK punktum efter add og mellemrummet imellem de 2.)

```bash
git add .gitignore README.md
#ELLER git add . tilføjer alle ændringer fra kommandopromptens nuværende placering og ned i undermapper (rekursivt).
git add .
# ELLER git add * wildcard tilføjer ALT (pas på.)
git add *
```



### Step 5 - Opret en ny commit, og giv commit en sigende besked.

```bash
# -m kort for message.
# Lav altid sigende messages, f.eks. hvad har du tilføjet/ændret/rettet osv.
git commit -m "Initial commit, tilføjet .gitignore og en README.md"

```



### Step 6 - Opret repository på Github 

* 6a:

![image-20200813203017383](C:\Users\Velreine\AppData\Roaming\Typora\typora-user-images\image-20200813203017383.png)

* 6b:

![image-20200813203138029](C:\Users\Velreine\AppData\Roaming\Typora\typora-user-images\image-20200813203138029.png)

Vælg et repository **navn**, **UNDLAD** at tilføje en .gitignore og **LAD-VÆR** at "**Initialize this repository with a README**" ❌

Tryk **Create Repository**

Efter repositoriet er oprettet har du nu et sted at opbevare din lokale versionsstyrede kode.



### Step 7 - Kobl din lokale-versionsstyrede mappe sammen med GitHub.

```bash
#git remote add <navn> <githublink>
git remote add origin https://github.com/<ditbrugernavn>/<ditrepositorynavn>.git
# Eksempel.
git remote add origin https://github.com/nicky/mit-nye-projekt.git

# Origin er bare et navn på den remote, man kan godt have flere remotes man kan pushe sine commits til.

```

### Tjek hvilke remotes der eksisterer i nuværende mappe:

```bash
git remote -v
```

### Fjern en remote (hvis du f.eks. har skrevet forkert)

```bash
git remote remove origin
```



### Step 8 - Push dine ændringer/commits til GitHub.

````bash
# git push -u <remote> <branch>
git push -u origin master
# ELLER (-u er forkotelse for --set-upstream)
git push --set-upstream origin master

````

Efterfølgende behøver du ikke at angive **origin** og **master**.

Du kan efterfølgende nøjes med:

```bash
git push
```





