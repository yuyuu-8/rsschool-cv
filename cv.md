# Anastasiya Stepuk
![My photo.](/225.jpg)

## Contact Information
- **_Address_**: Belarus, Minsk city
- **_Phone_**: +375-29-174-48-73
- **_Email_**: nastyastepuk05@gmail.com
- **_Telegram_**: [@yuyuu_8](https://t.me/yuyuu_8)
- **_GitHub_**: [yuyuu-8](https://github.com/yuyuu-8)

## Self Introduction
_I'm a beginner Frontend Developer with some expirience in Backend Development and Design. Driven by a passion for elegant design solutions and a commitment to continuous improvement, I seek a role that fosters creativity and professional growth. I aim to bring clarity and innovation to every project. In the process of work I learn quickly and have a great desire for professional growth._

## Skills
-  **_Stack:_** JavaScript, HTML5+, CSS3, LaTeX, C++, GO.
-  **_Software:_** VS Code, Visual Studio, Sublime, Codeblocks, RAD Studio, Wordpress, Figma, Adobe Photoshop, Adobe Illustrator.
-  **_Version control systems:_** Git, GitHub, GitLab.
-  **_Frameworks:_** React JS.

## Code Examples
```
import MovieCard from "../components/MovieCard";
import { useState, useEffect } from "react";
import { searchMovies, getPopularMovies } from "../services/api";
import "../css/Home.css";

function Home() {
  const [searchQuery, setSearchQuery] = useState("");
  const [movies, setMovies] = useState([]);
  const [error, setError] = useState(null);
  const [loading, setLoading] = useState(true);

  useEffect(() => {
    const loadPopularMovies = async () => {
      try {
        const popularMovies = await getPopularMovies();
        setMovies(popularMovies);
      } catch (err) {
        console.log(err);
        setError("Failed to load movies");
      } finally {
        setLoading(false);
      }
    };

    loadPopularMovies();
  }, []);

  const handleSearch = (e) => {
    e.preventDefault();
    alert(searchQuery);
    setSearchQuery("");
  };

  return (
    <div className="home">
      <form onSubmit={handleSearch} className="search-form">
        <input
          type="text"
          placeholder="Search for movie..."
          className="search-input"
          value={searchQuery}
          onChange={(e) => setSearchQuery(e.target.value)}
        />
        <button type="submit" className="search-button">
          Search
        </button>
      </form>

      <div className="movies-grid">
        {movies.map((movie) => (
          <MovieCard movie={movie} key={movie.id} />
        ))}
      </div>
    </div>
  );
}

export default Home;
```

## Work Experience
### **_Projects_**
1. _Movie Search Engine - [link](https://yuyuu-8.github.io/movie-search)_
   - A simple movie search engine built with React and Vite. The movies are loaded using [API](https://www.themoviedb.org)
2. _Wordpress site - [link](http://taxi7812.by/)_
  - In 3 weeks created and published Wordpress powered site from scratch without experience in platform. Covered all the work with databases, hosting and domain name. Later covered the work with creating ads using Yandex Direct, analyzed data and improved the adds to get more clients.

## Education
- **_Higher Education_**
  - _Belarusian State University: Applied Computer Science, 2023-2027, GPA 8.0/10.0_
- **_Additional Courses_**
  - _"Version Control with Git" at Epam_
  - _"Introduction to Programming (C++)" at Yandex Academy_
  - _"Frontend/JavaScript" at RS School_

## Languages
- **_English:_** Upper-Intermidiate
- **_Belarusian:_** Native
- **_Russian:_** Native
- **_Chinese:_** Intermidiate+
