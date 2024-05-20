# DS-Project

<a name="readme-top"></a>
<br />
<div align="center">
  <p align="center">
    Travel Guide Project made for the OOP course at Faculty of Computer and Information Science, Ain Shams University.
    <br />
    <br />
    <br />
    <br />
  </p>
</div>

<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
    </li>
    <li>
      <a href="#system-description">System Description</a>
      <ul>
        <li><a href="#classes-and-methods">Classes and Methods</a></li>
      </ul>
    </li>
    <li><a href="#usage">Usage</a></li>
    <li><a href="#extra-documentation-and-studies">Extra Documentation and Studies</a></li>
    <li><a href="#contributing">Contributing</a></li>
    <li><a href="#license">License</a></li>
  </ol>
</details>

# About The Project

![Splash Screen](https://github.com/ELDA7EE7/OOP-project-2.0/assets/114913488/86c677a2-2aae-4df3-a6e2-2931f28fd2c9)

This comprehensive and feature-rich system is designed to streamline the process of planning travel routes between countries, offering both users and administrators an intuitive and efficient platform. With functionalities ranging from adding and deleting countries and travel paths to searching for paths between countries with specific constraints, this system aims to provide a seamless experience for both travelers and administrators.

### Built With

* [![C++][C++.js]][C++-url]
* [![Qt][Qt.js]][Qt-url]

<p align="right"><a href="#readme-top">back to top</a></p>

# System Description

### Classes and Methods

#### Travel Method
- **Public Arguments:**
  - `String Name`: Name of Transportation
  - `int Cost`: Cost of Transportation
- **Constructors:**
  - Default Constructor
  - Parameterized Constructor

#### Graph
- **Private Arguments:**
  - `unordered_map<string, set<pair<TravelMethod, string>>> Graph`: To save Graph
- **Private Methods:**
  - `Write()`: Writes the graph data to a file
  - `Read()`: Reads the graph data from a file
- **Public Void Methods:**
  - `Add Path(String country1, String country2, String methodName, int cost)`: Adds a new path from `country1` to `country2`
  - `Update Path(String country1, String country2, String methodName, String newMethodName, int newCost)`: Updates the path between `country1` and `country2`
  - `Delete Path(String country1, String country2, String methodName)`: Deletes the path between `country1` and `country2`
  - `Add Country(String country)`: Adds a new country to the graph
  - `Delete Country(String country)`: Deletes a country from the graph
- **Public Bool Method:**
  - `Is Complete()`: Returns `true` when the graph is complete
- **Public List<String> Methods:**
  - `All Countries()`: Returns all countries in the graph
  - `BFS(String StartNode, unordered_map<string, bool> visited)`: Traverses the graph using the BFS algorithm
  - `DFS(String StartNode, unordered_map<string, bool> visited)`: Traverses the graph using the DFS algorithm
- **Public Method to Get Paths:**
  - `set<pair<long, list<pair<TravelMethod, string>>>> Get Paths(String country1, String country2, Long Cost, unordered_map<string, bool> visited)`: Returns all paths between `country1` and `country2` that don’t exceed the maximum cost, sorted by cost

<p align="right"><a href="#readme-top">back to top</a></p>

# Usage

## Input and Output Scenarios:

### Get Paths
* **Input:** User enters `Country 1` and `Country 2`
* **Output:** Displays all paths between the entered countries within the maximum cost

### Graph Info
* **Output:** Displays all countries in the graph

### Traverse
* **Input:** User enters `Country 1` and `Country 2`
* **Output:** Displays all paths between the entered countries, sorted by nearest first or farthest first from `Country 1`

### Options:
1. **Add Path**
   * **Input:** User enters `Country 1`, `Country 2`, `Cost`, and `Transportation Method`
   * **Output:** Adds a new path between the entered countries
2. **Delete Path**
   * **Input:** User enters `Country 1`, `Country 2`, and `Transportation Method`
   * **Output:** Deletes the path between the entered countries
3. **Update Path**
   * **Input:** User enters `Country 1`, `Country 2`, `Old Transportation Method`, `New Transportation Method`, and `New Cost`
   * **Output:** Updates the path between the entered countries
4. **Add Country**
   * **Input:** User enters the `Country` name
   * **Output:** Adds a new country to the graph
5. **Delete Country**
   * **Input:** User enters the `Country` name
   * **Output:** Deletes the country from the graph

<p align="right"><a href="#readme-top">back to top</a></p>

# Extra Documentation and Studies

### [UML Diagram](https://drive.google.com/file/d/15DKX1cpXYcr4WeUYd-v6bjtgYUV0-6Rs/view?usp=sharing)
### [Brand Guidelines](https://www.behance.net/gallery/187621769/ByteBibliotheca-Brand-Guidelines)
### [UI / UX Case Study](https://www.behance.net/gallery/187613467/ByteBibliotheca-UI-UX-Case-Study)

<p align="right"><a href="#readme-top">back to top</a></p>

# Contributing

Contributions are what make the open source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

If you have a suggestion that would make this better, please fork the repo and create a pull request. You can also simply open an issue with the tag "enhancement".
Don't forget to give the project a star! Thanks again!

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

<p align="right"><a href="#readme-top">back to top</a></p>

# License

MIT License

Copyright (c) [2023] [ByteBibliotheca]

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

<p align="right"><a href="#readme-top">back to top</a></p>

<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[C++.js]: https://img.shields.io/badge/C++-00599C?style=for-the-badge&logo=c%2B%2B&logoColor=white
[C++-url]: https://www.cplusplus.com/
[Qt.js]: https://img.shields.io/badge/Qt-41CD52?style=for-the-badge&logo=Qt&logoColor=white
[Qt-url]: https://www.qt.io/
