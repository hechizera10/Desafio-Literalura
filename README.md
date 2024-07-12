
# Introduction
This is the challenge of Alura Oracle Next Education, the purpose is to practise and use the Gutendex API to save to our database in MySQL using Spring Data


## Quickstart
[List fixes or bugs](#list-of-fixes-or-bugs)

[Folder Structure](#folder-structure)

[Technologies](#technologies)

[Demo images](#demo)

## List of fixes or bugs
### Hotfixes:
<b>HotFix v1.01 (11 June 2024):</b>

- Fixed showing language as a code, now showing full language title
  - Ex. When getting the book from Gutendex it was showing Idioma with code language: 'en', 'es', 'fr'.
  - Updated using getFullLanguageName(languageCode) static method to convert the language code to the full language  title in spanish.  
- Fixed when retrieving Books, Authors, or Top Books, there was an empty repose. Forgot to write the else to send a message there were no elements in our database.

<b>HotFix v1.01b (13 June 2024):</b>
- Fixed when a book was already registered, the language was shown as code but language that language is not defined in our program, so we filter as N/A.
- Fixed when an author birth and death year was shown as null, we fixed with custom message.
- Fixed retreiving books writed by author


### Limited:
First Release V1.00:
- As mainly the majority books are written in English, Spanish or French. The application is limited for these three languages but no worries if the book is written in another language it will show as N/A.
## Folder Structure
```

src
│
├── entities ───────── Entities for our database
│
├── menu ───────────── Main menu of the application, a menu list messages and a validator
│
├── models ─────────── Models for API
│    │
│    └── dto ───────── Filter to send the data from dto not entities.
│
├── repository ─────── Applying Spring Data JPA to make the queries.
│
└── service ────────── All our persistence logics and api consumption.

```

## Technologies
- Java

- Spring Boot

- Spring Data JPA

- Hibernate ORM

- MySQL

- Gutendex API

