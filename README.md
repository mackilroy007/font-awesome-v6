# font-awesome-cheet sheet 

## Font Awesome V6 Json 

### Using Node js
1. download icons.json file
2. execute following code in node js:
```
var json = require("{file-path}/icons.json"); var FA6Json = {}; Object.keys(json).forEach(iconName => { const icon = json[iconName]; icon.styles.forEach(style => { if (!FA6Json[style]) { FA6Json[style] = []; } FA6Json[style].push(`fa-${style} fa-${iconName}`); }) }); require("fs").writeFile("{file-path}/FA6icons.json", JSON.stringify(FA6Json,null,2), () => {});
```
>(less ram intensive)

### Using Browser
1. step copy Font Awesome kit (pro or free)
2. open metadata/icons.json
3. within browser paste following code: 
```
var json = { copy and past lates font awesome 6x metadata/icons.json }; 
var FA6Json = {}; Object.keys(json).forEach(iconName => { const icon = json[iconName]; icon.styles.forEach(style => { if (!FA6Json[style]) { FA6Json[style] = []; } FA6Json[style].push(iconName); }) }); 
```
4. copy object from console 
>(very ram intensive and might crash your dev tools and or cause errors)

## Adapted to Font Awesome V6 based V5 cheatsheet (old)
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
