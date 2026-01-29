FROM python:3.12.12-alipine@sha256:880de52dca7182fc9ecefaf43436abcaa8a5ea9a9a91cd6d2c238ce40223b6ae

WORKDIR /app
COPY . /app/

RUN pip install -r requirements.txt

# Create non-root user
RUN useradd -m appuser && chown -R appuser:appuser /app
USER appuser

EXPOSE 8000

# Add health check
HEALTHCHECK --interval=30s --timeout=5s --start-period=5s \
  CMD curl -f http://localhost:8000/health || exit 1

CMD ["uvicorn", "app.main:app", "--host", "0.0.0.0", "--port", "8000"]
