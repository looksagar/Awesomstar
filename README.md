# Awesomstar

Awesome (star)rating system with PHP, MySQL and pure JavaScript.

![](screenshot.jpg)

## Getting Started

```bash
# Get the latest snapshot
$ git clone --depth=1 https://github.com/pinceladasdaweb/Awesomstar.git
```

Add the following javascript in your page:

```html
<script src="path/to/awesomstar.min.js"></script>
<script>
    new Awesomstar();
</script>
```

The script depends on the following HTML markup:

```html
<span class="rating" data-rating-id="1" data-rating-val="3">
    <input class="star" type="radio" name="star" id="star-1" value="1"><label for="star-1">1</label>
    <input class="star" type="radio" name="star" id="star-2" value="2"><label for="star-2">2</label>
    <input class="star" type="radio" name="star" id="star-3" value="3"><label for="star-3">3</label>
    <input class="star" type="radio" name="star" id="star-4" value="4"><label for="star-4">4</label>
    <input class="star" type="radio" name="star" id="star-5" value="5"><label for="star-5">5</label>
</span>
```

The values below are sent from the database for the JavaScript to update the status of the rating of each element:

| Value                              | Description                                                 |
| ---------------------------------- |:-----------------------------------------------------------:|
| **data-rating-id**                 | The id of the element in the database.                      |
| **data-rating-val**                | The average value of the vote.                              |

After the user clicks the value of the desired rating, is sent via POST to the back end the following values:

| Value                              | Description                                                 |
| ---------------------------------- |:-----------------------------------------------------------:|
| **id**                             | The id of the element in the database.                      |
| **rating**                         | The value of the rating ranges from 1 to 5.                 |

## How to run a callback function after vote:

```html
<script>
    new Awesomstar({
        callback: function (data) {
            console.log(data);
        }
    });
</script>
```

An error message or success is returned, providing feedback to the user.

## Browser support

![IE](https://cloud.githubusercontent.com/assets/398893/3528325/20373e76-078e-11e4-8e3a-1cb86cf506f0.png) | ![Chrome](https://cloud.githubusercontent.com/assets/398893/3528328/23bc7bc4-078e-11e4-8752-ba2809bf5cce.png) | ![Firefox](https://cloud.githubusercontent.com/assets/398893/3528329/26283ab0-078e-11e4-84d4-db2cf1009953.png) | ![Opera](https://cloud.githubusercontent.com/assets/398893/3528330/27ec9fa8-078e-11e4-95cb-709fd11dac16.png) | ![Safari](https://cloud.githubusercontent.com/assets/398893/3528331/29df8618-078e-11e4-8e3e-ed8ac738693f.png)
--- | --- | --- | --- | --- |
IE 9+ ✔ | Latest ✔ | Latest ✔ | Latest ✔ | Latest ✔ |

## Contributing

Check [CONTRIBUTING.md](CONTRIBUTING.md) for more information.

## History

Check [Releases](https://github.com/pinceladasdaweb/Awesomstar/releases) for detailed changelog.

## License

[MIT](LICENSE)