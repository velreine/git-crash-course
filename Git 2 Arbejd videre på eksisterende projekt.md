# Git 2: Arbejd videre på eksisterende projekt 

## f.eks. arbejde videre på en anden computer, eller hent din makkers kode ned.



### Step 1: Clone eller Pull

```bash
git clone https://github.com/<brugernavn>/<repositorynavn>.git
# ELLER
git pull https://github.com/<brugernavn>/<repositorynavn>.git
# F.EKS.
git pull https://github.com/nicky/mit-nye-projekt.git
git clone https://github.com/nicky/mit-nye-projekt.git
```

git pull henter den aktive branch (typisk **master** branch), hvorimod 

git clone henter alle branches (**ikke kun** master)



### Step 2: Begynd at arbejde videre du har ændret index.html

Echo er bare lige for at få en hurtig filændring, du ville jo nok typisk arbejde videre i din **IDE** (**VS-Code**, **Visual Studio** osv.)

```bash
echo "<p>My awesome new change</p>" >> index.html
```



### Step 3: Stage de ændrede fil(er)  (den vil komme med på næste commit)

````bash
git add index.html
# Eller git add .
git add .
````



### Step 4: Opret en ny commit, alle "staged" changes vil komme med i denne commit.

```bash
git commit -m "Tilføjet en awesome ny change til index.html"
# -m er kort for message, giv altid en sigende besked hvad har du ændret/tilføjet/rettet osv.
```

### Step 5: Push din commit(s) til remote branchen.

```bash
# Hvis det er første gang du pusher:
git push -u origin master
# Hvis du har pushet før (du har sat --set-upstream origin master), så nøjes med git push.
git push
```

### Se dine opdaterede filer er nu pushet op på GitHub eller et andet Source Repository du bruger.



