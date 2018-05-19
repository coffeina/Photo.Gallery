# Photo Gallery 

[Link to gallery](https://coffeina.github.io/Photo.Gallery/)

![screenshot1](assets/1.png)

![screenshot2](assets/2.png)

![screenshot1](assets/3.png)

## Looping through images:

```
for (var i = 1; i <= 5; i++) {
    var newImage = document.createElement('img');
    newImage.setAttribute('src', 'images/pic' + i + '.jpg');
    thumbBar.appendChild(newImage);
    newImage.onclick = function(e) {
        var imgSrc = e.target.getAttribute('src');
        displayImage(imgSrc);
    }
}
```

##  Wiring up the Darken/Lighten button

```
btn.onclick = function() {
    var btnClass = btn.getAttribute('class');
    if (btnClass === 'dark') {
        btn.setAttribute('class', 'light');
        btn.textContent = 'Lighten';
        overlay.style.backgroundColor = 'rgba(0,0,0,0.5)';
    } else {
        btn.setAttribute('class', 'dark');
        btn.textContent = 'Darken';
        overlay.style.backgroundColor = 'rgba(0,0,0,0)';
    }
}
```

## License

Photo.Gallery is available under the MIT license.