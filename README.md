
# Dự án Phân tích & Dự báo doanh thu Olist

Dự án khai thác dữ liệu thương mại điện tử Olist để phân tích xu hướng doanh thu, hành vi khách hàng, đánh giá sản phẩm và dự báo doanh thu tương lai bằng Python và Power BI.

----------

## Mục tiêu

-   Phân tích doanh thu theo thời gian (ngày, tuần, tháng)
    
-   Đánh giá độ trễ theo sản phẩm, phương thức thanh toán
    
-   Dự báo doanh thu trong tương lai theo Prophet
    
-   Tạo Dashboard Power BI để tương tác
    

----------

## Phân tích EDA

-   Doanh thu tăng và đạt đỉnh vào **11/2017**
    
-   **Ngành furniture** và  giao trễ cao
    
-   Khách hàng đánh giá thấp nếu giao trễ
    
-   Phương thức thanh toán đa số là credit_card
    

----------

## 🔬 Mô hình Prophet dự báo doanh thu

-   Sử dụng Prophet để dự báo doanh thu tương lai theo:
    
    -   **Tháng**: `forecast_months.csv`
        
    -   **Tuần**: `forecast_weeks.csv`
        
    -   **Ngày**: `forecast_weeks.csv`
        
-   Kết hợp thành `forecast_all.csv`
    

----------

## Dashboard Power BI (5 trang)

### Trang 1: KPI, doanh thu theo thời gian và sai lệch

-   KPI: Đạt dự báo, doanh thu thực tế, sai lệch
    
-   Line chart theo tháng/tuần/ngày
- Column chart: sai lệch theo thời gian
- Pie chart: phân loại sai lệch
    

### Trang 2: Đơn hàng và sản phẩm

-   Card: tổng số đơn
    
-   Line chart: Số lượng đơn hàng qua các tháng
- Column chart: Doanh thu theo sản phẩm, tổng tiền theo phương thức thanh toán
- Pie chart: Tỷ lệ đơn hàng theo phương thức thanh toán
- Scatter chart: Tương quan giữa số sản phẩm trong một đơn hàng và tổng giá trị đơn hàng
    

### Trang 3: Giao hàng và đánh giá

-   Bar chart: Doanh thu theo điểm đánh giá, Số lượng đơn hàng giao đúng hạn và giao trễ theo tháng, Thời gian trung bình giao hàng thực tế theo loại sản phẩm
    
-   Scatter chart: Độ trễ thời gian giao hàng ảnh hưởng đến đánh giá
- Line chart: Doanh thu trung bình theo điểm đánh giá
    

### Trang 4: Khu vực khách hàng

-   Column chart: Doanh thu theo bang của khách hàng, Số đơn hàng theo thành phố, Doanh thu trung bình mỗi đơn hàng theo bang, Trễ theo bang
    

### Trang 5: Giao trễ

-   Line chart: Phân phối doanh thu theo thời gian đặt hàng trong ngày, Tỷ lệ trung bình giao trễ theo tháng
    
-   Column chart: Phân bố độ trễ và  điểm đánh giá, Tỷ lệ sản phẩm giao hàng trễ
    

## Insight chính

-   Doanh thu đạt đỉnh 11/2017 → có thể do khuyến mãi lớn
    
-   Ngành furniture trễ nhưng doanh thu cao
    
-   Sai lệch dự báo giảm dần cuối kì
    
-   Review ảnh hưởng nhiều đến đơn hàng cao giá trị
    

----------

##  Đề xuất chiến lược

1.  **Giảm tỷ lệ trễ giao**: cần đối với hàng cồng kềnh (furniture)
    
2.  **Nâng cao trải nghiệm review**: do đánh giá ảnh hưởng doanh thu
    
3.  **Cá nhân hóa theo khu vực**: shipping delay thay đổi theo tỉnh
    
4.  **Tối ưu phương thức thanh toán**: thắp tệ phơi hợp không hiệu quả
    

----------

## Kỹ thuật sử dụng

-   Python: `pandas`, `prophet`, `matplotlib`, `statsmodels`
    
-   Power BI: DAX, KPI Card, Column Chart, Line Chart, Scatter Chart,...
    
-   Dữ liệu: `olist_data_clean.csv`, `forecast_all.csv`
    


