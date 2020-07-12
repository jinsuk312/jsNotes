# jsNotes

Notes on Javascript

##Store values

```var Age = 2;
let name = 'Lamby';
const isDog = 'true';

var userName = prompt('Whats your name?');
var confirmName = confirm('Did you put the correct name?');```

##IF/ELSE - Prompt user at browser
```if(userName & confirmName){
    alert(userName + ' would you like to adopt ' + userName + '?';
}else{
    alert('Refresh the page and enter the correct name');
}```

##Writing on the Page
```// document.write() overwrites the entire page. We don't normally use this, but we will today for simplicity
			document.write('Welcome to our page ' + userName);```