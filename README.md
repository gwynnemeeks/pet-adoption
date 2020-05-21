# Pet Adoption Homework

## Description
This is a project to show off my first DOM String to build and print information cards to the DOM. It is also my first experience with Event Listeners and filtering.

### Feature List
* Show all pets in a collection.
* Allows pink styling and soft fonts into your life.
* Filter pets by type.
* Reset filter button.

## Screenshots
![image](https://user-images.githubusercontent.com/63276406/82616961-4eef6b80-9b94-11ea-8318-e5efb0ccc17d.png)

## How To Run
1. Clone down this repo
1. Use your favorite http server (like [http-server](https://www.npmjs.com/package/http-server)) to serve it up (`hs`)
1. In your browser, go where it's being served (default is localhost:8080)

## Contributors
* [Gwynne Meeks](https://github.com/gwynnemeeks)

## TODO/Feature Request
- [ ] Finish the event listener filters
- [ ] remove pets with broken picture links.

code block example:
```js
const buildPetCards = (petsCollection) => {
    let domString = '';
    for (let i = 0; i < petsCollection.length; i++) {
        domString += '<div class="pets">';
        domString += `<h2>${petsCollection[i].name}</h2>`;
        domString += `<img src="${petsCollection[i].imageUrl}" alt="">`;
        domString += `<h3>${petsCollection[i].color}</h3>`;
        domString += `<p>${petsCollection[i].specialSkill}</p>`;
        domString += `<h3>${petsCollection[i].type}</h3>`;
        domString += '</div>';
    }
    printToDom('#pets', domString);
    
};
```