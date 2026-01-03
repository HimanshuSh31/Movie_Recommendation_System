# Movie Recommendation System

A content-based movie recommendation system that suggests similar movies based on genres, keywords, cast, director, and tagline using machine learning techniques.

## Overview

This project implements a content-based filtering approach to recommend movies similar to a user's favorite film. The system analyzes movie features and uses TF-IDF vectorization with cosine similarity to find the most relevant recommendations.

## Features

- **Content-Based Filtering**: Recommends movies based on similarity in genres, keywords, cast, director, and tagline
- **Fuzzy Matching**: Handles typos and variations in movie name input
- **Fast Recommendations**: Uses pre-computed similarity matrix for instant results
- **4,803 Movies**: Comprehensive dataset with detailed movie information

## Dataset

The project uses a movie dataset with 4,803 films containing:
- **Basic Information**: Title, budget, revenue, runtime, popularity
- **Content Features**: Genres, keywords, tagline, cast, director
- **Metadata**: Release date, vote average, vote count, and more

## Technical Implementation

### Libraries Used

- **NumPy** - Numerical computations
- **Pandas** - Data manipulation and analysis
- **Scikit-learn** - Machine learning algorithms
  - TfidfVectorizer - Text to numerical feature conversion
  - cosine_similarity - Similarity calculation
- **difflib** - Fuzzy string matching

### Algorithm

1. **Feature Selection**: Extract genres, keywords, tagline, cast, and director
2. **Data Processing**: Combine features into a single text representation
3. **Vectorization**: Convert text to numerical vectors using TF-IDF
4. **Similarity Calculation**: Compute cosine similarity between all movie pairs
5. **Recommendation**: Return top similar movies based on similarity scores

## Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/Movie_Recommendation_System.git
cd Movie_Recommendation_System
```

2. Install required packages:
```bash
pip install -r requirements.txt
```

## Usage

1. Open the Jupyter notebook:
```bash
jupyter notebook "Movie Recommendation Project.ipynb"
```

2. Run all cells to load the data and compute similarities

3. Enter your favorite movie name when prompted:
```python
Enter your favourite movie name: Avengers
```

4. The system will return similar movie recommendations

## How It Works

**Example**: When you search for "Avengers"
1. System matches to "The Avengers" using fuzzy matching
2. Retrieves pre-computed similarity scores
3. Returns movies with highest similarity:
   - Avengers: Age of Ultron (78.6% similarity)
   - Captain America: Civil War (40.5% similarity)
   - Iron Man 3 (21.5% similarity)
   - And more...

## Project Structure

```
Movie_Recommendation_System/
├── Movie Recommendation Project.ipynb   # Main implementation notebook
├── Movie Recommendation Project.html    # Notebook export
├── movies.csv                           # Movie dataset (23.4 MB)
├── 06-July-Movie.csv                   # Similarity matrix (349 MB) - Not included in repo
├── requirements.txt                     # Python dependencies
└── README.md                           # Project documentation
```

## Note on Large Files

The similarity matrix file (`06-July-Movie.csv` - 349 MB) is excluded from the repository due to GitHub's file size limits. You can regenerate it by running the notebook, which will compute and save the similarity matrix.

## Results

The recommendation system successfully identifies similar movies by analyzing:
- **Genre overlap** (Action, Sci-Fi, Adventure, etc.)
- **Keyword similarity** (superheroes, alien invasion, etc.)
- **Cast connections** (actors appearing in similar films)
- **Director style** (filmmakers with similar work)

## Future Enhancements

- Add collaborative filtering for user-based recommendations
- Implement a web interface using Flask/Streamlit
- Include movie posters and additional metadata
- Add filtering by year, rating, or language
- Integrate with movie APIs for real-time data

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is open source and available under the MIT License.

## Author

**Himanshu Sharma**
- LinkedIn: [Himanshu Sharma](https://www.linkedin.com/in/himanshush31/)

## Acknowledgments

- Inspired by content-based recommendation systems

