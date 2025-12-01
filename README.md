# Spotify Global Music Dataset Analysis (2009–2025)

## Thông tin nhóm

### Thành viên
| Họ và tên | MSSV |
|-----------|------|
| Phạm Phú Hòa | 23122030 |
| Trần Chí Nguyên | 23122044 |
| Nguyễn Lâm Phú Quý | 23122048 |

### Trường
**Vietnam National University, Ho Chi Minh City**  
**University of Science**  
**Faculty of Information Technology**  
**CSC17104 – Programming for Data Science**

---

## Tổng quan dự án

Dự án này phân tích dữ liệu âm nhạc toàn cầu từ Spotify, bao gồm thông tin về nghệ sĩ, bài hát, và xu hướng âm nhạc từ năm 2009 đến 2025. Mục tiêu là khám phá các mẫu hình trong sự phổ biến của nghệ sĩ, xu hướng track, và sự phát triển của âm nhạc qua thời gian.

---

## Dataset

### Nguồn dữ liệu

**Platform:** Kaggle  
**URL:** [Spotify Global Music Dataset (2009–2025)](https://www.kaggle.com/datasets/wardabilal/spotify-global-music-dataset-2009-2025)  
**Tác giả:** Warda Bilal  
**Ngày công bố:** November 2025  

### License

**CC0: Public Domain** - Dữ liệu được phép sử dụng cho mục đích giáo dục và nghiên cứu.

### Mô tả dataset

Dataset bao gồm 2 file CSV:

1. **spotify_data clean.csv** (1.42 MB)
   - **Rows:** 8,582
   - **Columns:** 15
   - **Mô tả:** Dữ liệu về các bài hát hiện đại và nghệ sĩ gần đây (chủ yếu từ 2025)

2. **track_data_final.csv**
   - **Rows:** 8,778
   - **Columns:** 15
   - **Mô tả:** Dữ liệu về các bài hát phổ biến và kinh điển từ 2009-2023 từ các nghệ sĩ nổi tiếng

### Phương pháp thu thập dữ liệu

- **Nguồn:** Spotify's public API
- **Phương pháp:** API extraction
- **Thời gian thu thập:** 2009 - 2025
- **Mục đích:** Educational and research purposes only

### Cấu trúc dữ liệu

**Các cột chính:**
- `track_id`: ID định danh của track
- `track_name`: Tên bài hát
- `track_number`: Số thứ tự track
- `track_popularity`: Độ phổ biến của track (0-100)
- `explicit`: Nội dung tường minh (true/false)
- `artist_name`: Tên nghệ sĩ
- `artist_popularity`: Độ phổ biến của nghệ sĩ (0-100)
- `artist_followers`: Số lượng người theo dõi nghệ sĩ
- `artist_genres`: Thể loại âm nhạc của nghệ sĩ
- `album_id`: ID của album
- Và các cột khác...

### Kích thước và độ phức tạp

- **Tổng số dòng:** 17,360 (2 files kết hợp)
- **Tổng số cột:** 15 columns
- **Kích thước:** ~2.87 MB
- **Unique artists:** Hơn 8,000 nghệ sĩ
- **Thời gian:** 16 năm dữ liệu (2009-2025)

---

## Câu hỏi nghiên cứu

Dự án sẽ trả lời 6 câu hỏi nghiên cứu có ý nghĩa (2 × 3 thành viên), trong đó ít nhất 1 câu hỏi yêu cầu xây dựng và đánh giá mô hình machine learning.

### Danh sách câu hỏi (sẽ được cập nhật)

1. **[Question 1]** - TBD
2. **[Question 2]** - TBD
3. **[Question 3]** - TBD
4. **[Question 4]** - TBD
5. **[Question 5]** - TBD
6. **[Question 6 - ML Model]** - TBD

*(Các câu hỏi chi tiết sẽ được bổ sung sau quá trình khám phá dữ liệu)*

---

## Kết quả chính

*(Phần này sẽ được cập nhật sau khi hoàn thành phân tích)*

### Key Findings

1. TBD
2. TBD
3. TBD

### Insights quan trọng nhất

TBD

---

## Cấu trúc thư mục

```
DS Project/
│
├── dataset/                          # Thư mục chứa dữ liệu
│   ├── spotify_data clean.csv        # Dataset 2025
│   └── track_data_final.csv          # Dataset 2009-2023
│
├── notebooks/                        # Jupyter notebooks
│   └── spotify_analysis.ipynb        # Main analysis notebook
│
├── src/                              # Source code (nếu có)
│   ├── utils.py                      # Helper functions
│   └── models.py                     # ML models
│
├── docs/                             # Tài liệu
│   └── team_plan.md                  # Kế hoạch và phân công công việc
│
├── README.md                         # File này
├── project_requirements.txt          # Yêu cầu đồ án
├── requirements.txt                  # Python dependencies
└── .gitignore                        # Git ignore file
```

---

## Hướng dẫn chạy dự án

### Yêu cầu hệ thống

- Python 3.8 trở lên
- Jupyter Notebook hoặc JupyterLab
- Git

### Cài đặt dependencies

```bash
# Clone repository
git clone https://github.com/chisngyen/Spotify_Global_Music_Analysis.git
cd Spotify_Global_Music_Analysis

# Cài đặt các thư viện cần thiết
pip install -r requirements.txt
```

### Chạy phân tích

1. Mở Jupyter Notebook:
   ```bash
   jupyter notebook
   ```

2. Navigate đến thư mục `notebooks/`

3. Mở file `spotify_analysis.ipynb`

4. Chạy các cell theo thứ tự từ trên xuống dưới (Run All Cells)

### Lưu ý

- Đảm bảo các file dataset có trong thư mục `dataset/`
- Một số phân tích có thể mất vài phút để chạy
- Kết quả và visualizations sẽ hiển thị trực tiếp trong notebook

---

## Dependencies

### Core Libraries

```
pandas>=2.0.0
numpy>=1.24.0
matplotlib>=3.7.0
seaborn>=0.12.0
```

### Machine Learning

```
scikit-learn>=1.3.0
xgboost>=2.0.0
```

### Data Processing

```
jupyter>=1.0.0
notebook>=7.0.0
```

*(Chi tiết đầy đủ trong file `requirements.txt`)*

---

## Tiến trình dự án

- [x] Chọn dataset
- [x] Thiết lập môi trường làm việc
- [ ] Khám phá dữ liệu (EDA)
- [ ] Xác định câu hỏi nghiên cứu
- [ ] Tiền xử lý dữ liệu
- [ ] Phân tích và trả lời câu hỏi
- [ ] Xây dựng ML model
- [ ] Viết báo cáo và kết luận
- [ ] Hoàn thiện documentation

---

## Liên hệ

Nếu có bất kỳ câu hỏi nào về dự án, vui lòng liên hệ:

- **Trần Chí Nguyên** - 23122044
- **GitHub Repository:** [Spotify_Global_Music_Analysis](https://github.com/chisngyen/Spotify_Global_Music_Analysis)

---

## Tham khảo

1. Spotify API Documentation: https://developer.spotify.com/documentation/web-api
2. Kaggle Dataset: https://www.kaggle.com/datasets/wardabilal/spotify-global-music-dataset-2009-2025
3. Course materials: CSC17104 – Programming for Data Science

---

**Last Updated:** December 1, 2025
