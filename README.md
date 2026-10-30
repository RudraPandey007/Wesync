# WeSync

The frontend is connected to the FastAPI backend. Authentication, profile loading, interest selection, matching, connection requests, and persistent chat use the API. All accounts in this WeSync installation share one community, regardless of college name or email domain. Matches are based on shared interests.

## Run locally

Start the backend in one terminal:

```sh
cd backend
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
uvicorn main:app --reload --host 127.0.0.1 --port 8000
```

Start the frontend in a second terminal:

```sh
cd frontend
python3 -m http.server 5173 --bind 127.0.0.1
```

Open `http://127.0.0.1:5173`. Create accounts with any valid email address and choose at least three interests. All users registered in this installation can discover one another when they share an interest. The SQLite database stores accounts, profiles, interests, connection requests, and messages.
