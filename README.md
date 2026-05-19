b1: 		pip install pandas openpyxl

b2: 		python main.py





# IAP BENCHMARK - CHƯƠNG TRÌNH CHẤM ĐIỂM LỊCH TRỰC COI THI

Chương trình tự động kiểm tra toàn bộ các ràng buộc cứng (Hard Constraints), tính điểm phạt cho các ràng buộc mềm (Soft Constraints) của lịch gác thi và xuất báo cáo trực quan ra Excel.

## 1. Cấu trúc thư mục và Chuẩn bị dữ liệu
Đặt chính xác 3 file dữ liệu Excel gốc đầu vào vào thư mục `data/` theo đúng cấu trúc dưới đây:

```text
iap_benchmark/
├── data/
│   ├── can_bo.xlsx             # Danh sách cán bộ gốc
│   ├── ca_thi.xlsx             # Danh sách ca thi yêu cầu
│   └── lich_truc_final.xlsx    # Lịch trực cần chấm điểm
├── config.py                   # Cấu hình hằng số và trọng số
├── data_loader.py              # Tiền xử lý dữ liệu Pandas
├── hard_constraints.py         # Kiểm tra tính khả thi (Hard)
├── soft_constraints.py         # Tính điểm trừ tối ưu (Soft)
├── excel_exporter.py           # Xuất báo cáo định dạng Excel
└── main.py                     # File thực thi chính (Orchestrator)
