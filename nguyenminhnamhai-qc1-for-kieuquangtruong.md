# Phiếu QC 1 — Road v1.0

Lô được kiểm (học viên): Kiều Quang Trường - 2A202603205        Người kiểm (học viên): Nguyễn Minh Nam Hải - 2A202603076
Ngày: 20/11/2026                          Phiên bản guideline: Road v1.0
File được kiểm (tên + `revision` trong manifest): `kieuquangtruong-front.zip`, `kieuquangtruong-fisheye.zip` · revision 2
Số ảnh kiểm: 6 (+ 0 ảnh thêm, ghi riêng)   Số nhãn đã kiểm (shape + tag): 65

## Tổng hợp theo mã
| Mã | Loại lỗi | Số mục kiểm | Số lỗi | Mức |
| --- | --- | ---: | ---: | --- |
| QC1-01 tag camera | sai thuộc tính / bỏ sót |  | 0 | nặng |
| QC1-02 đủ L1, R1 | bỏ sót |  | 0 (3 cảnh báo lint được miễn) | nặng |
| QC1-03 position | sai thuộc tính / thừa |  | 0 | nặng |
| QC1-04 tâm vạch, chiều, điểm dừng | sai phạm vi / bỏ sót |  | 0 | chính |
| QC1-05 vạch đứt, che | sai phạm vi / sai thuộc tính |  | 0 | chính |
| QC1-06 style, color, kind | sai thuộc tính |  | 0 | chính |
| QC1-07 vùng lái | sai phạm vi / bỏ sót / thừa |  | 0 | chính |
| QC1-08 đèn, màu | bỏ sót / sai phạm vi / sai thuộc tính |  | 0 | nặng / chính |
| QC1-09 facing, type, group, biển phụ | sai thuộc tính |  | 0 | chính |
| QC1-10 hình in, đủ biển | bỏ sót / sai phạm vi |  | 0 | chính |
| QC1-11 fisheye | sai phạm vi / sai thuộc tính |  | 0 | chính |
| QC1-12 file | lỗi file |  | 0 | nhẹ / nặng |

## Danh sách lỗi (mỗi lỗi một dòng)
| # | Mã | Ảnh | Nhãn (label, id) | Mức | Mô tả ngắn |
| --- | --- | --- | --- | --- | --- |
| — | — | — | — | — | Không có lỗi |

## Ca mơ hồ
| Ảnh | Câu hỏi cho lead | Lời đáp (nếu có) |
| --- | --- | --- |
| A05 | Lint báo QC1-02 thiếu L1 và R1. Hai bên làn không thấy vạch sơn; có được miễn không? | Coach xác nhận không thấy vạch, miễn QC1-02 |
| A09 | Lint báo QC1-02 thiếu R1. Bên phải là vỉa hè, đã vẽ `road_curb`; có được miễn không? | Coach xác nhận không thấy vạch, miễn QC1-02 |

## Quyết định
Lỗi nặng: 0   Lỗi chính: 0 / 65 nhãn = 0 %   Lỗi nhẹ: 0   Ca chờ lead: 0
Quyết định (Release / Hold / Rework): Release
Lý do (theo luật của phiếu): Không có lỗi nặng. Lỗi chính 0 %, dưới ngưỡng 5 %. QC1-02 ở A05 và A09 là ca coach đã xác nhận không thấy vạch, nên được miễn.

Loại lỗi: bỏ sót = thiếu nhãn phải có; thừa = gán cái không phải đối tượng; sai phạm vi = hình lệch, sai chiều, dừng sai chỗ, tràn vùng. Ba loại này theo cách chia lỗi gán nhãn của ISO/IEC 5259-4 (mục 8.4.2); "sai thuộc tính" và "lỗi file" là khóa học thêm. Cách xếp mức: [thang mức lỗi](docs/qc_severity_road_v1.0.md).
