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
   - **Mô tả:** Dữ liệu về các bài hát hiện đại và nghệ sĩ trên Spotify từ 2009 đến nay

2. **track_data_final.csv**
   - **Rows:** 8,778
   - **Columns:** 15
   - **Mô tả:** Bản mở rộng của dữ liệu trong `sportify_data clean.csv`

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

Dự án trả lời 6 câu hỏi nghiên cứu có ý nghĩa (2 × 3 thành viên), trong đó có 1 câu hỏi xây dựng và đánh giá mô hình machine learning.

### Danh sách câu hỏi

1. **[Câu hỏi 1] So sánh loại album**
   - Độ phổ biến khác nhau như thế nào giữa Album, Single và Compilation?

2. **[Câu hỏi 2] Explicit content và popularity**
   - Những bài hát có explicit content có độ phổ biến cao hơn hay thấp hơn so với những bài không explicit?

3. **[Câu hỏi 3] Golden duration analysis**
   - Có tồn tại khoảng thời lượng "vàng" nào cho độ phổ biến của bài hát không?

4. **[Câu hỏi 4] Số lượng bài hát và độ nổi tiếng nghệ sĩ**
   - Nghệ sĩ phát hành nhiều bài hát có xu hướng nổi tiếng hơn không?

5. **[Câu hỏi 5] Classic songs vs Recent songs**
   - Nhạc cũ (2009-2015) còn phổ biến bằng nhạc mới (2020-2025) không?

6. **[Câu hỏi 6 - ML Model] Đặc trưng quan trọng theo từng phân khúc**
   - Các đặc trưng nào quan trọng để dự đoán độ phổ biến của track ở từng phân khúc (thấp, trung bình, cao)?

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

| Model | Val R² (10-fold) | Val R² Std | Val MAE | Val RMSE | Test R² | Test MAE | Test RMSE |
|-------|-----------------|------------|---------|----------|---------|----------|-----------|
| **LightGBM** | **0.28** | 0.04 | **15.08** | **20.35** | **0.30** | **15.04** | **20.14** |
| Gradient Boosting | 0.28 | 0.04 | 15.20 | 20.40 | 0.30 | 15.16 | 20.23 |
| XGBoost | 0.26 | 0.04 | 15.28 | 20.69 | 0.29 | 15.15 | 20.26 |
| Random Forest | 0.25 | 0.03 | 15.21 | 20.77 | 0.29 | 15.04 | 20.38 |
| Extra Trees | 0.24 | 0.04 | 15.16 | 20.88 | 0.25 | 15.21 | 20.93 |
| Linear Regression | 0.22 | 0.03 | 16.15 | 21.24 | 0.23 | 16.11 | 21.11 |

**Mô hình tốt nhất:** LightGBM với Test R²=0.30, Test MAE=15.04, Test RMSE=20.14

### Phát hiện thú vị nhất

**Nhạc cũ (2009-2015) vẫn duy trì độ phổ biến tương đương nhạc mới (2020-2025)**, chứng tỏ giá trị của catalog âm nhạc là lâu dài. Điều này mở ra cơ hội kinh doanh cho việc khai thác lại các bản thu cũ và tạo playlist "throwback"

---

## Cấu trúc thư mục

```
Spotify_Global_Music_Analysis/
│
├── dataset/                          # Thư mục chứa dữ liệu
│   ├── spotify_data clean.csv        # Dataset chính (8,582 tracks)
│   └── track_data_final.csv          # Dataset mở rộng (8,778 tracks)
│
├── notebooks/                        # Jupyter notebooks
│   ├── 01_data_collection.ipynb      # Thu thập và load dữ liệu
│   ├── 02_data_exploration.ipynb     # Khám phá dữ liệu ban đầu
│   ├── 03_question_formulation.ipynb # Xây dựng câu hỏi nghiên cứu
│   ├── 04_data_analysis.ipynb        # Phân tích và trả lời câu hỏi
│   ├── 05_reflection.ipynb           # Phản ánh và kết luận
│   └── final_notebook.ipynb          # Notebook tổng hợp đầy đủ
│
├── team_plan.md                      # Kế hoạch và phân công làm việc
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
