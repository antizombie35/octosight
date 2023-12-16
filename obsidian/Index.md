![[Index16-12-2023_16_03_58.excalidraw.svg]]
%%[[Index16-12-2023_16_03_58.excalidraw.md|🖋 Edit in Excalidraw]]%%
<font size = "2">**O**pen sour**c**e **T**ranspiled **O**bsidian-based **S**ynced **I**nterconnected **G**ithub-hosted **H**yperlinked ar**t**ifact 
... or an octopus with laser sight
[Originální repo link](https://github.com/antizombie35/octosight)
</font>
# Biologie
```dataview
LIST FROM "biologie" SORT file.ctime DESC
```
# Literatura
```dataview
LIST FROM "literatura" SORT file.ctime
```
%%## Mluvnice
## Sloh
# Chemie
# Francouzština
# Fyzika
## Teorie
## Cvičení
# Historie
# IT
# Matika
# ZSV%%
```dataview
LIST FROM "zsv" SORT file.ctime
```
***
Naposledy aktualizováno:
```dataviewjs
let currentDate = new Date(Date.now());
dv.table([],
  dv.pages()
  .where(p => moment(p.file.mtime.toString()).isSame(currentDate.toString(), 'day'))
  .sort(p => p.file.mtime, 'desc')
  .slice(0, 1)  // Take only the first (latest) entry
  .map(p => {
    const lastModified = new Date(p.file.mtime);
    return [`${lastModified.getDate().toString().padStart(2, '0')}.${(lastModified.getMonth() + 1).toString().padStart(2, '0')}.${lastModified.getFullYear()} ${lastModified.getHours().toString().padStart(2, '0')}:${lastModified.getMinutes().toString().padStart(2, '0')}:${lastModified.getSeconds().toString().padStart(2, '0')}`];
  })
);

```

