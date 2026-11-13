Hệ thống đếm Token của AI **không hề bị lỗi hay đếm trùng**. Nguyên nhân do thuật toán **BPE (Byte-Pair Encoding)**:

-   LLM chia nhỏ từ theo sub-word.
    
-   Tiếng Việt có dấu và ít xuất hiện trong dữ liệu huấn luyện nên bị BPE cắt thành nhiều mảnh byte nhỏ, khiến Mẫu B tốn nhiều token hơn Mẫu A.
    

**2 cách tối ưu prompt tiếng Việt:**

1.  **Lược bỏ hư từ:** Cắt bỏ các từ nối, trợ từ không cần thiết (như _của, các loại, những..._).
    
2.  **Dùng thuật ngữ tiếng Anh:** Giữ nguyên các thuật ngữ chuyên ngành ngắn gọn (như _ROI, conversion rate_) để giảm số lượng token bị cắt nhỏ.
