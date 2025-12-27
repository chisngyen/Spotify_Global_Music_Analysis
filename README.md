# Spotify Global Music Dataset Analysis (2009–2025)

## Thông tin nhóm

### Thành viên
| Họ và tên | MSSV | Email |
|-----------|------|-------|
| Phạm Phú Hòa | 23122030 | 23122030@student.hcmus.edu.vn |
| Trần Chí Nguyên | 23122044 | 23122044@student.hcmus.edu.vn |
| Nguyễn Lâm Phú Quý | 23122048 | 23122048@student.hcmus.edu.vn |

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

Dataset bao gồm: **track_data_final.csv**
   - **Rows:** 8,778
   - **Columns:** 15

### Phương pháp thu thập dữ liệu

- **Nguồn:** Spotify's public API
- **Phương pháp:** API extraction
- **Thời gian thu thập:** 2009 - 2025
- **Mục đích:** Học tập và nghiên cứu

### Cấu trúc dữ liệu

Ý nghĩa các cột:

Thông tin bài hát (Track Information):
- `track_id`: Mã định danh duy nhất của bài hát
- `track_name`: Tên bài hát
- `track_number`: Vị trí trong album
- `track_popularity`: Độ phổ biến (0-100)
- `track_duration_ms`: Thời lượng (milliseconds)
- `explicit`: Có nội dung nhạy cảm không

Thông tin nghệ sĩ (Artist Information):
- `artist_name`: Tên nghệ sĩ
- `artist_popularity`: Độ phổ biến nghệ sĩ (0-100)
- `artist_followers`: Số người theo dõi
- `artist_genres`: Thể loại âm nhạc

Thông tin Album (Album Information):
- `album_id`: Mã định danh album
- `album_name`: Tên album
- `album_release_date`: Ngày phát hành
- `album_total_tracks`: Tổng số bài
- `album_type`: Loại (album/single/compilation)

Các cột quan trọng cho phân tích: `track_popularity`, `artist_popularity`, `artist_followers`, `artist_genres`, `album_release_date`, `track_duration_ms`.

### Kích thước và độ phức tạp

- **Tổng số dòng:** 17,360 (2 files kết hợp)
- **Tổng số cột:** 15 columns
- **Kích thước:** ~2.87 MB
- **Unique artists:** Hơn 8,000 nghệ sĩ
- **Thời gian:** 16 năm dữ liệu (2009-2025)

---

## Câu hỏi nghiên cứu

Dự án trả lời 6 câu hỏi nghiên cứu có ý nghĩa (2 × 3 thành viên), trong đó có 1 câu hỏi xây dựng và đánh giá mô hình machine learning.

### Danh sách câu hỏi

1. Loại album nào (album, compilation, single) có độ phổ biến cao hơn?
2. Bài hát có nội dung nhạy cảm (explicit = True) có phổ biến hơn không?
3. Có tồn tại "thời lượng vàng" nào cho bài hát để đạt độ phổ biến cao nhất không?
4. Nghệ sĩ phát hành nhiều bài hơn có đạt độ nổi tiếng cao hơn không?
5. Bài hát cũ (2009-2015) có giữ được độ phổ biến so với bài hát mới (2020-2025) không?
6. Yếu tố nào quan trọng nhất ở từng nhóm mức độ nổi tiếng khác nhau?
7. Có thể dự đoán độ phổ biến bài hát bằng machine learning không? Độ chính xác ra sao?

---

## Kết quả chính

### Phát hiện chính từ phân tích

**1. Nội dung tường minh không làm giảm độ phổ biến**
- Các bài hát có nội dung tường minh đạt mức độ phổ biến cao hơn đáng kể (57.5 vs 50.5)
- Nghệ sĩ không cần tự kiểm duyệt để đạt được thành công thương mại

**2. Khoảng thời lượng vàng: 3.5-4.5 phút**
- Bài hát trong khoảng này đạt popularity cao nhất (~55.6-55.9)
- Bài hát quá ngắn (<2p) hoặc quá dài (>5p) có độ phổ biến thấp hơn

**3. Album vượt trội hơn single**
- Full album có độ phổ biến cao nhất (55.5), vượt single (46.1) và compilation (40.5)
- Người nghe có xu hướng ưa thích trải nghiệm album trọn vẹn

