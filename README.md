# Build an ANIME Search Database in React JS with Jikan Anime API

![11](https://user-images.githubusercontent.com/108209653/175992388-8e51bb23-5f03-4a03-847b-a05dc2ad5a4f.png)

In this project, we will learn how to build an anime search database using the Jikan Anime API and React JS but more specifically, react hooks. We look into forms, fetching data, components and looping through arrays to display cards. We also utilize SCSS as our preprocessor.

Project Demo
[https://the-anime-database-notsodevv.vercel.app/](https://the-anime-database-notsodevv.vercel.app/)

## Create React App

Create React App is a comfortable environment for learning React, and is the best way to start building a new single-page application in React.

It sets up your development environment so that you can use the latest JavaScript features, provides a nice developer experience, and optimizes your app for production. You’ll need to have Node >= 14.0.0 and npm >= 5.6 on your machine. To create a project, run:

```bash
npx create-react-app my-app
cd my-app
npm start
```
Create React App doesn’t handle backend logic or databases; it just creates a frontend build pipeline, so you can use it with any backend you want. Under the hood, it uses Babel and webpack, but you don’t need to know anything about them.

When you’re ready to deploy to production, running npm run build will create an optimized build of your app in the build folder. You can learn more about Create React App from its README and the User Guide.

[https://reactjs.org/docs/create-a-new-react-app.html](https://reactjs.org/docs/create-a-new-react-app.html)

## Project Structure
![175810661-8c1312b3-b08c-43ea-a2b0-39ca0d0bb781](https://user-images.githubusercontent.com/108209653/175812348-3e6f3e15-6759-49db-be8d-3361ea8c5c26.png)

Our main code lies in the src folder lets go and explore it.
![175811188-7b0c90de-6101-4cf1-a6a0-033464fa4ec4](https://user-images.githubusercontent.com/108209653/175812391-3ef8efbe-ec38-4565-987e-b079b693ea13.png)

## Fetching API Path and Version

We will fetch our API Path and Version from the following link:

[https://jikan.docs.apiary.io/](https://jikan.docs.apiary.io/)

We will use the API to fetch the Anime by using Fetch with async/await:

![image](https://user-images.githubusercontent.com/108209653/175811745-b437f5bc-1100-4fbd-8a2b-6898632ab0f0.png)


## How to Use Fetch with async/await

The Fetch API accesses resources across the network. You can make HTTP requests (using GET, POST and other methods), download, and upload files.

To start a request, call the special function fetch():
```bash
const response = await fetch(resource[, options]);
```
which accepts 2 arguments:

*1. resource: the URL string, or a Request object*

*2. options: the configuration object with properties like method, headers, body, credentials, and more.*

fetch() starts a request and returns a promise. When the request completes, the promise is resolved with the Response object. If the request fails due to some network problems, the promise is rejected.

async/await syntax fits great with fetch() because it simplifies the work with promises.

For example, let's make a request to fetch some movies:
```bash
async function fetchMovies() {
  const response = await fetch('/movies');
  // waits until the request completes...
  console.log(response);
}
```



fetchMovies() is an asynchronous function since it's marked with the async keyword.

await fetch('/movies') starts an HTTP request to '/movies' URL. Because the await keyword is present, the asynchronous function is paused until the request completes.

When the request completes, response is assigned with the response object of the request. Let's see in the next section how to extract useful data, like JSON or plain text, from the response.




## Visit this link to know more:
1. Intro to fetch()  
2. Fetching JSON
3. Handling fetch errors
4. Canceling a fetch request
5. Parallel fetch requests
6. Summary

[https://dmitripavlutin.com/javascript-fetch-async-await/](https://dmitripavlutin.com/javascript-fetch-async-await/)


## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.

