![[Index16-12-2023_16_03_58.excalidraw.svg]]
%%[[Index16-12-2023_16_03_58.excalidraw|🖋 Edit in Excalidraw]]%%
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
LIST FROM "literatura" SORT file.ctime DESC
```
%%## Mluvnice
## Sloh
# Chemie
# Francouzština
# Fyzika
# Historie
# IT
# Matika%%
# ZSV
```dataview
LIST FROM "zsv" SORT file.ctime DESC
```
***
<font size = "2">
Naposledy aktualizováno:
</font>

```dataviewjs
let currentDate = new Date(Date.now());
dv.table([],
  dv.pages()
  .sort(p => p.file.mtime, 'desc')
  .slice(0, 1)  // latest entry
  .map(p => {
    const lastModified = new Date(p.file.mtime);
    return [`${lastModified.getDate().toString().padStart(2, '0')}.${(lastModified.getMonth() + 1).toString().padStart(2, '0')}.${lastModified.getFullYear()} ${lastModified.getHours().toString().padStart(2, '0')}:${lastModified.getMinutes().toString().padStart(2, '0')}:${lastModified.getSeconds().toString().padStart(2, '0')}`];
  })
);

```