**4. Số lượng bài hát ảnh hưởng đến độ nổi tiếng nghệ sĩ**
- Nghệ sĩ phát hành nhiều (>100 tracks) đạt popularity gần gấp đôi nghệ sĩ ít (1-20 tracks)
- Việc phát hành đều đặn quan trọng hơn hoàn thiện một vài bài

**5. Yếu tố thành công khác nhau theo từng phân khúc**
- Phân khúc thấp: Danh tiếng nghệ sĩ là yếu tố chính (R²=0.47)
- Phân khúc cao: Khó dự đoán, phụ thuộc nhiều vào may mắn và viral (R²=0.03)

### Kết quả mô hình Machine Learning

**Mô hình dự đoán độ phổ biến track (Track Popularity Prediction):**

| Model | Val R² (10-fold) | Val R² Std | Val MAE (10-fold) | Val RMSE (10-fold) | Test R² | Test MAE | Test RMSE |
|---|---|---|---|---|---|---|---|
| Linear Regression | 0.247905 | 0.027522 | 15.590526 | 20.834189 | 0.266076 | 15.492175 | 20.674076 |
| XGBoost | 0.305837 | 0.026445 | 14.344764 | 20.015406 | 0.335108 | 14.191945 | 19.677780 |
| Random Forest | 0.326508 | 0.028958 | 14.198489 | 19.715141 | 0.351970 | 14.080961 | 19.426658 |
| Gradient Boosting | 0.320680 | 0.026713 | 14.337259 | 19.800271 | 0.348077 | 14.119382 | 19.484922 |
| Extra Trees | 0.316147 | 0.041134 | 13.971972 | 19.861647 | 0.337142 | 13.885328 | 19.647661 |
| LightGBM | 0.319573 | 0.028751 | 14.305053 | 19.815313 | 0.350530 | 14.086811 | 19.448228 |
| Ensemble (Simple Avg) | - | - | - | - | 0.361574 | 14.035164 | 19.282167 |
| Ensemble (Weighted Avg) | - | - | - | - | 0.362591 | 14.002097 | 19.266803 |

**Mô hình tốt nhất:** LightGBM với Test R^2=0.355, Test MAE=14.08, Test RMSE=19.44

### Phát hiện thú vị nhất

**Nhạc cũ (2009-2015) vẫn duy trì độ phổ biến tương đương nhạc mới (2020-2025)**, chứng tỏ giá trị của catalog âm nhạc là lâu dài. Điều này mở ra cơ hội kinh doanh cho việc khai thác lại các bản thu cũ và tạo playlist "throwback"

---

## Cấu trúc thư mục

```
Spotify_Global_Music_Analysis/
│
├── dataset/                          # Thư mục chứa dữ liệu
│   └── track_data_final.csv          # Dataset (8,778 tracks)
│
├── notebooks/                        # Jupyter notebooks
│   ├── 01_data_collection.ipynb      # Thu thập và load dữ liệu
│   ├── 02_data_exploration.ipynb     # Khám phá dữ liệu ban đầu
│   ├── 03_question_formulation.ipynb # Xây dựng câu hỏi nghiên cứu
│   ├── 04_data_analysis.ipynb        # Phân tích và trả lời câu hỏi
│   ├── 04_q1_q2.ipynb                # Notebook con
│   ├── 04_q3_q4_q5.ipynb             # Notebook con
│   ├── 04_q6_q7.ipynb                # Notebook con
│   ├── 05_reflection.ipynb           # Phản ánh và kết luận
│   └── final_notebook.ipynb          # Notebook tổng hợp đầy đủ
│ 
├── README.md                         # File này - Tổng quan dự án
└── requirements.txt                  # Python dependencies
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
scipy>=1.10.0
```

### Visualization

```
matplotlib>=3.7.0
seaborn>=0.12.0
```

### Machine Learning

```
scikit-learn>=1.3.0
xgboost>=2.0.0
lightgbm>=4.0.0
```

### Development Tools

```
jupyter>=1.0.0
notebook>=7.0.0
```

### Installation
```
pip install -r requirements.txt
```

---

## Liên hệ

Nếu có bất kỳ câu hỏi nào về dự án, vui lòng liên hệ:

- **Trần Chí Nguyên** - 23122044
- **GitHub Repository:** [Spotify_Global_Music_Analysis](https://github.com/chisngyen/Spotify_Global_Music_Analysis)

