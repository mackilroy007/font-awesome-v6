# font-awesome-cheet sheet

## Adapted to Font Awesome V6 based V5 cheatsheet
Type in console on font awesome cheat sheet site  
```
[].concat.apply([], Array.prototype.map.call(document.querySelectorAll('.cheatsheet-set'), e => e.id).map(e =>{
  let prefix = '';
  switch (e) {
      case 'regular':
          prefix = 'fa-regular'
          break;
      case 'solid':
          prefix = 'fa-solid'
          break;
      case 'light':
          prefix = 'fa-light'
          break;
      case 'brands':
          prefix = 'fa-brands'
          break;
        case 'duotone':
        prefix = 'fa-duotone'
        break;
  }

  return {
      id: e,
      prefix: prefix
  }
}).map(e => Array.prototype.map.call(document.querySelectorAll(`#${e.id} article.icon > dl > .select-all.word-wrap`), element => `${e.prefix} fa-${element.outerText}`))).map(e => `"${e}"`).join(',')
```

>unfortunatly there still is no updated v6 cheatsheet atm
