# Git 3 : Vigtigste kommandoer

````bash
# Initialiser en ny mappe til at blive versionsstyret af git.
git init

# Tilføj "stage" dine ændringer (nye filer, ændrede filer, slettede filer) osv.
git add <filnavn>
git add * # < pas på.
git add .

# Opret en ny commit (alle staged changes kommer med på denne commit), sammen med en sigende besked.
git commit -m "Fixed that shitty bug in ProductController.cs bla bla..."

# Tilføj ny remote
git remote add origin https://github.com/nicky/mit-nye-projekt

# Fjern remote
git remote remove origin

# List remotes
git remote -v

# Push dine ændringer til dit remote repository (som f.eks. er hosted på GitHub)
git push -u origin master # < Første gang
git push # < Efterfølgende gange.

# Git status (når du skal finde ud af hvad fuck der foregår)
git status

# Gem dine ændringer ned i en "stash"
# En stash er bare en beholder til de lokale ændringer du må have lavet på filerne i projektet.
# Du kan "stash" dine ændringer, det vil sætte filerne tilbage til deres stadie inden du ændrede dem.
git stash

# Når du har brug for at se dine ændringer igen kan du "poppe" din stash
# Dette vil medføre konflikter hvis de ændringer som du har stashet ikke længere kan merges ind i filernes nuværende stadie problemfrit.
git stash pop

# Hiv ændringer eller hele projektet ned (alle branches)
git pull https://github.com/nicky/mit-nye-projekt
git pull

# Hiv kun den aktive branch ned (typisk master)
git clone https://github.com/nicky/mit-nye-projekt

# Opret en ny branch
git checkout -b my-new-feature-branch
git checkout -b v2.0

# Skift branch
git checkout master
git checkout my-new-feature-branch
git checkout v2.0

# Restore ændringer på fil(er) som er ændret siden sidste commit.
# ((Super power Ctrl+Z))
git restore .
git restore index.html

# Unstage ændringer dette vil fjerne ændringen fra ændringer som kommer med på næste commit.
# Du beholder den ændrede fil og dens ændringer den kommer bare ikke med på din commit før du laver en git add som stager ændringen igen.
git restore --staged index.html

# Uncommit 1! commit (eller x commits tallet efter ~) (hvis du f.eks. finder ud af at en fil ikke skulle med i denne commit)
# Dette er FØR du laver en git push.
# Tilde character (~) Windows:  Aktiver Num Lock, Hold ALT tryk 126 på NUMPAD. (ALT + 126)
git reset --soft HEAD~1


````

