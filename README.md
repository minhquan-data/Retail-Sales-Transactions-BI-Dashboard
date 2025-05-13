
# 🛍️ Dự án Business Intelligence – Phân tích Giao dịch Bán lẻ

Dự án Business Intelligence (BI) này tập trung vào việc phân tích dữ liệu giao dịch bán lẻ nhằm khám phá các xu hướng doanh thu, sản phẩm bán chạy và hành vi khách hàng. Dự án sử dụng **Python** để làm sạch dữ liệu, **SQL Server** để lưu trữ và xử lý, và **Power BI** để trực quan hóa dữ liệu.

## 🔧 Công cụ & Công nghệ
- **Python (Pandas, NumPy)** – Làm sạch và xử lý dữ liệu thô.
- **SQL Server** – Thiết kế mô hình dữ liệu **Star Schema** và thực thi truy vấn.
- **Power BI** – Xây dựng báo cáo tương tác và sử dụng **DAX** để tính toán.

## 📊 Tổng quan dự án

### 📁 Dữ liệu
- Hơn **130.000 dòng dữ liệu giao dịch bán lẻ**
- Bao gồm: Số tiền bán, thông tin sản phẩm (SKU, danh mục), thông tin khách hàng và chi tiết giao dịch.

### 🛠️ Quy trình ETL
1. **Làm sạch & Chuẩn hóa dữ liệu** *(Python)*:
   - Xử lý giá trị thiếu, định dạng lại ngày tháng, chuẩn hóa tên cột
   - Xuất dữ liệu đã xử lý ra file `.csv`

2. **Thiết kế mô hình dữ liệu**:
   - Áp dụng **mô hình Star Schema** gồm:
     - Bảng sự kiện: `FactSales`
     - Các bảng chiều: `DimProduct`, `DimCustomer`, `DimDate`
   - Nhập dữ liệu vào **SQL Server**

3. **Trực quan hóa & phân tích** *(Power BI)*:
   - Kết nối Power BI với SQL Server
   - Tạo dashboard sử dụng các biểu đồ và công thức DAX

## 📈 Các trang Dashboard

### 1. **Tổng quan doanh thu**
- Tổng doanh thu, số lượng giao dịch
- Doanh thu theo tháng
- Khách hàng và sản phẩm có doanh số cao nhất

### 2. **Phân tích khách hàng**
- Phân tích RFM: Gần đây (Recency), Tần suất (Frequency), Giá trị (Monetary)
- Phân loại khách hàng: Mới, Quay lại, Trung thành, Rời bỏ
- Biểu đồ phân bổ doanh thu theo từng phân khúc khách hàng

### 3. **Phân tích sản phẩm**
- Doanh thu theo SKU và danh mục SKU
- Giá trung bình và số lượng bán trên mỗi SKU
- Xu hướng doanh thu theo thời gian và danh mục sản phẩm

## 🧠 Các phát hiện chính
- Xác định các tháng có doanh thu cao nhất và sản phẩm bán chạy nhất
- Phân khúc khách hàng để hiểu rõ hành vi mua sắm
- Đánh giá hiệu quả sản phẩm theo thời gian

## 📌 Kết quả đạt được
- Hoàn thành giải pháp BI đầy đủ từ xử lý dữ liệu đến báo cáo
- Hỗ trợ ra quyết định dựa trên dữ liệu cho hoạt động bán lẻ

## 📁 Tệp dự án
- `Retail_Sales_Transactions_BI.ipynb`: File Python dùng để làm sạch dữ liệu
- Các file `.csv`: dữ liệu sau xử lý để import vào SQL Server
- File báo cáo Power BI (`.pbix`): chưa bao gồm trong thư mục này
