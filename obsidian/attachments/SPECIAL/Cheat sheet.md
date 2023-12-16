# Běžné

>Zvýraznění pomocí ">"

	blokové, čisté, no syntax highlighting formátování pomocí "Tab"

*Kurzíva*
_Taky kurzíva_
**tučné**
~~Přeškrtnutý text psaný AltGr + AlphaNum1~~
==zvýrazněné==

<!--Poznámka co není vidět na stránkách-->
%%druhá poznámka, line break jsou 2 mezery "  "%%

1. první
2. druhá
3. třetí

- švestka
- hruška
- pomelo

|Sloupec 1| Sloupec 2|
|---|---|
|bez mezery| mezera na začátku před PIPE|
***
# Advanced

LaTeX: $CO_2 + H_2O$

> [!Zvýraznění pomocí  ! a >]

Pro poznámku pod čarou  potřebujme zobáček nahoru [^1][^2]

[^1]: Psán AltGr + AlphaNum3 (podstatná je i ta dvojtečka)
[^2]: Obě poznámky budou vloženy až na konci stránky

[link](https://cs.wikipedia.org/wiki/Lilek_brambor)

[![ALT TEXT](https://upload.wikimedia.org/wikipedia/commons/thumb/7/7c/Aardappel_bloem_Parel_Solanum_tuberosum.jpg/258px-Aardappel_bloem_Parel_Solanum_tuberosum.jpg)](https://commons.wikimedia.org/wiki/File:Aardappel_bloem_Parel_Solanum_tuberosum.jpg "Květy lilku bramboru")

- [ ] Vytvořit list
- [x] Zaškrtnout druhé políčko listu
- [x] Zaškrtnout třetí políčko listu

```html
<html>
	<p>Pure code formátování</p>
</html>
```

```json
this {
	typ: "ŽSON",
	psáno: "AltGr AlphaNum7 pro ` "
},
that {
	Pepa: "doslova clueless"
}
```

```python
import this
for x in [0,1,2]
	print(x)
```

```rust
use std::mpsc

let x:String = "Džon";
println!("Ahoj {x:?}");
```

---