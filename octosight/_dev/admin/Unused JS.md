

> [!fail]
> Tato stránka není určena pro širokou veřejnost
> Pokud nevíte co děláte, nic zde neupravujte

```dataviewjs
let currentDate = new Date(Date.now());

dv.table(["File", "Folder", "Last Modified"],
  dv.pages()
  .where(p => moment(p.file.mtime.toString()).isSame(currentDate.toString(), 'day'))
  .sort(p => p.file.mtime, 'desc')
  .map(p => [
    p.file.link,
    p.file.folder,
    moment(p.file.mtime.toString()).fromNow(),
  ])
);
```

```dataviewjs
let currentDate = new Date(Date.now());

dv.table(["File", "Folder", "Last Modified", "Time Ago"],
  dv.pages()
  .where(p => moment(p.file.mtime.toString()).isSame(currentDate.toString(), 'day'))
  .sort(p => p.file.mtime, 'desc')
  .map(p => {
    const lastModified = new Date(p.file.mtime);
    const formattedLastModified = `${lastModified.getDate().toString().padStart(2, '0')}.${(lastModified.getMonth() + 1).toString().padStart(2, '0')}.${lastModified.getFullYear()} ${lastModified.getHours().toString().padStart(2, '0')}:${lastModified.getMinutes().toString().padStart(2, '0')}:${lastModified.getSeconds().toString().padStart(2, '0')}`;

    return [
      p.file.link,
      p.file.folder,
      formattedLastModified,
      moment(p.file.mtime.toString()).fromNow(),
    ];
  })
);
```

Poslední viditelná frontend aktualizace (desync octosight-html značí chybu při transpilaci):

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
