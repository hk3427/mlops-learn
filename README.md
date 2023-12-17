# How to Run :

1. python3 -m venv venv

2. source venv/bin/activate

3. python3 -m pip install pip setuptools wheel

4. python3 -m pip install -e .

5. uvicorn app.api:app --host 0.0.0.0 --port 8000 --reload --reload-dir tagifai --reload-dir app  # dev

6. gunicorn -c app/gunicorn.py -k uvicorn.workers.UvicornWorker app.api:app  # prod


