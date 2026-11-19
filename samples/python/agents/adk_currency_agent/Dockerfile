FROM python:3.12-slim

WORKDIR /app

COPY . .

RUN pip install --no-cache-dir uv && \
    uv sync --frozen --no-dev

ENV PATH="/app/.venv/bin:$PATH"

CMD ["sh", "-c", "currency_agent --host 0.0.0.0 --port ${PORT:-8080}"]
