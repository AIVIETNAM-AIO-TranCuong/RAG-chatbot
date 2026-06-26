# PDF RAG Chatbot

Ứng dụng Streamlit này cho phép upload file PDF, tạo embedding bằng `ollama`, lưu vào `chromadb`, và trả lời câu hỏi dựa trên nội dung PDF.

## Yêu cầu

- Python 3.11+ (hoặc Python tương thích với các thư viện)
- Streamlit
- pypdf
- chromadb
- ollama

## Cài đặt bằng Anaconda

1. Mở Anaconda Prompt.
2. Kích hoạt môi trường conda của bạn (ví dụ):

```powershell
conda activate project-1.2
```

3. Cài các thư viện cần thiết:

```powershell
python -m pip install streamlit pypdf chromadb ollama
```

## Chạy ứng dụng

```powershell
streamlit run app.py
```

## Sử dụng

1. Mở trang web Streamlit theo URL được in ra khi chạy.
2. Upload file PDF.
3. Nhấn `Xử lý PDF`.
4. Nhập câu hỏi vào ô chat.

## Lưu ý

- Ứng dụng yêu cầu kết nối đến model `vicuna: 7b-v1.5-q5_1` thông qua `ollama`.

### Promt:

Sử dụng promt sau để tương tác với trợ lý.

- PROMPT = """Bạn là trợ lý hỏi đáp. Dùng các đoạn ngữ cảnh dưới đây để trả lời câu hỏi. Nếu ngữ cảnh không có thông tin, hãy nói là bạn không biết, đừng bịa. Trả lời ngắn gọn, chính xác, bằng tiếng Việt.
Ngữ cảnh: {context}
Câu hỏi: {question}
"""

