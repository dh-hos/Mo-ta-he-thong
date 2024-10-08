<div align="center">

`Công ty TNHH Giải Pháp Kỹ Thuật Số DH - Mẫu: DH-02: Mô tả thay đổi hệ thống DHG.Hospital 3.1`

</div>

<div align="center">
  <img src="https://raw.githubusercontent.com/dh-hos/dhg.hospitalprinter/main/Deploy_Tools/Logo.ico" alt="Simple Icons" width=70>
  <h1>PHIẾU MÔ TẢ THAY ĐỔI HỆ THỐNG</h1>  
</div>
<div align="center">

#### Chủ đề: GIẤY CHỨNG NHẬN PHẪU THUẬT TỰ THIẾT KẾ [THÔNG TƯ 32/2023/TT-BYT VĂN BẢN HIỆN HÀNH](https://gofile.me/78TQg/1OBGlzHz8)

</div>

###### :eight_spoked_asterisk: Người lập: [**Nguyễn Triều Vương**](https://github.com/vuongdh)

###### :eight_spoked_asterisk: Ngày lập: **25/08/2024**

###### :eight_spoked_asterisk: Khách hàng: **Tất cả khách hàng sử dụng DHG.Hospital**

###### :eight_spoked_asterisk: Xử lý yêu cầu

:white_check_mark: **Mở rộng tham số: nt.giaycnpta5**
``` sql
UPDATE CURRENT.system SET diengiai = 'Giấy chứng nhận phẫu thuật A5' 
        || E'\n' 
        ||'Giá trị:' || E'\n' 
        ||'- 0 (hoặc null): Không sử dụng.' || E'\n' 
        ||'- 1: Sử dụng (mẫu Crystal Report)' || E'\n' 
        ||'- 2: Sử dụng (mẫu tự thiết kế).'
WHERE UPPER(tents) = UPPER('nt.giaycnpta5')
``` 

:white_check_mark: **Mẫu giấy CNPT**

![image](https://github.com/user-attachments/assets/4e349cba-50aa-44e5-9f1f-c531953aae6f)

![image](https://github.com/user-attachments/assets/c3f1cd14-e891-47b4-838b-9fb0ca35734b)

:white_check_mark: **Mô tả dữ liệu**
| STT | TÊN CỘT | KIỂU DỮ LIỆU | GHI CHÚ |
|:-------:|-------|:-------:|-------|
|1|hoten |VARCHAR|Họ và tên người bệnh.|
|2|diachi|VARCHAR|Địa chỉ |
|3|vaovien|VARCHAR|Ngày vào viện định dạng (..giờ ..phút..ngày..tháng...năm)|
|4|ravien|VARCHAR|Ngày ra viện định dạng (..giờ ..phút..ngày..tháng...năm)|
|5|vitri|VARCHAR|Đã phẫu thuật (Vị trí, phương thức,...) (phauthuat.vitri)|
|6|sophieu|VARCHAR|Số phiếu (02/BV-02)|
|7|nhommau|VARCHAR|Nhóm máu (phauthuat.nhommau)|
|8|rh|VARCHAR|Rh (phauthuat.rh)|
|9|soluutru|VARCHAR|Số lưu trữ (bnnoitru.soluu)|
|10|trinhtupt|VARCHAR|Cách thức phẫu thuật (phauthuat.trinhtu)|
|11|bsphauthuat|VARCHAR|Bs phẫu thuật (bs phẫu thuật chính)|
|12|ngayvv_dd|VARCHAR|Ngày vào viện định dạng: dd/MM/yyyy|
|13|ngayrv_dd|VARCHAR|Ngày ra viện định dạng: dd/MM/yyyy|

