📚 #Media Library 

📝 ##Project Overview

This project implements a basic media library using JavaScript classes and inheritance. It allows users to manage books and movies, including checking items in and out, and adding/viewing ratings. 
The project focuses on demonstrating object-oriented principles such as inheritance, encapsulation, and polymorphism.

🚀 ##Features

- **Media Base Class**: A parent class `Media` that includes common properties for media items (e.g., title, checked-out status, ratings).
- **Book and Movie Classes**: Child classes `Book` and `Movie` inherit from `Media` and add specific attributes (e.g., author for books and director for movies).
- **Check Out Status**: Users can toggle the checked-out status of books and movies.
- **Ratings**: Users can add ratings to media items and calculate the average rating.

🛠️ ##Technologies Used

- **JavaScript (ES6)**: Leverages classes, inheritance, and array methods.
- **Object-Oriented Programming (OOP)**: Demonstrates principles like encapsulation and inheritance.

🏛️ ##Classes Overview

###1. Media (Parent Class)
The `Media` class contains shared properties and methods used by all types of media (Books, Movies).

####Properties:
- `_title`: Title of the media.
- `_isCheckedOut`: Boolean representing whether the media is checked out (initially set to `false`).
- `_ratings`: An array to store user ratings (initially empty).

####Methods:
- `toggleCheckOutStatus()`: Toggles the `_isCheckedOut` status.
- `getAverageRating()`: Returns the average rating based on the `_ratings` array.
- `addRating()`: Adds a rating to the media.

📖 ###2. Book (Subclass)
The `Book` class extends `Media` and includes properties specific to books.

####Properties:
- `_author`: The author of the book.
- `_pages`: The number of pages in the book.

####Methods: Inherits all methods from the `Media` class.

🎬  ###3. Movie (Subclass)
The `Movie` class extends `Media` and includes properties specific to movies.

####Properties:
- `_director`: The director of the movie.
- `_runTime`: The duration of the movie in minutes.

####Methods: Inherits all methods from the `Media` class.

💻 ##Example Usage

```javascript
const historyOfEverything = new Book('Bill Bryson', 'A Short History of Nearly Everything', 544);

// Toggle check-out status and log
historyOfEverything.toggleCheckOutStatus();
console.log(historyOfEverything.isCheckedOut); // true

// Add ratings and log average rating
historyOfEverything.addRating(4);
historyOfEverything.addRating(5);
historyOfEverything.addRating(5);
console.log(historyOfEverything.getAverageRating()); // 4.67

const speed = new Movie('Jan de Bont', 'Speed', 116);

// Toggle check-out status and log
speed.toggleCheckOutStatus();
console.log(speed.isCheckedOut); // true

// Add ratings and log average rating
speed.addRating(1);
speed.addRating(1);
speed.addRating(5);
console.log(speed.getAverageRating()); // 2.33
```

🔮 ##Future Improvements
- Add additional media types like **CD** or **Podcast** to extend the `Media` class with relevant properties.
- Implement a more advanced UI for users to interact with the media library.
- Add persistence through a database or local storage to save media data across sessions.

📜 ##License
This project is part of the Codecademy **Learn Intermediate JavaScript** course.

