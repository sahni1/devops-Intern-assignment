FROM ghcr.io/astral-sh/uv:python3.10-bookworm


WORKDIR /app


COPY . .


RUN uv sync --dev


EXPOSE 8002


CMD ["uv", "run", "app.py"]
