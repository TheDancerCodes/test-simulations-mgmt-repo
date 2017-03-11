#### Output
- **Using**: GitHub
- **Deliver**: a Pull Request showing two Design Patterns (suggestions: Decorator, Factory, Observer, Prototype...)
- **With**: *independently*

#### Design Patterns Used

#### MVC
MVC is an achitectural pattern that is used to separate an application's concerns. That is, application code is broken into three layers:
- *Model* - represents an object carrying data. e.g. `InvertedIndex Class`
- *View* - represents the front end view of the data that model contains. e.g. `index.html`
- *Controller* - acts on both model and view. It controls the data flow into model object and updates the view whenever data changes. e.g. `eventManager.js`

Hence as explained above, in the case of the Inverted Index App, the model is the `InvertedIndex Class`, the view is the front end HTML and CSS, while the controller is the JavaScript app and the associated `eventManager.js`.

#### Constructor Pattern
A constructor is a special method used to initialize a newly created object once memory has been allocated for it. 

The `InvertedIndex Class` makes explicit use of the constructor design pattern in that, to create an instance of the class, a constructor function must be called which initializes the `indexes` object that holds a hashmap of all the indexes create from the uploaded files.

```javascript
class InvertedIndex {
  
  constructor() {
    this.indexes = {};
  }

  createIndex(filename, filedata) {

  }

  searchIndex(query, filename) {

  }

```
An we can create a new instance of `InvertedIndex` by calling the constructor thus:
```javascript
const invertedIndex = new InvertedIndex();

invertedIndex.createIndex(object, fileName);

invertedIndex.searchFiles(queryString, filterName);
```