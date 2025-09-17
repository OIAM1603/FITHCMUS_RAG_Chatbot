# **Chatbot RAG – Hỏi đáp về Chương trình đào tạo FITHCMUS (Chương trình Chuẩn)**

## **Giới thiệu**

Dự án xây dựng một **chatbot dựa trên Retrieval-Augmented Generation (RAG)**, giúp sinh viên và giảng viên **tra cứu nhanh, chính xác** các thông tin về **chương trình đào tạo ngành Công nghệ Thông tin** (chương trình Chuẩn) tại **Trường Đại học Khoa học Tự nhiên – ĐHQG.HCM**.

---

## **Demo**

* **Video demo:** https://youtu.be/O_b75FD5jB4
* **Giao diện chính:**

  * Trang chủ, hỏi đáp, FAQ, và gửi phản hồi.

---

## **Mục tiêu**

* Hỗ trợ **tìm kiếm thông tin nhanh chóng** về ngành, chuyên ngành, tín chỉ, và mô tả môn học.
* Cung cấp **câu trả lời tự nhiên, dễ hiểu** từ tài liệu chính thức của khoa.

**Ví dụ:**

* Input: `Tôi cần tích lũy bao nhiêu tín chỉ bắt buộc chuyên ngành Công nghệ tri thức?`
* Output: `Bạn cần tích lũy tối thiểu 16 tín chỉ cho các học phần bắt buộc chuyên ngành Công nghệ tri thức.`

---

## **Cấu trúc dự án**

```
├── backend/            # API và pipeline RAG
├── frontend/           # Giao diện web (React + Vite)
├── data/               # Dữ liệu gốc và dữ liệu sau khi tiền xử lý
└── README.md           # Tài liệu dự án
```

---

## **Công nghệ sử dụng**

* **Back-end:** Python, LangChain, FastAPI
* **Front-end:** React (Vite)
* **Vector Database:** Qdrant
* **Mô hình:**

  * **Embedding:** `multilingual-e5-base`
  * **LLM generate:** `gemini-1.5-flash`
* **Môi trường:** Google Colab, VS Code

---

## **Cài đặt và chạy**

### **1. Chạy backend**

```bash
cd backend
pip install -r requirements.txt
python app.py
```

### **2. Chạy frontend**

```bash
cd frontend
npm install
npm run dev
```

* Truy cập: [http://localhost:5173](http://localhost:5173)

---

## **Kết quả nổi bật**

* **Retrieval:** Precision\@5 đạt **84%**, nDCG\@5 đạt **87%**.
* **Generation (gemini-1.5-flash):**

  * BLEU: **0.60**
  * ROUGE-L: **0.82**
  * SBERT Similarity: **0.88**
* **Tính chính xác ngữ cảnh:** 92.7%
* **Faithfulness (độ trung thực):** 91.4%

---

## 🔮 **Hướng phát triển**

* Mở rộng dữ liệu đào tạo nhiều khóa.
* Tối ưu prompt và thuật toán tìm kiếm.
* Cải thiện tốc độ phản hồi và khả năng chịu tải.
