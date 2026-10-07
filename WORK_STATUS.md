# WORK_STATUS

## Mục tiêu hiện tại
Lưu bản notebook Colab đã chạy vào đúng cấu trúc project để người dùng tự push và nộp.

## Việc đã hoàn thành
- Đọc README, liệt kê bốn bài code bắt buộc: 5.1, 5.2, 6.1, 7.1.
- Kiểm tra Git ban đầu: notebook đã có output lỗi thiếu `matplotlib` từ trước; thay đổi này được giữ nguyên.
- Hoàn thiện các TODO code 5.1, 5.2, 6.1, 7.1 và bonus 8.1, giữ nguyên scaffold.
- Đặt `STUDENT_ID = "2A202602759"` theo tên project. Dựa trên log công khai do notebook sinh, điền chẩn đoán `UWB` / `underrated_noise` và cách sửa `inflate_R`.
- Chạy riêng các cell có liên quan bằng NumPy: kiểm tra 5.1, 5.2, 6.1, 7.1, 8.1, 9.1 và 9.2 đều pass. NIS UWB ban đầu mean 13.22, median 9.31; sau sửa pooled mean NIS 2.39 trên 1350 phép đo.
- Đọc output lưu trên Colab tại liên kết người dùng gửi: setup chạy với NumPy 2.1.3; các ô 5.1, 5.2, 6.1, 7.1, 8.1 đều in `passed`; ô 9.2 in pooled mean NIS 2.39 và `passed`. Không thấy traceback trong các output lưu đã đọc.
- Tải bản `.ipynb` từ Colab và xác nhận 119 cell, source/ID cell giống bản local, 47 cell có output, 19 hình PNG, không có error output. Đã chép vào `Lab/kalman_fusion_lab_STUDENT.ipynb` và xác minh SHA-256 `398e576a72264aaaa77cede66bab0c95e7ef468698a02b894a9e1bc401241772`.
- `git diff --check` thành công. Git status: notebook đã sửa, `WORK_STATUS.md` chưa được track; chưa stage, commit hoặc push.

## Việc đang làm
- Không có việc code đang làm; chờ người dùng tự push.

## File đã sửa/tạo
- Tạo `WORK_STATUS.md`.
- Sửa `Lab/kalman_fusion_lab_STUDENT.ipynb` ở các TODO và bốn biến chẩn đoán; sau đó thay bằng bản Colab có output cùng source.

## Quyết định quan trọng
- Chỉ sửa phần code trong notebook học viên; bảo toàn cấu trúc, chữ ký hàm và thay đổi có sẵn.
- Không dùng `_reveal_truth`; chẩn đoán Phần 9 theo NIS và residual từ log công khai.
- Không viết báo cáo 20 điểm vì người dùng yêu cầu toàn bộ phần code; không tạo số liệu hay nhận xét chưa được chạy.
- Người dùng yêu cầu tự push; không stage, commit hoặc push thay người dùng.

## Lỗi/vấn đề còn tồn tại
- VS Code trước đó thiếu `matplotlib`; bản Colab hiện import thành công. Chưa xác minh kernel VS Code đã được cài gói.
- Python bundled của agent là 3.12.14, khác metadata notebook từng chạy bằng 3.11.7; cài vào Python bundled không đảm bảo sửa được kernel VS Code. Python bundled thiếu `matplotlib`, `scipy`, `nbformat`, `nbclient`, `ipykernel`.
- Bản local đã được thay bằng output chạy thành công từ Colab; output lỗi thiếu `matplotlib` cũ không còn.
- Báo cáo Phần 9 (20 điểm chấm tay) trên Colab vẫn là mẫu chưa điền. Colab hiện báo `Các thay đổi sẽ không được lưu` với tài khoản truy cập của agent; chưa xác minh quyền lưu của người dùng.
- Bản Colab tải xuống giữ output nhưng `execution_count` là `null` ở các cell code; đây là trạng thái xuất file Colab, chưa xác minh bằng trình chấm chính thức.

## Bước tiếp theo cần làm
- Nếu muốn điểm báo cáo 20, người dùng cần điền mục báo cáo Phần 9 theo output thực tế trước khi nộp.
- Người dùng tự kiểm tra `git status`, stage các file muốn nộp, commit và push lên `origin/main`.
