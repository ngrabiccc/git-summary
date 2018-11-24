# git(hub)

Ovo je podsjetnik na Krešino predavanje o git(hub)u, te par smjernica i konvencija vezanih uz UI development. Kako i sam shvatio git tek nakon što sam izbrisao 60-tak commita Mariju, volio bi da se vama ne dogodi slična situacija.

Ako u bilo kojem dijelu zapnete, ili imate pitanja, udrite mail: **[drazen@dump.hr](mailto:drazen@dump.hr)**

Datoteka je podjeljenja na:

 - Terminologija
 - Konvencije
 - Setup
 - Komande
 - Upotreba (domaći rad)
 - Taskovi (izrazitno bitno za UI development)

## Terminologija
> Repository

"Folder" projekta koji sadrži source kod.
> Lokalno

Sadržaj koji postoji na našem računalu, ali nije postavljen na remote repository.
> Remote

Sadržaj koji se nalazi online, bio to server ili platforme poput github-a.

> Push/pull/sync

Dohvatiti, poslati, sinkronizirati verziju koda sa remote-om

> Pull request

Zahtjev za spajanje jednog brancha u drugi.

> Merge

Spajanje dvaju brancheva.

> Conflict

Kada dva filea imaju izmjene na istim lokacijama, događa se conflict unutar kojega se ručno bira koja će izmjena na kraju ostati.

## Konvecije
1. **Sve** pišite na engleskom jeziku. Bit će situacija u kojima će se pridružiti neki stranac, pa je bitno da su svi na istoj razini.
2. Dijelite posao na manje cjeline (taskove), kako se nebi zapleli u vlasitom kodu.
3.  Taskove - brancheve (zadnja sekcija) zapisujete obliku P(rvo slovo imena)prezime-B(roj)-naziv_taska, u primjeru `dbaric-7-simple_button`
4. Imenujte commite po "koracima" taska. Na gornjem primjeru `Created button structure` i `Styled button`

## Setup

Doslovno ova tri linka na linku ispod:
https://help.github.com/articles/set-up-git/

## Komande (osnovne) 

> `git init`
> "postavljanje" repositorya

> `git remote add origin https://github.com/_user_/_repo_.git`
> umjesto linka na repo, ovim unutar foldera u kojem ste stavili `git init` postavljate ključnu riječ remote

> `git add .`
> dohvaćanje svih promjena koje su nastale od zadnjeg commita

> `git commit -m "Commit message"`
> kreiranje commita

> `git checkout (-b) branchName`
> "skakanje" u branch, uz `-b` kreiranje i skakanje u branchName

> `git push / git push origin branchName`
> slanje commita na master ili određeni branchName

> `git pull / git pull origin branchName`
> dohvaćanje promjena sa mastera ili određenog branchNamea

## Upotreba

Kreirati repository. Dodati me kao contributora (dbaric ili drazen@dump.hr). Kada obavite task (1) javiti na Slack.
|       Task number         |Task name|Task description|
|----------------|-------------------------------|-----------------------------|
|/|Setup|Create a file named `text.txt`. File content: `Dobar dan. Ja san u masteru`. Commit and push to master.         |
|1|Branching|Open a new branch, edit `text.txt` so it reads `Dobar dan. Ja NISAN u masteru`. Push branch remotly and open pull request ([click if you get stuck](https://help.github.com/articles/creating-a-pull-request/#creating-the-pull-request)). Assign me for code review and contact me on Slack.        |
|/|Merge|After I approve your pull request, resolve conflict (as you wish) using web editor and delete the branch. [(click if you get stuck again)](https://help.github.com/articles/resolving-a-merge-conflict-on-github/)|



## Taskovi

Taskovi su sistematičke cjeline po kojima se dijeli proces u programiranju. U UI developmentu, njih određuje development lead, ali kako ćete tijekom internshipa većinom raditi sami, morate znati kako ih i kreirati.

Ne postoje pravila po kojima će neki task biti zadan (ako ste dovoljno odvažni, može vam i cijeli site biti jedan task), ali najbolje se tijekom programiranja držati određenih konvecija, a one koje ćemo se mi držati nalaze se ispod.

Kod UI developmenta, taskove dijelimo na neke vizualne cjeline. Pogledajmo primjer Medium-a, gdje ćemo dizajn cijele stranice podijeliti u manje grupe (koje će biti branchevi) kako bi znali na kojem se što radilo.
![
](https://i.pinimg.com/originals/5f/2a/1e/5f2a1ec32255339dd27cb77d62cf46bd.png)

|       Task number         |Task name|Task description|
|----------------|-------------------------------|-----------------------------|
|1|Navigation            |Site navigation (which consists of logo, links, search and user avatar)            |
|2|Content |Left container - articles            |
|3|Sidebar|List on the right, probably links|


