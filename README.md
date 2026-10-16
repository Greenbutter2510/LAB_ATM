# NHOM6V2 — Labtainer

Bản nhom6v2 sửa metadata Docker Hub cho bài WAN–DMZ–LAN2. Giữ nguyên nhom6v1; gói cài nhom6v2 **phải dùng bản r4** (gói v2 đầu tiên lỗi checkwork).

```bash
imodule https://github.com/Greenbutter2510/LAB_ATM/releases/download/nhom6v2-2026-10-16/nhom6v2-imodule-2026-10-16-r4.tar.gz
labtainer nhom6v2
```

[Release nhom6v2 và SHA-256](https://github.com/Greenbutter2510/LAB_ATM/releases/tag/nhom6v2-2026-10-16). Labtainer tải 8 image `greenbutter2510/nhom6v2.<role>.student` từ Docker Hub; tài liệu tiếng Việt nằm trong `nhom6v2/docs/`. Trên VM nguồn, baseline CLO2 Y/Y và sau khi nhập luật CLO3 theo hướng dẫn, checkwork đạt 6 Y; chưa xác minh trên VM thứ hai sạch.

---

## Bản nhom6v1 (lưu trữ)

Bài lab phân đoạn WAN–DMZ–LAN2: quan sát baseline CLO2, sau đó người học tự cấu hình `iptables` cho CLO3. Bài gồm tám container; Docker image được lưu công khai trong namespace [`greenbutter2510`](https://hub.docker.com/u/greenbutter2510).

## Cài trên máy Labtainer VM

```bash
imodule https://github.com/Greenbutter2510/LAB_ATM/releases/download/nhom6v1-2026-10-14/nhom6v1-imodule-2026-10-14-rc1.tar.gz
labtainer nhom6v1
```

Gói `imodule` cung cấp cấu hình, grader và tài liệu; Labtainer tải tám image `greenbutter2510/nhom6v1.<role>.student:latest` từ Docker Hub. Nếu đang có `nhom6v1` riêng trên máy, sao lưu trước khi cài vì `imodule` giải nén vào thư mục labs. Trước khi cài, có thể tải tệp checksum trong cùng release để đối chiếu SHA-256.

Xem `nhom6v1/docs/HUONG_DAN_THUC_HANH_NHOM6V1_VI.pdf` để làm thủ công và dùng probe Python trên đúng terminal. Bài chỉ sử dụng môi trường Docker của Labtainer; không áp dụng các lệnh kiểm tra mạng vào máy chủ/mạng ngoài lab.
