# Policys

Detta är D-sektionen inom TLTHs policyer. Under "Releases" finns alla versioner av policyer sedan HTM1 2020. Om man följer commit-meddelanden finns det mer detaljerad historik.

## Användning

All text i repot ska vara skrivet på svenska.

### Efter ett sektionsmöte eller styrelsemöte

- Klona repot. `git clone https://github.com/Dsek-LTH/policys`
- Om du redan har klonat det, se till att du är på senaste revisionen. `git checkout master && git pull`
- Skapa en ny branch. `git checkout -b [branchnamn, tex HTM1-2020]`
- För varje motion och proposition:
  - Ändra policyns TeX-fil på det sätt som krävs för den nya motionen eller propositionen.
  - Efter varje införd ändring skapa en commit med ett meddelande innehållande mötesförkortningen för mötet och ändringen. T.ex. `git commit -m "[HTM1 2020] La till valberedningsrepresentant i tackpolicyn"` eller `git commit -m "[S19 2020] Skapade bilpolicy"`.
  - Om en mer detaljerad beskrivning behövs bör kroppen av commitens meddelande istället användas. `git commit`
- Se till att uppdatera policyns historik. Det vill säga om den har uppdaterats på ett styrelsemöte så lägg till vilket möte det var. Samma sak gäller för sektionsmöte. Finns ingen historik för policyn, skapa en.
- Pusha upp din branch till Github `git push -u origin [branchnamn, tex HTM1-2020]`
- Öppna en pull request på https://github.com/Dsek-LTH/policys/pulls för att få med dina ändringar i huvudbranchen.
- När denna godkänts så ska en ny release och PDF automatiskt skapas. Om det inte sker automatisk så ska man göra en egen release. Glöm i så fall inte att lägga till alla byggda PDF:er, inte bara de uppdaterade.

### När du vill göra redaktionella ändringar

Redaktionella ändringar ändrar inte betydelsen av en policy, utan ändrar enbart läsbarheten eller rättar små uppenbara fel. För att skapa en redaktionell ändring, följ instruktionerna för "Efter ett sektionsmöte" utöver att commit-meddelandet ska inte innehålla en mötesförkortning utan istället [Redaktionella ändringar]. T.ex. `git commit -m "[Redaktionella ändringar] Fixade stavfel"`. Döp gärna branchen till något i stil med "redaktionellaandringar".

### När du vill göra ändringar till repot

Ändringar som inte påverkar policyer direkt så som ändringar av continuous integration, README-filen eller att lägga till/ta bort en policy ska inte innehålla en mötesförkortning utan istället [Repoändringar]. T.ex. `git commit -m "[Repoändringar] Ändrade README"`. Döp gärna branchen till något i stil med "repoandringar".

### Dokumentklasser och paket

För att kunna bygga dokumenten behöver du ha D-seks latexfiler installerade på lämpligt ställe. [Du hittar dem här](https://github.com/Dsek-LTH/dsek-latex).
