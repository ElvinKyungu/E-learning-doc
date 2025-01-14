# E-learning application

<p>challenge from the club of developpers and scientific circle Math-Info</p>

#### Application e-learning :

<a href="http://club-elearning.herokuapp.com/">club-Elearning </a>

## purpose
Build an api backend application for an online learning plate-forme

## Installation
To install this application run 
```git
git clone https://github.com/jocelinkisenga/E-learning.git
```
And navigate to the application folder then run 
```git
composer install 
```
to install composer's dependances

## API DOCS (end-points)

### register end-point : /register
To register the end-point is <strong> /register </strong> , the end-point will return a bear token witch will be used for different requests.
 
#### headers :
```javascript
 	{
 		username,
 		email,
 		password
 	}
```
### login end-point : /login
To login the end-point is <strong> /login </strong> , the end-point will return a bear token witch will be used for different requests.
#### headers :
 ```javascript
 	{
 			email,
 			password
 	}
 ```
 

### all Courses end-point : /
<p> To fetch all the courses the end-point is <strong>/ </strong> whith the http method GET 
</p>

#### results:
```javascript
{
    "0": "all courses",
    "course": [
        {
            "id": 23,
            "owner_id": 5,
            "title": "kisenga1@gmail.com",
            "description": "jocelinkisenga",
            "number_chapters": null,
            "created_at": "2022-06-23T13:33:17.000000Z",
            "updated_at": "2022-06-23T13:33:17.000000Z",
            "image": "1655991197_téléchargement.jpeg"
        },
        {
            "id": 22,
            "owner_id": 3,
            "title": "kisenga1@gmail.com",
            "description": "jocelinkisenga",
            "number_chapters": null,
            "created_at": "2022-06-23T13:07:54.000000Z",
            "updated_at": "2022-06-23T13:07:54.000000Z",
            "image": "1655989674_téléchargement.jpeg"
        },
        {
            "id": 21,
            "owner_id": 4,
            "title": "python",
            "description": "learn python in one day and learn it well",
            "number_chapters": null,
            "created_at": "2022-06-23T12:56:36.000000Z",
            "updated_at": "2022-06-23T12:56:36.000000Z",
            "image": "1655988996_téléchargement.jpeg"
        }],
      }
```

### single course end-point : /course/id_course/
To get a single course, use the end point <strong> /course/id_course/ </strong> , with the GET http method
#### result:
```javascript
{
    
    "course": [
        {
            "id": 23,
            "owner_id": 5,
            "title": "kisenga1@gmail.com",
            "description": "jocelinkisenga",
            "number_chapters": null,
            "created_at": "2022-06-23T13:33:17.000000Z",
            "updated_at": "2022-06-23T13:33:17.000000Z",
            "image": "1655991197_téléchargement.jpeg"
        },
        ],
    }
```

### create course end-point : /course
  to create a course you need first to make a request and let the admin allow you.
  The end-point for creating a course is <strong> /course </strong>, with the POST http method.

#### headers
  ```javascript
  {
  	title,
  	description,
  	image
  }
  ```

  ### request permission end-point /permissions
  To request a permission get loged in first.
  The end-point to ask for permission is <strong>/permissions</strong>, with the http method POST,
  This end point helps you to create a course after it's allowed by the admin.<br>
  <i>By defaut the after asking requesting a permission , the route for adding courses will be enabled, no need for the admin to confirm it</i>


## requirements
> php v8
> laravel 9

<strong> build with love by Jocelin kisenga </strong>
