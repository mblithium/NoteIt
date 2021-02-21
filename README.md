# NoteIT

It is a browser extension built using HTML, CSS and Javascipt. It is used for note taking with saving and opening facilities.
Once it is opened you can switch from tab to tab without minimizing your browser tab.

![NoteIt](https://github.com/fluffyP4nd4/NoteIt/blob/main/images/noteit.png)

## Installation

Use git to clone the repo to your Local machine

```
git  clone  https://github.com/fluffyP4nd4/NoteIt.git
```

To run this extension on your browser click the links and follow the given steps

### Chrome, FireFox,Opera,IE, Safari

### Contribution

The following code was added:

- Clear fields button:

```html
<tr>
	<td><button id="clean">Clean</button></td>
</tr>
```

```javascript
//Clean fields
var btn3 = document.getElementById("clean");
btn3.addEventListener("click", () => {
	cleanFields();
});
```

- Clear fields when saving a file:

```javascript
//Function Clean fields
function cleanFields() {
	document.querySelector("#text").value = "";
	document.getElementById("fileLoad").value = [];
	document.getElementById("flname").value = "";
}
```

- Validate that filename field is not empty when saving:

```javascript
//Check that the file name field is not empty
if (fileName === "") {
	alert("You must upload a name for the file");
	return;
}
```

- Validate that a file is selected when the open button is clicked:

```javascript
//valid if I select the file
if (!fileToRead) {
	alert("You must select a file to open it");
	return;
}
```
