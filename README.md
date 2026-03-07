# ALICE-Neural SaaS

BCI neural signal compression and intent extraction API

## License

AGPL-3.0

## Architecture

```
Frontend :3000  -->  API Gateway :8080  -->  Core Engine :8081
```

| Layer | Port | Technology |
|-------|------|-----------|
| Frontend | 3000 | Next.js 14, Tailwind CSS |
| API Gateway | 8080 | Rust, Axum |
| Core Engine | 8081 | Rust, Axum, ALICE-Neural |

## Endpoints

| Method | Path | Description |
|--------|------|-------------|
| `POST /api/v1/compress` | 神経信号圧縮 |
| `POST /api/v1/extract` | 意図抽出 |
| `GET  /api/v1/models` | 対応モデル一覧 |
| `GET`  | `/health` | ヘルスチェック |

## Quick Start

```bash
cd services/core-engine
cargo run --release
curl http://localhost:8081/health
```

## Author

Moroya Sakamoto
