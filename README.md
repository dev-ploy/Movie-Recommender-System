# Movie Recommender System

A web-based movie recommender app built with Streamlit. Enter a movie name and get five similar movie recommendations, each with its poster fetched from TMDB.

## Features
- Select a movie from a dropdown list
- Get five recommended movies based on similarity
- See posters for each recommended movie
- Powered by precomputed similarity matrix and TMDB API

## Demo
[View the deployed app here](http://movie-recom.duckdns.org:8501)

## Getting Started

### Requirements
- Python 3.12+
- `streamlit`, `pandas`, `requests`, `pickle`
- `movies_dict.pkl` and `similarity1.pkl` files in the project directory

### Local Run
1. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
2. Start the app:
   ```bash
   streamlit run app.py
   ```
3. Open your browser at `http://localhost:8501`

### Deployment
- See the [Procfile](Procfile) for Heroku deployment.
- For AWS EC2, run with:
   ```bash
   streamlit run app.py --server.address=0.0.0.0 --server.port=8501
   ```
- For public access, point your domain or DuckDNS subdomain to your EC2 public IP.

## How It Works
- Loads movie data and similarity matrix from pickle files
- Uses TMDB API to fetch movie posters
- Displays recommendations and posters in a Streamlit web UI

## Project Structure
- `app.py` — main Streamlit app
- `movies_dict.pkl` — movie data
- `similarity1.pkl` — similarity matrix
- `Procfile` — for Heroku deployment

## License
MIT


