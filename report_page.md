# Báo cáo Lab 0 – CSC4005

**Họ tên:** Đặng Quốc AN 
**MSSV:** 1675020001  
**Lớp:** KHMT17-01

---

## 1. Thiết lập môi trường

Em sử dụng **Conda (Miniconda)** để tạo môi trường Python 3.10 cho học phần CSC4005.
Các bước thực hiện:

```bash
conda create -n csc4005 python=3.10 -y
conda activate csc4005
pip install -r requirements.txt
```

File `requirements.txt` bao gồm: NumPy, Pandas, Matplotlib, Scikit-learn, PyTorch, Torchvision, Torchaudio, PyYAML, tqdm, Jupyter.

## 2. Kiểm tra và chạy smoke-test

- **Bước 1:** Chạy `python check_env.py` — xác minh toàn bộ thư viện đã cài đặt đúng, kiểm tra phiên bản Python, PyTorch và thực hiện phép tính tensor cơ bản. Kết quả được lưu tại `outputs/logs/env_check.txt`.
- **Bước 2:** Chạy `python run_smoke_test.py` — pipeline hoàn chỉnh: tạo synthetic dataset (500 samples, 20 features), xây dựng SimpleMLP (20→32→2), training 3 epochs với Adam (lr=0.001, batch_size=32), lưu checkpoint và vẽ loss curve. Các file output sinh ra:
  - `outputs/logs/smoke_test_log.txt`
  - `outputs/figures/loss_curve.png`
  - `outputs/checkpoints/smoke_model.pt`

## 3. Vấn đề gặp phải

- **Lỗi:** Khi chạy `conda create -n csc4005 python=3.10` trên PowerShell, môi trường không khởi tạo được.
- **Cách xử lý:** Chuyển sang Anaconda Prompt và thực hiện lại lệnh, sau đó mở VS Code, chọn `Python: Select Interpreter` và chọn `csc4005-dl(3.10.20)`.

## 4. Kết quả

| Thông tin | Giá trị |
|-----------|---------|
| Hệ điều hành | Windows 11 |
| Python version | 3.10 |
| Torch version | _(xem outputs/logs/env_check.txt)_ |
| Thiết bị | CPU |
| Trạng thái | Thành công |
