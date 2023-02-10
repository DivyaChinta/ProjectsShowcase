The goal of this coding exam is to quickly get you off the ground with **setState Callback Function**.

### Refer to the video and image below:

<div style="text-align: center;">
    <video style="max-width:70%;box-shadow:0 2.8px 2.2px rgba(0, 0, 0, 0.12);outline:none;" loop="true" autoplay="autoplay" controls="controls" muted>
    <source src="https://assets.ccbp.in/frontend/content/react-js/projects-showcase-success-output.mp4" type="video/mp4">
  </video>
</div>

<br/>

**Failure View**

<div style="text-align: center;">
    <img src="https://assets.ccbp.in/frontend/content/react-js/projects-showcase-failure-output.gif" alt="failure view" style="max-width:70%;box-shadow:0 2.8px 2.2px rgba(0, 0, 0, 0.12)">
</div>

<br/>

### Design Files

<details>

<summary>Click to view</summary>

- [Medium (Size >= 768px), Large (Size >= 992px) and Extra Large (Size >= 1200px) - Success](https://assets.ccbp.in/frontend/content/react-js/projects-showcase-success-lg-output.png)
- [Medium (Size >= 768px), Large (Size >= 992px) and Extra Large (Size >= 1200px) - Failure](https://assets.ccbp.in/frontend/content/react-js/projects-showcase-failure-lg-output.png)

</details>

### Set Up Instructions

<details>

<summary>Click to view</summary>

- Download dependencies by running `npm install`
- Start up the app using `npm start`

</details>

### Completion Instructions

<details>

<summary>Functionality to be added</summary>

<br/>

The app must have the following functionalities

- When the app is opened initially,

  - An HTTP GET request should be made to **projectsApiUrl** with query parameter as `category` and its initial value as `ALL`
  - The **_loader_** should be displayed while fetching the data
  - After the data is fetched successfully, display the projects list received in the API response

- When a category option is selected,

  - An HTTP GET request should be made to the **projectsApiUrl** with the query parameter as `category` and its value as the `id` of the active category option
  - The **_loader_** should be displayed while fetching the data
  - After the data is fetched successfully, display the projects list received in the API response

- The `App` component is provided with `categoriesList`. It consists of a list of category objects with the following properties in each category object

  |     Key     | Data Type |
  | :---------: | :-------: |
  |     id      |  String   |
  | displayText |  String   |

</details>

<details>

<summary>API Requests & Responses</summary>

<br/>

**projectsApiUrl**

#### API: `https://apis.ccbp.in/ps/projects`

#### Example: `https://apis.ccbp.in/ps/projects?category=ALL`

#### Method: `GET`

#### Description:

Returns a response containing the list of all projects

#### Response:

```json
{
  "projects": [
      {
        "id": "f680c5fb-a4d0-4f43-b356-785d920208df",
        "name": "Music Page",
        "image_url": "https://assets.ccbp.in/frontend/react-js/projects-showcase/music-page-img.png"
      },
       ...
  ],
  "total": 34
}
```

</details>

### Important Note

<details>

<summary>Click to view</summary>

<br/>

**The following instructions are required for the tests to pass**

- Each category option in the HTML `select` element should have the value attribute as the value of key `id` and text content as the value of the key `displayText` from the `categoriesList` provided
- Wrap the `Loader` component with an HTML container element and add the `data-testid` attribute value as **loader** to it
- The project image in each project item should have the alt as the value of the key `name` from each project object in the projects API response

</details>

### Resources

<details>

<summary>Image URLs</summary>

- https://assets.ccbp.in/frontend/react-js/projects-showcase/website-logo-img.png alt should be **website logo**
- https://assets.ccbp.in/frontend/react-js/projects-showcase/failure-img.png alt should be **failure view**

</details>

<details>

<summary>Colors</summary>

<br/>

<div style="background-color:#f1f5f9; width: 150px; padding: 10px; color: black">Hex: #f1f5f9</div>
<div style="background-color:#cbd5e1; width: 150px; padding: 10px; color: black">Hex: #cbd5e1</div>
<div style="background-color:#475569; width: 150px; padding: 10px; color: white">Hex: #475569</div>
<div style="background-color:#ffffff; width: 150px; padding: 10px; color: black">Hex: #ffffff</div>
<div style="background-color:#328af2; width: 150px; padding: 10px; color: white">Hex: #328af2</div>
<div style="background-color:#e2e8f0; width: 150px; padding: 10px; color: black">Hex: #e2e8f0</div>
<div style="background-color:#e6e9ec; width: 150px; padding: 10px; color: black">Hex: #e6e9ec</div>

</details>

<details>

<summary>Font-families</summary>

- Roboto

</details>

> ### _Things to Keep in Mind_
>
> - All components you implement should go in the `src/components` directory.
> - Don't change the component folder names as those are the files being imported into the tests.
