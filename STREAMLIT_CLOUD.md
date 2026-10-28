# Streamlit Community Cloud

Upstream: `bentoML-processamento-imagens@71c01015c49d65a50b04aaa2d256d5a62e7118b6` (lesson 008).

## Deploy

1. Push this repository to GitHub (public).
2. Open https://share.streamlit.io → **New app**.
3. Main file path: `app.py`
4. Python: 3.13 (or closest supported; see `requires-python` in upstream).

## Refresh from monorepo

```bash
cd /path/to/bentoML-processamento-imagens
python scripts/export_streamlit_cloud.py 008 --out /home/lugatj/code/research/streamlit-psi-drift-alert
cd /home/lugatj/code/research/streamlit-psi-drift-alert
git add -A && git commit -m "sync from monorepo" && git push
```

Runtime does **not** call `git rev-parse`. Samples are vendored under `samples/`.
BentoML is omitted from `requirements.txt` (offline Streamlit path only).
