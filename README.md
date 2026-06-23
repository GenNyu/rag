# RAG Project

Skeleton cho một ứng dụng Retrieval-Augmented Generation (RAG): nạp dữ liệu, chia nhỏ văn bản, tạo embeddings, lưu vào vector database, truy xuất đoạn liên quan và sinh câu trả lời bằng LLM.

## Cấu trúc thư mục

```
.
├── README.md            # Mô tả, hướng dẫn cài đặt & chạy
├── requirements.txt      # Danh sách thư viện Python
├── .env.example          # Mẫu khai báo API keys & thông tin nhạy cảm
├── config.yaml            # Cấu hình model, chunk size, vector DB
├── src/
│   ├── ingestion/         # Nạp dữ liệu (PDF, CSV, web)
│   ├── chunking/           # Chia nhỏ văn bản
│   ├── embeddings/         # Tạo embeddings
│   ├── vectordb/            # Thao tác vector database
│   ├── retrieval/            # Truy xuất đoạn liên quan
│   ├── prompts/                # Mẫu prompt
│   ├── llm/                     # Gọi LLM
│   ├── api/                      # API endpoints
│   └── utils/                     # Hàm tiện ích
├── tests/                 # Kiểm thử
├── logs/                   # Log
└── main.py                 # Điểm khởi chạy ứng dụng
```

## Cài đặt

```bash
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
cp .env.example .env  # rồi điền API keys của bạn
```

## Chạy

```bash
python main.py
```

## Cấu hình

Các tham số về model, chunk size, vector database... được khai báo trong [`config.yaml`](config.yaml).
