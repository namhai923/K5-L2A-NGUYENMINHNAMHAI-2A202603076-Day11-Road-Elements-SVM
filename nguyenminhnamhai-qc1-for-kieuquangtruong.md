# Phiếu QC 1 — Road v1.0

Lô được kiểm (học viên): Kiều Quang Trường - 2A202603205        Người kiểm (học viên): Nguyễn Minh Nam Hải - 2A202603076
Ngày: 21/11/2026                          Phiên bản guideline: Road v1.0
File được kiểm (tên + `revision` trong manifest): `kieuquangtruong-front.zip`, `kieuquangtruong-fisheye.zip` · revision 5
Số ảnh kiểm: 20 (+ 8 ảnh thêm, ghi riêng)   Số nhãn đã kiểm (shape + tag): 377

## Tổng hợp theo mã
| Mã | Loại lỗi | Số mục kiểm | Số lỗi | Mức |
| --- | --- | ---: | --- | --- |
| QC1-01 tag camera | sai thuộc tính / bỏ sót | 112 tag | 0 lỗi cấu trúc phát hiện | nặng |
| QC1-02 đủ L1, R1 | bỏ sót | 16 ảnh front | A05 được miễn; A09 chờ xác nhận | nặng |
| QC1-03 position | sai thuộc tính / thừa | 65 lane | Chưa chốt kiểm tay | nặng |
| QC1-04 tâm vạch, chiều, điểm dừng | sai phạm vi / bỏ sót | 52 lane front kiểm chiều | 0 cảnh báo chiều; tâm vạch và điểm dừng chưa chốt | chính |
| QC1-05 vạch đứt, che | sai phạm vi / sai thuộc tính | 65 lane | 6 nhóm position trùng cần đối chiếu vạch đôi | chính |
| QC1-06 style, color, kind | sai thuộc tính | 65 lane | A04 L1 có single/double, chờ kiểm | chính |
| QC1-07 vùng lái | sai phạm vi / bỏ sót / thừa | 78 polygon kiểm cấu trúc | Chưa chốt kiểm tay | chính |
| QC1-08 đèn, màu | bỏ sót / sai phạm vi | 48 box đèn kiểm thuộc tính | Chưa chốt kiểm tay | nặng / chính |
| QC1-09 facing, type, group, biển phụ | sai thuộc tính | 86 box kiểm thuộc tính | Chưa chốt kiểm tay | chính |
| QC1-10 hình in, đủ biển | bỏ sót / sai phạm vi | 38 box biển kiểm cấu trúc | Chưa chốt kiểm tay | chính |
| QC1-11 fisheye | sai phạm vi / sai thuộc tính | 31 polyline | 3 road_curb B02 đã kiểm đúng; lane B04/B08 chờ kiểm | chính |
| QC1-12 file | lỗi file | 2 ZIP | 0 lỗi file phát hiện | nhẹ / nặng |

## Danh sách lỗi (mỗi lỗi một dòng)
| # | Mã | Ảnh | Nhãn (label, id) | Mức | Mô tả ngắn |
| --- | --- | --- | --- | --- | --- |
| — | — | — | — | — | Không có lỗi |

## Ca mơ hồ
| Ảnh | Câu hỏi cho lead | Lời đáp (nếu có) |
| --- | --- | --- |
| A05 | Lint báo QC1-02 thiếu L1; ảnh không thấy vạch sơn, có được miễn không? | Coach đã xác nhận không thấy vạch, miễn QC1-02 theo thông tin học viên |
| A09 | Lint báo QC1-02 thiếu R1; có thuộc ngoại lệ không thấy vạch không? | Chưa có xác nhận riêng cho bài Trường |
| A01, A04, A06, A09, A11, A14 | Position trùng có phải hai nét của vạch đôi không? | Học viên giải thích là vạch đôi; 5 cặp double/double, riêng A04 single/double cần đối chiếu |
| B02 | Ba road_curb tại (1001,515), (1190,659), (1056,552) chỉ có 2 điểm | Đã kiểm thực tế: đoạn ngắn bám đúng mép đường, giữ nguyên |
| B04, B08 | Lane 3 điểm có bám đúng cung trong ngưỡng 5 px không? | Chưa có xác nhận kiểm tay riêng |v

## Quyết định
Lỗi nặng: chưa chốt   Lỗi chính: chưa chốt / chưa có mẫu số kiểm tay   Lỗi nhẹ: chưa chốt   Ca chờ xác nhận: như bảng trên
Quyết định (Release / Hold / Rework): Chờ Nguyễn Minh Nam Hải xác nhận
Lý do (theo luật của phiếu): Output revision 5 có 13 cảnh báo, không tương đương 13 lỗi thật. A05 được coach xác nhận ngoại lệ; 3 road_curb B02 đã kiểm đúng. Cần chốt các ca còn mở trước khi tính tỉ lệ lỗi và ra quyết định. Không lấy 377 nhãn kiểm cấu trúc làm mẫu số lỗi hình học.

Loại lỗi: bỏ sót = thiếu nhãn phải có; thừa = gán cái không phải đối tượng; sai phạm vi = hình lệch, sai chiều, dừng sai chỗ, tràn vùng. Ba loại này theo cách chia lỗi gán nhãn của ISO/IEC 5259-4 (mục 8.4.2); "sai thuộc tính" và "lỗi file" là khóa học thêm. Cách xếp mức: [thang mức lỗi](../docs/qc_severity_road_v1.0.md).
