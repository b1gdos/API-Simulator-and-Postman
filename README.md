# API-Simulator-and-Postman
Lab - Explore Rest APIs with API Simulator and Postman

##################
#     Part 1     #
##################

School Library site

In this part of the labo, we are goint to work with REST APIs in the API Simulator. 

First we are going to list the books by using GET /books
*They are diferent types of parameter that we can use for have a more dip result in this task. 
*Also we are using JSON format to see the different types of date.
When we execute GET /books API we get the following result:
[
  {
    "id": 0,
    "title": "IP Routing Fundamentals",
    "author": "Mark A. Sportack"
  },
  {
    "id": 1,
    "title": "Python for Dummies",
    "author": "Stef Maruch Aahz Maruch"
  },
  {
    "id": 2,
    "title": "Linux for Networkers",
    "author": "Cisco Systems Inc."
  },
  {
    "id": 3,
    "title": "NetAcad: 20 Years Of Online-Learning",
    "author": "Cisco Systems Inc."
  },
  {
    "id": 4,
    "title": "IPv6 Fundamentals",
    "author": "Rick Graziani"
  },
  {
    "id": 5,
    "title": "31 Days Before Your CCNA Exam",
    "author": "Allan Johnson"
  }
]

-This is a list of books in the library.
We can get the same result by using curl via the terminal.
curl -X GET "http://library.demo.local/api/v1/books" -H "accept: application/json" 

We can also use custom search with curl in this case we use ?includeISBN=true:
http://library.demo.local/api/v1/books?includeISBN=true"  -H "accept: application/json" 

We use a token in the POST /loginViaBasic API that allow us to login in the  API simulator to unlock differents features. 

We add books using POST /books API, in order to complite this task we need to add a payload. 

{ 
  "id": 4, 
  "title": "IPv6 Fundamentals", 
  "author": "Rick Graziani" 
}

This way we were able to add multiple entrys in the school library.

We can also list or delete books by the {id}

##################
#     Part 2     #
##################

Use postman to make API call to the API Simulator

In this part of the labo we were able to simulate the same task but in a real application. 

When we open postman we are in an untitle request
We can make GET, POST, PUT, PATCH, DELETE, etc. calls 

If we give the URI http://library.demo.local/api/v1/books and send it we get the following information.
[
    {
        "id": 0,
        "title": "IP Routing Fundamentals",
        "author": "Mark A. Sportack"
    },
    {
        "id": 1,
        "title": "Python for Dummies",
        "author": "Stef Maruch Aahz Maruch"
    },
    {
        "id": 2,
        "title": "Linux for Networkers",
        "author": "Cisco Systems Inc."
    },
    {
        "id": 3,
        "title": "NetAcad: 20 Years Of Online-Learning",
        "author": "Cisco Systems Inc."
    },
    {
        "id": 4,
        "title": "IPv6 Fundamentals",
        "author": "Rick Graziani"
    },
    {
        "id": 5,
        "title": "31 Days Before Your CCNA Exam",
        "author": "Allan Johnson"
    }
]

We can also use a toke to use the authorization area and there we can use an username and password. 

To finish, in this task we were able to gather, add, delete information, using REST APIs. 
