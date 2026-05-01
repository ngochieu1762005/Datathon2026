# DATATHON 2026 - The Gridbreaker

## 1. Giới thiệu

Repository này là bài làm của đội thi **Nguyễn Ngọc Hiếu** cho cuộc thi **DATATHON 2026 Vòng 1 - The Gridbreaker**.

### Thành viên đội thi

- Nguyễn Ngọc Yến
- Nguyễn Ngọc Hiếu
- Huỳnh Kim Gia Bảo
- Phạm Minh Trí

Bài toán chính của cuộc thi là phân tích dữ liệu kinh doanh của một doanh nghiệp thương mại điện tử thời trang và xây dựng mô hình dự báo doanh thu.

File dự báo cuối cùng của nhóm là:

```text
sub_final.csv
```

## 2. Cấu trúc repository

```text
Datathon2026/
│
├── README.md
├── requirements.txt
├── sub_final.csv
│
├── notebooks/
│   ├── 01_clean-data-and-create-daily-table.ipynb
│   ├── 02_eda.ipynb
│   └── 03_pipeline_final.ipynb
│
├── raw_data/
│   ├── baseline.ipynb
│   ├── customers.csv
│   ├── geography.csv
│   ├── inventory.csv
│   ├── order_items.csv
│   ├── orders.csv
│   ├── payments.csv
│   ├── product_items.csv
│   ├── promotions.csv
│   ├── returns.csv
│   ├── reviews.csv
│   ├── sales.csv
│   ├── sample_submission.csv
│   ├── shipments.csv
│   └── web_traffic.csv
│
├── outputs/
│   ├── daily_table.csv
│   ├── sub_final.csv
│   └── outputs_part2/
│       ├── figures/
│       └── tables/
│
└── report/
    ├── img/
    ├── neurips_2025.sty
    ├── neurips_2025.tex
    └── report.pdf
```

## 3. Dữ liệu đầu vào

Toàn bộ dữ liệu gốc được đặt trong thư mục:

```text
raw_data/
```

Các file dữ liệu chính bao gồm:

```text
customers.csv
geography.csv
inventory.csv
order_items.csv
orders.csv
payments.csv
product_items.csv
promotions.csv
returns.csv
reviews.csv
sales.csv
sample_submission.csv
shipments.csv
web_traffic.csv
```

Thư mục này là điểm bắt đầu của toàn bộ quá trình xử lý dữ liệu. Khi chạy lại bài làm, cần giữ nguyên tên file và đường dẫn như trong repository để tránh lỗi khi notebook đọc dữ liệu.

## 4. Cài đặt môi trường

Cài đặt các thư viện cần thiết bằng lệnh:

```bash
pip install -r requirements.txt
```

File `requirements.txt` chứa các thư viện phục vụ cho xử lý dữ liệu, trực quan hóa, mô hình dự báo và giải thích mô hình.

## 5. Cách chạy lại bài làm

Để tái tạo lại kết quả, chạy các notebook trong thư mục `notebooks/` theo đúng thứ tự sau:

```text
1. notebooks/01_clean-data-and-create-daily-table.ipynb
2. notebooks/02_eda.ipynb
3. notebooks/03_pipeline_final.ipynb
```

Ý nghĩa từng notebook:

### Notebook 1: Làm sạch dữ liệu và tạo bảng ngày

```text
01_clean-data-and-create-daily-table.ipynb
```

Notebook này đọc dữ liệu gốc từ thư mục `raw_data/`, xử lý các bảng cần thiết và tạo bảng dữ liệu tổng hợp theo ngày.

Kết quả quan trọng được tạo ra là:

```text
outputs/daily_table.csv
```

File này đóng vai trò là bảng dữ liệu trung gian chính, được sử dụng cho cả phân tích EDA và mô hình dự báo.

### Notebook 2: Phân tích dữ liệu

```text
02_eda.ipynb
```

Notebook này thực hiện phần phân tích khám phá dữ liệu, trực quan hóa xu hướng và xây dựng các insight kinh doanh.

Các biểu đồ và bảng phân tích được lưu trong:

```text
outputs/outputs_part2/
```

Trong đó:

```text
outputs/outputs_part2/figures/
```

chứa các biểu đồ đã xuất ra dưới dạng ảnh.

```text
outputs/outputs_part2/tables/
```

chứa các bảng số liệu trung gian phục vụ cho phân tích và báo cáo.

### Notebook 3: Pipeline dự báo cuối cùng

```text
03_pipeline_final.ipynb
```

Notebook này xây dựng pipeline dự báo doanh thu, tạo đặc trưng, huấn luyện mô hình và xuất file dự báo cuối cùng.

Kết quả đầu ra là:

```text
sub_final.csv
```

File này cũng được lưu trong:

```text
outputs/sub_final.csv
```


## 7. File dự báo cuối cùng

File nộp cuối cùng là:

```text
sub_final.csv
```

Định dạng file:

```text
Date,Revenue,COGS
2023-01-01,...
2023-01-02,...
2023-01-03,...
```

Score: 634048.35161

## 8. Báo cáo

Báo cáo cuối cùng được lưu tại:

```text
report/report.pdf
```

Các file liên quan đến báo cáo gồm:

```text
report/neurips_2025.tex
report/neurips_2025.sty
report/img/
```

Trong đó:

- `report.pdf` là bản báo cáo cuối cùng
- `neurips_2025.tex` là file LaTeX chính
- `neurips_2025.sty` là file định dạng mẫu báo cáo
- `report/img/` chứa các hình ảnh được đưa vào báo cáo

## 9. Nội dung chính của bài làm

Bài làm được xây dựng theo một quy trình đầy đủ:

1. Đọc và làm sạch dữ liệu gốc
2. Tổng hợp dữ liệu về cấp độ ngày
3. Phân tích xu hướng doanh thu và giá vốn
4. Phân tích tính mùa vụ theo năm, tháng, tuần và ngày
5. Đánh giá tác động của khuyến mãi
6. So sánh hành vi kinh doanh giữa ngày thường, cuối tuần và cuối tháng
7. Xây dựng mô hình dự báo doanh thu
8. Xuất file dự báo cuối cùng để nộp Kaggle
9. Viết báo cáo tổng hợp kết quả phân tích và phương pháp mô hình

## 10. Tính tái lập

Để chạy lại kết quả, cần đảm bảo:

- Giữ nguyên cấu trúc thư mục như trong repository
- Đặt đầy đủ dữ liệu gốc trong thư mục `raw_data/`
- Chạy notebook theo đúng thứ tự từ 01 đến 03
- Không đổi tên các file đầu vào
- Tạo được file `outputs/daily_table.csv` trước khi chạy mô hình
- File nộp cuối cùng là `sub_final.csv`

Bài làm không sử dụng dữ liệu ngoài. Các đặc trưng và kết quả đều được tạo từ dữ liệu do cuộc thi cung cấp.


