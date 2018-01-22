# `polish-plurals`

# Description
Package meant mostly for Polish users who are looking for the simplest way to use nouns with numbers in Polish correctly.

This package takes into account complicated Polish grammar rules and allows you to specify different forms – 1 singular and 2 plural — of nouns to be used.

## Usage

In the simplest case you need to provide 3 forms of the noun and a number. Those 3 required forms are:

* singular nominative
* plural nominative
* plural genitive

```javascript
import { polishPlurals } from 'polish-plurals';

polishPlural("komentarz", "komentarze", "komentarzy", 1); // komentarz
polishPlural("komentarz", "komentarze", "komentarzy", 0); // komentarzy
polishPlural("komentarz", "komentarze", "komentarzy", 3); // komentarze
```

### Binding
You might consider `bind`ing the function to save some typing and avoid repetition:

```javascript
import { polishPlurals } from 'polish-plurals';

const commentsLabel = polishPlurals.bind(null, 'komentarz', 'komentarze', 'komentarzy');
commentsLabel(1); // komentarz
commentsLabel(0); // komentarzy
commentsLabel(3); // komentarze
```
