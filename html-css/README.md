# HTML

Responsive design
Flexbox
- images 100%
- layouting met controle over 1 dimentie
- op technisch vlak zeker een uitdaging
  - image size
    - picture en source attributen
  - tables
    - Heel horizontaal georienteerd

Tables voor layouting
- Zeer traag
- Veel tijd verspillen met aanpassingen

```
@media screen and (min-width: 500px){
	div {
	}
}
```

## CSS grid
- Layouting met controle over 2 dimenties
```
display: grid;
grid-template-columns: 100px 200px 300px;

grid-template-columns: 100px minmax(20%, 50em) 300px;
grid-template-rows: ...
grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
```

Fraction unit
- Split table direct in correcte grootte
- `grid-template-colunms: 1fr 2fr 2fr`
  - hetzelfde als `grid-template-colunms: 20% 40% 40%`

```
grid-auto-columns
grid-column: 4;
grid-column: 4 / 7; // Gaat tot het begin van 7
grid-column: 1 / -1; // Eerste tot laatste
grid-column: 1 / span 2; // Eerste tot en met tweede
grid-column: span 1 / 4; // Derde tot vierde
```

```
grid-gap: 2em 1em;
grid-auto-rows: 100px;
grid-auto-flow: 10em;
grid-auto-flow: row dense;
grid-auto-fit;
grid-auto-fill:;
```

```
grid-template-areas: "test" "test2";
grid-area: "test";
```

## Accessibility

