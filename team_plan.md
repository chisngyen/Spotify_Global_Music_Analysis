# Kế hoạch nhóm và Phân công công việc

## Thông tin nhóm

**Tên dự án:** Spotify Global Music Dataset Analysis (2009–2025)  
**Môn học:** CSC17104 – Programming for Data Science  
**Học kỳ:** 1, Năm học 2025-2026  

### Thành viên nhóm

| STT | Họ và tên | MSSV | Email | Vai trò |
|-----|-----------|------|-------|---------|
| 1 | Phạm Phú Hòa | 23122030 | 23122030@hcmus.edu.vn | Leader |
| 2 | Trần Chí Nguyên | 23122044 | 23122044@hcmus.edu.vn | Member |
| 3 | Nguyễn Lâm Phú Quý | 23122048 | 23122048@hcmus.edu.vn | Member |

---

## Mục tiêu dự án

Phân tích dữ liệu Spotify (2009–2025) để:
1. Hiểu xu hướng âm nhạc theo thời gian
2. Phân tích yếu tố ảnh hưởng đến độ phổ biến bài hát/nghệ sĩ
3. Xây dựng 1 mô hình ML dự đoán track popularity
4. Khám phá quan hệ giữa loại phát hành, nội dung explicit, thời lượng và thành công
5. Cung cấp insights có giá trị cho ngành

### Kết quả mong đợi

- 1 Jupyter Notebook hoàn chỉnh (final_notebook.ipynb)
- 7 câu hỏi nghiên cứu được trả lời đầy đủ (có 2 về ML model)
- Visualizations rõ ràng, nhất quán
- README + Documentation đầy đủ

---

## Phân công công việc chi tiết

### 1) Data Collection & Setup 
- Download và verify dataset (Kaggle) — Trần Chí Nguyên
- Setup GitHub repository, branch protection — Trần Chí Nguyên
- Setup môi trường (Python, Jupyter, venv) — Tất cả
- Tạo cấu trúc project — Phạm Phú Hòa

### 2) Data Exploration 
- Dataset Overview & Basic Info — Phạm Phú Hòa
- Numerical Columns Analysis — Nguyễn Lâm Phú Quý
- Categorical Columns Analysis — Nguyễn Lâm Phú Quý
- Missing Data Analysis — Phạm Phú Hòa
- Relationships & Correlations — Tất cả
- Initial Observations Summary — Trần Chí Nguyên

### 3) Question Formulation 
- Brainstorming câu hỏi nghiên cứu — Tất cả
- Formulate Q1–Q2 — Trần Chí Nguyên
- Formulate Q3–Q4 — Phạm Phú Hòa
- Formulate Q5–Q6 (ML) — Nguyễn Lâm Phú Quý
- Review & finalize — Tất cả

### 4) Data Analysis & Modeling 
- Q1–Q2: Preprocess, Analysis, Viz, Interpretation — Trần Chí Nguyên
- Q4–Q5: Preprocess, Analysis, Viz, Interpretation — Nguyễn Lâm Phú Quý
- Q3, Q6, Q7 (ML): Preprocess, Analysis, Viz, Interpretation, Train, Evaluate — Phạm Phú Hòa

### 5) Project Summary & Documentation
- Key Findings Summary — Trần Chí Nguyên
- Limitations & Future Directions — Phạm Phú Hòa
- Update README.md (final) — Nguyễn Lâm Phú Quý
- Individual Reflections — Tất cả
- Code review & cleanup — Tất cả
- Final testing & verification — Tất cả

### Tỷ lệ đóng góp
- Phạm Phú Hòa: ~33% — EDA, Q1–Q2, Limitations
- Trần Chí Nguyên: ~34% — PM, EDA, Q3–Q4, Summary
- Nguyễn Lâm Phú Quý: ~33% — Cat EDA, ML Q5–Q6, README final

---

## Quy trình làm việc

### 1) Version Control (Git)
- Branches:
  - main: production-ready
  - develop: integration branch
  - feature/<ten-feature>: mỗi task/câu hỏi
- Commits:
  - feat:, fix:, docs:, style:, refactor:, test:, chore:
- PR rules:
  - ≥1 reviewer
  - CI lint + tests must pass
  - Squash merge to keep history clean

### 2) Communication
- GitHub Issues/Projects: task tracking
- Zalo/Messenger: daily sync
- Google Meet: weekly 45’
  - Review tiến độ
  - Blockers
  - Kế hoạch tuần tới

### 3) Quality Standards
- Code: PEP 8, meaningful names, no hard-coded paths, proper error handling
- Notebook: clear markdown, reproducible top-to-bottom, tidy plots
- Docs: README, inline comments, function docstrings
- Data: no silent coercion, explicit NaN handling, reproducible seeds

---

## Cấu trúc Project (đề xuất)

```
Spotify_Global_Music_Analysis/
├─ dataset/
│  └─ track_data_final.csv
├─ notebooks/
│  ├─ eda.ipynb
│  └─ final_notebook.ipynb
├─ src/
│  ├─ data_loading.py
│  ├─ preprocessing.py
│  ├─ viz.py
│  └─ models.py
├─ reports/
│  └─ figures/
├─ tests/
│  └─ test_preprocessing.py
├─ docs/
│  └─ README.md
├─ project_requirements.txt
└─ .github/workflows/ci.yml
```

---

## Success Criteria

1. Trả lời đủ 6 câu hỏi (có 1 ML model)
2. Notebook chạy từ đầu đến cuối không lỗi
3. Visualizations rõ ràng, nhất quán
4. README + comments + markdown đầy đủ
5. Tuân thủ project_requirements.txt
6. Mỗi thành viên đóng góp tương đương (~33%)
7. Code theo best practices, PR reviewed

---

## Rủi ro và Giải pháp

- Data Quality Issues
  - Mitigation: Thorough EDA, explicit preprocessing, validation checks
- Time Management
  - Mitigation: Weekly checkpoints, small PRs, buffer before deadline
- Technical Difficulties
  - Mitigation: Pair-programming, references, instructor help
- Scope Creep
  - Mitigation: Giữ 6 câu hỏi, freeze scope sau Week 2

---

## Tools

- Python 3.10+
- Jupyter Notebook
- Pandas, NumPy, Scikit-learn, Seaborn/Matplotlib
- XGBoost/LightGBM (cho ML)
- VS Code, Git & GitHub