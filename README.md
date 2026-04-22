# Exploring Mental Health

## Thông tin thành viên

| Họ và tên | MSSV |
| :---- | :----: |
| Phan Thị Phương Chi | 23120025 |
| Trần Thanh Đạt | 23120030 |
| Lê Minh Hải | 23120041 |
| Hồ Thuỳ Hương | 23120046 |
| Trần Kim Ngân | 23120060 |
| Cao Tiến Thành | 23120088 |

---

## Phân công công việc
| Thành viên | MSSV | Công việc | % Hoàn thành |
| :--- | :--- | :--- | :---: |
| Phan Thị Phương Chi | 23120025 | Phân tích EDA, lựa chọn thuật toán và tối ưu hóa. | 100% |
| Trần Thanh Đạt | 23120030 | Biên soạn báo cáo, thiết kế slide và biên tập video. | 100% |
| Lê Minh Hải | 23120041 | Biên soạn báo cáo, thiết kế slide và biên tập video. | 100% |
| Hồ Thuỳ Hương | 23120046 | Xử lý dữ liệu thiếu, làm sạch nhiễu và tạo biến mới. | 100% |
| Trần Kim Ngân | 23120060 | Phân tích EDA, lựa chọn thuật toán và tối ưu hóa. | 100% |
| Cao Tiến Thành | 23120088 | Xử lý dữ liệu thiếu, làm sạch nhiễu và tạo biến mới. | 100% |

---

## Mô tả tập dữ liệu
- Tên dữ liệu: [Exploring Mental Health Data](https://www.kaggle.com/competitions/playground-series-s4e11)

- Mục tiêu: Phân tích các yếu tố ảnh hưởng đến sức khỏe tâm thần, dự đoán xu hướng hoặc tìm ra các mối tương quan giữa môi trường sống/làm việc và tình trạng tâm lý từ đó phát triển mô hình dự đoán dự vào các yếu tố trên.

- Thông tin và ý nghĩa của các biến:

    | STT | Tên biến | Ý nghĩa | Kiểu dữ liệu |
    | :-- | :--- | :--- | :--- |
    | 1 | **id** | Mã định danh duy nhất của mỗi khách hàng. | Phân loại |
    | 2 | **Name** | Tên của người tham gia khảo sát. | Phân loại |
    | 3 | **Gender** | Giới tính (Nam, Nữ). | Nhị phân |
    | 4 | **Age** | Tuổi của người tham gia. | Số trị |
    | 5 | **City** | Thành phố sinh sống. | Phân loại |
    | 6 | **Working Status** | Là Người đi làm hay Sinh viên. | Nhị phân |
    | 7 | **Profession** | Nghề nghiệp của người đi làm. | Phân loại |
    | 8 | **Academic Pressure** | Mức độ áp lực học tập (thang điểm 0-5). | Thứ bậc |
    | 9 | **Work Pressure** | Mức độ áp lực công việc (thang điểm 0-5). | Thứ bậc |
    | 10 | **CGPA** | Điểm trung bình học tập của sinh viên. | Số trị |
    | 11 | **Study Satisfaction** | Mức độ hài lòng về học tập (0-5). | Thứ bậc |
    | 12 | **Job Satisfaction** | Mức độ hài lòng về công việc (0-5). | Thứ bậc |
    | 13 | **Sleep Duration** | Thời gian ngủ trung bình. | Phân loại |
    | 14 | **Dietary Habits** | Chế độ ăn uống hàng ngày. | Phân loại |
    | 15 | **Degree** | Bằng cấp cao nhất đạt được. | Phân loại |
    | 16 | **Suicidal thoughts** | Đã từng có ý định tự tử chưa (Yes/No). | Nhị phân |
    | 17 | **Work/Study Hours** | Thời gian học tập hoặc làm việc trong ngày. | Số trị |
    | 18 | **Financial Stress** | Mức độ áp lực tài chính (0-5). | Thứ bậc |
    | 19 | **Family History** | Gia đình có tiền sử bệnh tâm thần hay không. | Nhị phân |
    | 20 | **Depression** | Tình trạng trầm cảm (1: Có, 0: Không). | Mục tiêu |

---

## Hướng dẫn cài đặt môi trường
1. **Clone repository:**
   ```bash
   git clone https://github.com/tdat1465/exploring-mental-health-data-lab.git
   cd exploring-mental-health-data-lab
   ```

2. **Cài đặt thư viện**
    ```bash
    pip install -r requirements.txt
    ```

## Cấu trúc thư mục

```text

exploring-mental-health-data-lab/
├── artifacts/                          # Chứa các file model và pipeline đã huấn luyện
│   ├── feature_model_baseline.joblib
│   ├── feature_pipeline.joblib
│   ├── model_cat.joblib
│   ├── model_stack.joblib
│   ├── model_xgb_scale.joblib
│   └── model_xgb.joblib
├── data/                     
│   ├── processed/                      # Dữ liệu đã qua xử lý (sau khi làm sạch, biến đổi)
│   ├── raw/                            # Dữ liệu thô (gốc) ban đầu
│   ├── test/                           # Dữ liệu dùng để kiểm tra (test set)
│   └── train/                          # Dữ liệu dùng để huấn luyện (train set)
├── notebooks/                
│   ├── EDA.ipynb                       # Phân tích dữ liệu khám phá
│   ├── feature_engineering.ipynb       # Kỹ thuật đặc trưng
│   ├── modeling.ipynb                  # Huấn luyện và lựa chọn mô hình
│   ├── prediction.ipynb                # Dự đoán trên tập dữ liệu mới
│   └── preprocessing.ipynb             # Tiền xử lý dữ liệu
├── README.md  
├── requirements.txt               
└── submission.csv                      # File kết quả dự đoán của tập test.csv

