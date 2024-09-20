1. Link Figma my group:
   https://www.figma.com/design/sa3cveR7SSUzsdqFUZqM03/Figma-GUI-BookStore?node-id=1-734&node-type=canvas&t=WjRfpvcMs4xmfWrl-0
2. UseCase is written in WORD:
   Nhóm 1: Xây dựng app bán sách
21110255_Nguyễn Thành Nghiệp
21110185_Hồ Văn Huỳnh Hợp
21110149_Võ Thế Dân
Lược đồ Usecase (Usecase Diagram)
 
2. Mô tả chi tiết Usecase 

STT	Actor	Ý Nghĩa
1	Khách vãng lai	Người chỉ xem sản phẩm.
2	Khách hàng	Người xem và mua sản phẩm.
3	Quản lý	Người quản lý sản phẩm, đơn hàng, khách hàng và việc kinh doanh.

2.1. UC-1.1 Use case đăng ký tài khoản


Use Case ID	UC-1.1
Use Case Name	Đăng ký tài khoản.
Actors	Khách vãng lai.
Short Description	Cho phép Actors đăng ký tài khoản mới.
Pre-Conditions	Actors sở hữu một tài khoản email.
Post-Conditions	Actors đăng ký thành công tài khoản khách hàng.
Main Flow	1. Tại trang chủ, Actors nhấn vào lựa chọn là  “Đăng ký”.
2. Hệ thống chuyển hướng đến trang đăng ký tài khoản bao gồm nút "Đăng ký" và các trường thông tin trống:
- Thông tin bắt buộc:
+ Thông tin khách hàng: họ và tên, email, số điện thoại, địa chỉ.
+ Thông tin tài khoản: tên đăng nhập, mật khẩu, nhập lại mật khẩu.
3. Actors nhập các trường thông tin.
4. Actors nhấn nút "Đăng ký".
5. Hệ thống kiểm tra thông tin Actors nhập.
6. Thực hiện UC-1.4 (Xác nhận mã OTP).
7. Hệ thống hiển thị thông báo đăng ký thành công.
8. Hệ thống gửi mail thông báo đăng ký thành công và chào mừng tới email của Actors.
9. Hệ thống chuyển hướng đến trang chủ.
Alternative Flow	
Exception Flow	5.1. Một trong các trường thông tin bắt buộc bị bỏ trống thì hiển thị thông báo yêu cầu Actors nhập đầy đủ thông tin bắt buộc.
Quay lại bước 2.
5.2. Một trong các trường thông tin không đúng định dạng thì hiển thị thông báo yêu cầu nhập lại.
Quay lại bước 2.
5.3. Các thông tin: tên tài khoản, email hoặc số điện thoại đã tồn tại trong cơ sở dữ liệu thì hiển thị thông báo yêu cầu Actors nhập lại thông tin bị trùng.
Quay lại bước 2.
5.4. Mật khẩu và nhập lại mật khẩu không trùng khớp thì hiển thị thông báo yêu cầu Actors nhập lại mật khẩu.
Quay lại bước 2.
2.2. UC-1.2 Use case đăng nhập
Use Case ID	UC-1.2
Use Case Name	Đăng nhập.
Actors	Khách hàng, quản lý.
Short Description	Cho phép Actors đăng nhập vào website.
Pre-Conditions	Actors sở hữu tài khoản trong hệ thống.
Post-Conditions	Actors đăng nhập thành công vào website.
Main Flow	1. Tại trang chủ, Actors nhấn vào lựa chọn là “Đăng nhập”
2. Hệ thống chuyển hướng đến trang đăng nhập bao gồm nút "Đăng nhập", ô tích “Ghi nhớ tài khoản này”, … và các trường thông tin trống:
- Thông tin bắt buộc: tên đăng nhập, mật khẩu.
3. Actors nhập các trường thông tin.
4. Actors nhấn nút "Đăng nhập".
5. Hệ thống kiểm tra thông tin Actors nhập.
6. Hệ thống chuyển hướng Actors đến trang chủ.
Alternative Flow	3.1.1. Actors nhập các trường thông tin.
3.1.2. Actors tích vào ô “Ghi nhớ tài khoản này”.
Tiếp tục đến bước 4.
3.2.1. Actors nhấn nút “Quên mật khẩu”.
3.2.2. Thực hiện UC-1.3 (Quên mật khẩu).
Quay lại bước 1.
3.3.1. Actors nhấn nút “Đăng ký tài khoản mới”.
3.3.2. Thực hiện UC-1.1 (Đăng ký tài khoản).
Quay lại bước 1.
Exception Flow	5.1. Một trong các trường thông tin bắt buộc bị bỏ trống thì hiển thị thông báo yêu cầu Actors nhập đầy đủ thông tin bắt buộc.
Quay lại bước 2.
5.2. Một trong các trường thông tin không đúng định dạng thì hiển thị thông báo yêu cầu nhập lại.
Quay lại bước 2.
5.3. Tên đăng nhập hoặc mật khẩu không đúng thì hiển thị thông báo yêu cầu nhập lại tên đăng nhập hoặc mật khẩu.
Quay lại bước 2.
5.4. Tài khoản Actors đã bị khóa thì hiển thị thông báo tài khoản Actors đã bị khóa.
Quay lại bước 2.
2.3. UC-1.3 Use case quên mật khẩu

Use Case ID	UC-1.3
Use Case Name	Quên mật khẩu.
Actors	Khách hàng và quản lý.
Short Description	Cho phép Actors tạo mật khẩu mới khi quên mật khẩu.
Pre-Conditions	Actors sở hữu tài khoản trong hệ thống.
Post-Conditions	Actors tạo thành công mật khẩu mới.
Main Flow	1. Tại trang chủ, Actors nhấn vào lựa chọn là “Đăng nhập”
2. Hệ thống chuyển hướng đến trang đăng nhập có nút “Quên mật khẩu”.
3. Actors nhấn nút “Quên mật khẩu”
4. Hệ thống chuyển hướng đến trang quên mật khẩu bao gồm nút "Gửi mã" và trường thông tin trống:
- Thông tin bắt buộc: email.
5. Actors nhập trường thông tin.
6. Actors nhấn nút “Đặt lại mật khẩu”.
7. Hệ thống kiểm tra thông tin Actors vừa nhập.
8. Hệ thống gửi một đường dẫn chứa Token vào trong email
9. Actors truy cập hộp thư email để lấy truy cập vào đường dẫn.
10. Hệ thống chuyển hướng đến trang tạo mật khẩu mới bao gồm nút “Xác nhận” và các trường thông tin trống:
- Thông tin bắt buộc: mật khẩu mới, nhập lại mật khẩu mới.
11. Actors nhập các trường thông tin.
12. Actors nhấn nút "Xác nhận".
13. Hệ thống kiểm tra thông tin Actors nhập.
14. Thông báo tạo mật khẩu mới thành công.
15. Hệ thống điều hướng Actors đến trang đăng nhập.
Alternative Flow	
Exception Flow	6.1. Một trong các trường thông tin bắt buộc bị bỏ trống thì hiển thị thông báo yêu cầu Actors nhập đầy đủ thông tin bắt buộc.
Quay lại bước 4.
6.2. Một trong các trường thông tin không đúng định dạng thì hiển thị thông báo yêu cầu nhập lại.
Quay lại bước 4.
6.3. Thông tin email không tồn tại trong cơ sở dữ liệu thì hiển thị thông báo email không tồn tại.
Quay lại bước 4.
12.1. Mật khẩu mới và nhập lại mật khẩu mới không trùng khớp thì thông báo yêu cầu Actors nhập lại mật khẩu.
Quay lại bước 10.
2.4. UC-1.4 Use case xác nhận mã OTP

Use Case ID	UC-1.4
Use Case Name	Xác nhận mã OTP.
Actors	Khách vãng lai, khách hàng và quản lý.
Short Description	Cho phép xác nhận mã OTP để xác thực Actors.
Pre-Conditions	Actors đúng địa chỉ email của Actors.
Post-Conditions	Xác thực Actors thành công.
Main Flow	1. Hệ thống chuyển hướng đến trang xác nhận mã OTP bao gồm các nút “Gửi mã”, “Xác nhận” và các trường thông tin trống:
- Thông tin bắt buộc: mã OTP.
2. Actors nhấn nút “Gửi mã”.
3. Hệ thống gửi mã xác nhận OTP đến email của Actors.
4. Actors truy cập hộp thư email để lấy mã xác nhận OTP.
5. Người nhập các trường thông tin.
6. Actors nhấn nút “Xác nhận”.
7. Hệ thống kiểm tra thông tin Actors nhập.
8. Xác nhận mã OTP thành công.
Alternative Flow	
Exception Flow	4.1. Mã xác nhận OTP sẽ hết hiệu lực sau 5 phút nếu không được sử dụng.
Quay lại bước 2.
7.1. Một trong các trường thông tin bắt buộc bị bỏ trống thì hiển thị thông báo yêu cầu Actors nhập đầy đủ thông tin bắt buộc.
Quay lại bước 1 và bỏ qua bước 2, 3, 4 nếu OTP còn hiệu lực.
7.2. Mã OTP không đúng thì hiển thị thông báo mã OTP không chính xác.
Quay lại bước 1 và bỏ qua bước 2, 3, 4 nếu OTP còn hiệu lực.

2.5. UC-1.5 Use case đổi mật khẩu

Use Case ID	UC-1.5
Use Case Name	Đổi mật khẩu.
Actors	Khách hàng và quản lý.
Short Description	Cho phép Actors đổi mật khẩu mới cho tài khoản.
Pre-Conditions	Tài khoản Actors đã được đăng nhập thành công.
Post-Conditions	Actors đổi mật khẩu mới thành công.
Main Flow	1. Tại trang chủ, Actors nhấn vào biểu tượng tài khoản.
2. Hệ thống sổ ra 3 lựa chọn là “Thông tin tài khoản”, “Đổi mật khẩu” và “Đăng xuất”.
3. Actors nhấn vào nút “Đổi mật khẩu”.
4. Hệ thống chuyển hướng đến trang đổi mật mật khẩu bao gồm nút "Lưu mật khẩu" và các trường thông tin trống:
- Thông tin bắt buộc: mật khẩu hiện tại, mật khẩu mới, nhập lại mật khẩu mới.
5. Actors nhập các trường thông tin.
6. Actors ấn nút "Lưu mật khẩu".
7. Hệ thống kiểm tra thông tin Actors nhập.
8. Hệ thống thông báo đổi mật khẩu thành công.
9. Hệ thống điều hướng Actors đến trang chủ.
Alternative Flow	
Exception Flow	7.1. Một trong các trường thông tin bắt buộc bị bỏ trống thì hiển thị thông báo yêu cầu Actors nhập đầy đủ thông tin bắt buộc.
Quay lại bước 4.
7.2. Một trong các trường thông tin không đúng định dạng thì hiển thị thông báo yêu cầu nhập lại.
Quay lại bước 4.
7.3. Mật khẩu hiện tại không đúng thì hiện thông báo yêu cầu nhập lại mật khẩu hiện tại.
Quay lại bước 4.
7.4. Mật khẩu mới và nhập lại mật khẩu mới không trùng khớp thì thông báo yêu cầu Actors nhập lại mật khẩu mới.
Quay lại bước 4.
2.6. UC-1.6 Use case thay đổi thông tin tài khoản

Use Case ID	UC-1.6
Use Case Name	Thay đổi thông tin tài khoản.
Actors	Khách hàng và quản lý.
Short Description	Cho phép Actors thay đổi thông tin tài khoản.
Pre-Conditions	Tài khoản Actors đã được đăng nhập thành công.
Post-Conditions	Actors thay đổi thông tin tài khoản thành công.
Main Flow	1. Tại trang chủ, Actors nhấn vào biểu tượng tài khoản.
2. Hệ thống sổ ra 3 lựa chọn là “Thông tin tài khoản”, “Đổi mật khẩu” và “Đăng xuất”.
3. Actors nhấn vào nút “Thông tin tài khoản”.
4. Hệ thống chuyển hướng đến trang thông tin tài khoản bao gồm các nút “Chỉnh sửa”, “Lưu thông tin” và các trường thông tin bị khóa: 
- Thông tin bắt buộc:họ và tên, địa chỉ, email, số điện thoại.
5. Actors nhấn nút “Chỉnh sửa” thì các trường (trừ email) sẽ mở khóa cho phép chỉnh sửa.
6. Actors chỉnh sửa các trường thông tin.
7. Actors ấn nút "Lưu thông tin".
8. Hệ thống kiểm tra thông tin Actors chỉnh sửa.
9. Hệ thống hiển thị thông báo thay đổi thông tin thành công.
10. Hệ thống điều hướng Actors đến trang chủ.
Alternative Flow	 
Exception Flow	9.1. Một trong các trường thông tin bắt buộc bị bỏ trống thì hiển thị thông báo yêu cầu Actors nhập đầy đủ thông tin bắt buộc.
Quay lại bước 4.
9.2. Một trong các trường thông tin không đúng định dạng thì hiển thị thông báo yêu cầu nhập lại.
Quay lại bước 4.
2.7. UC-1.7 Use case đăng xuất
Use Case ID	UC-1.7
Use Case Name	Đăng xuất.
Actors	Khách hàng, quản lý.
Short Description	Cho phép Actors đăng xuất khỏi website.
Pre-Conditions	Tài khoản Actors đã được đăng nhập thành công.
Post-Conditions	Actors đăng xuất khỏi thành công khỏi website
Main Flow	1. Tại trang chủ, Actors nhấn vào biểu tượng tài khoản.
2. Hệ thống sổ ra 3 lựa chọn là “Thông tin tài khoản”, “Đổi mật khẩu” và “Đăng xuất”.
3. Actors nhấn vào nút “Đăng xuất”.
4. Hệ thống tiến hành đăng xuất tài khoản khỏi hệ thống.
5. Hệ thống thông báo đăng xuất thành công.
6. Hệ thống điều hướng Actors đến trang chủ.
Alternative Flow	
Exception Flow	
3.2.8. UC-1.8 Use case lọc sản phẩm
Use Case ID	UC-1.8
Use Case Name	Lọc sản phẩm.
Actors	Khách vãng lai và khách hàng.
Short Description	Cho phép Actors lọc danh sách sản phẩm.
Pre-Conditions	Không có
Post-Conditions	Actors lọc thành công được danh sách sản phẩm.
Main Flow	1. Tại trang chủ, Actors nhấn vào tên danh mục cần lọc ở menu trái của trang chủ.
2. Hệ thống hiển thị danh sách sản phẩm theo danh mục đã chọn.
Alternative Flow	
Exception Flow	

2.9. UC-1.9 Use case tìm kiếm sản phẩm
Use Case ID	UC-1.9
Use Case Name	Tìm kiếm sản phẩm.
Actors	Khách vãng lai và khách hàng.
Short Description	Cho phép Actors tìm kiếm được sản phẩm mong muốn.
Pre-Conditions	
Post-Conditions	Actors tìm được sản phẩm như mong muốn.
Main Flow	1. Actors nhấn vào ô tìm kiếm sản phẩm ở phần đầu trang.
2. Actors nhập tên sản phẩm vào ô tìm kiếm.
3. Actors nhấn nút “Tìm”.
4. Hệ thống hiển thị danh sách các sản phẩm tìm thấy theo yêu cầu tại phần sản phẩm.
Alternative Flow	
Exception Flow	4.1. Hệ thống không tìm thấy sản phẩm nào theo yêu cầu thì hiển thị thông báo “Không tìm thấy sản phẩm nào”.
Quay lại bước 1.

3.2.10. UC-1.10 Use case xem danh sách sản phẩm
Use Case ID	UC-1.10
Use Case Name	Xem danh sách sản phẩm.
Actors	Khách vãng lai và khách hàng.
Short Description	Cho phép Actors xem được danh sách sản phẩm.
Pre-Conditions	
Post-Conditions	Actors xem danh sách sản phẩm thành công.
Main Flow	1. Actors nhấn nút “Trang chủ” ở phần đầu trang.
2. Hệ thống chuyển hướng đến trang chủ bao gồm phần danh sách sản phẩm.
Alternative Flow	
Exception Flow	
2.11. UC-1.11 Use case thêm sản phẩm vào giỏ hàng
Use Case ID	UC-1.11
Use Case Name	Thêm sản phẩm vào giỏ hàng.
Actors	Khách hàng.
Short Description	Cho phép Actors thêm sản phẩm vào giỏ hàng.
Pre-Conditions	Tài khoản Actors đã được đăng nhập thành công.
Trên trang chi tiết sản phẩm hoặc trang danh sách sản phẩm hiển thị được sản phẩm
Post-Conditions	Actors thêm sản phẩm với số lượng mong muốn vào giỏ hàng thành công.
Main Flow	1. Thực hiện UC-1.10 (Xem danh sách sản phẩm).
2. Actors nhấn vào hình ảnh của sản phẩm muốn thêm vào giỏ hàng.
3. Hệ thống chuyển hướng Actors đến trang chi tiết sản phẩm gồm hình ảnh, mô tả, giá cả, lựa chọn số lượng và đánh giá sản phẩm.
4. Actors thực hiện thêm sản phẩm vào giỏ hàng.
5. Hiển thị thông báo hệ thống sản phẩm đã được thêm thành công vào giỏ hàng.
Alternative Flow	2.1. Actors nhấn vào tên sản phẩm ở dưới hình ảnh của sản phẩm muốn thêm vào giỏ hàng.
Tiếp tục bước 3.
5.1. Sản phẩm đã có trong giỏ hàng, hệ thống tăng số lượng sản phẩm vừa thêm lên một.
5.2. Actors có thể chọn tiếp tục mua hàng hoặc đến giỏ hàng để chỉnh sửa, thanh toán.
Exception Flow	Nếu Actors chưa đăng nhập, hệ thống sẽ yêu cầu đăng nhập trước khi thực hiện việc để sản phẩm được thêm vào giỏ hàng.
Nếu xảy ra lỗi, hệ thống sẽ hiển thị thông báo lỗi và yêu cầu người dùng thử lại sau.

2.12. UC-1.12 Use case quản lý giỏ hàng
Use Case ID	UC-1.12
Use Case Name	Quản lý giỏ hàng.
Actors	Khách hàng.
Short Description	Cho phép Actors cập nhật số lượng sản phẩm mong muốn và xóa các sản phẩm không muốn mua.
Pre-Conditions	Tài khoản Actors đã được đăng nhập thành công.
Sản phẩm đã được thêm vào giỏ hàng.
Post-Conditions	Actors quản lý giỏ hàng thành công.
Main Flow	1. Actors nhấn vào nút “Giỏ hàng” ở phần đầu trang.
2. Hệ thống chuyển hướng Actors đến trang giỏ hàng. Hệ thống chuyển hướng Actors đến trang chi tiết sản phẩm gồm hình ảnh, mô tả, giá cả, lựa chọn số lượng và đánh giá sản phẩm. 
3. Actors thực hiện các thay đổi trên giỏ hàng như:
A. Cập nhật số lượng sản phẩm:
A1. Thực hiện tăng hoặc giảm số lượng
-	Nhấn nút “+” bên cạnh số lượng sản phẩm để điều chỉnh tăng số lượng sản phẩm.
-	Nhấn nút “-” bên cạnh số lượng sản phẩm để điều chỉnh giảm số lượng sản phẩm.
A2. Hệ thống sẽ tự động cập nhật những thay đổi và tổng giá tiền của các sản phẩm sau mỗi lần thay đổi.
B. Xóa sản phẩm:
B1. Actors nhấn nút “x” ở cuối mục sản phẩm muốn xóa.
B2. Hệ thống hiển thị thông báo xác nhận xóa. Actors xác nhận muốn xóa thì chọn “Yes”.
B3.Hệ thống sẽ tự động cập nhật giỏ hàng và hiển thị thông báo xóa sản phẩm khỏi giỏ hàng thành công.
Alternative Flow	
Exception Flow	Nếu xảy ra lỗi, hệ thống sẽ hiển thị thông báo có lỗi và yêu cầu người dùng thử lại sau.
2.13. UC-1.13 Use case đặt hàng
Use Case ID	UC-1.13
Use Case Name	Đặt hàng.
Actors	Khách hàng.
Short Description	Cho phép Actors đặt hàng.
Pre-Conditions	Tài khoản Actors đã được đăng nhập thành công.
Sản phẩm đã được thêm vào giỏ hàng.
Post-Conditions	Actors đặt hàng thành công, đơn hàng được tạo và ghi nhận trong hệ thống.
Actors nhận thông báo xác nhận đơn hàng, thông tin chi tiết của đơn hàng.
Main Flow	1. Actors nhấn vào nút “Giỏ hàng” ở phần đầu trang.
2. Hệ thống chuyển hướng Actors đến trang giỏ hàng.
3. Hệ thống hiển thị danh sách các sản phẩm có trong giỏ hàng gồm các tiêu chí như tên sản phẩm, số lượng, giá .
4. Actors chọn các sản phẩm muốn mua trong giỏ hàng và nhấn vào nút "Tiến hành thanh toán".
5. Hệ thống chuyển hướng đến trang thanh toán bao gồm nút “Đặt hàng” và các trường thông tin: 
- Thông tin bắt buộc: địa chỉ giao hàng, phương thức thanh toán, phương thức vận chuyển.
6. Actors nhập các trường thông tin.
7. Actors chọn một trong các  phương thức thanh toán (tiền mặt, PayPal) và  ấn vào nút “Đặt hàng”.
8. Hệ thống kiểm tra thông tin đơn hàng.
9. Hệ thống hiển thị thông báo Actors đặt hàng thành công, sau đó chuyển hướng người dùng đến trang danh sách sản phẩm để người dùng có thể tiếp tục mua sắm.
Alternative Flow	Thanh toán qua PayPal
1.	Actors được chuyển hướng đến trang của PayPal để hoàn thành thanh toán.
2.	Nếu thanh toán thành công, hệ thống sẽ cập nhật trạng thái đơn hàng là đã thanh toán, sau đó gửi thông tin cho đơn vị vận chuyển.
Exception Flow	7.1. Một trong các trường thông tin bắt buộc bị bỏ trống thì hiển thị thông báo yêu cầu Actors nhập đầy đủ thông tin bắt buộc.
Quay lại bước 5.
7.2. Một trong các trường thông tin không đúng định dạng thì hiển thị thông báo yêu cầu nhập lại.
Quay lại bước 5.
7.3. Nếu thanh toán bằng PayPal thất bại, hệ thống sẽ cập nhật trạng thái đơn hàng là chờ thanh toán, trong 24h, người dùng sẽ phải thanh toán lại nếu không muốn đơn hàng bị hủy.
2.14. UC-1.14 Use case xem thông tin đơn hàng
Use Case ID	UC-1.14
Use Case Name	Xem thông tin đơn hàng.
Actors	Khách hàng.
Short Description	Cho phép Actors xem thông tin các đơn hàng.
Pre-Conditions	Tài khoản Actors đã được đăng nhập thành công.
Post-Conditions	Actors xem được thông tin các đơn hàng.
Main Flow	1. Actors nhấn vào nút “Đơn hàng” ở phần đầu trang.
2. Hệ thống chuyển hướng Actors đến trang đơn hàng.
3. Actors nhấn vào nút “Chi tiết” ở phần hành động của dòng đơn hàng muốn xem thông tin.
4. Hệ thống chuyển hướng đến trang thông tin đơn hàng.
Alternative Flow	
Exception Flow	2.1. Actors chưa có đơn hàng nào thì hiển thị “Không có đơn hàng nào”.
Kết thúc UC-1.14.
2.15. UC-1.15 Use case quản lý danh mục
Use Case ID	UC-1.15
Use Case Name	Quản lý danh mục.
Actors	Nhân viên, quản lý.
Short Description	Cho phép Actors quản lý các danh mục sản phẩm.
Pre-Conditions	Tài khoản Actors đã được đăng nhập thành công.
Post-Conditions	Actors quản lý danh mục sản phẩm thành công.
Main Flow	1. Nhấn nút “Quản lý danh mục” ở menu trái của trang quản lý.
2. Hệ thống chuyển hướng đến trang quản lý danh mục.
Actors có thể chọn các chức năng sau:
A. Thêm danh mục:
A1. Actors nhấn nút “Thêm danh mục mới”.
A2. Hệ thống chuyển hướng đến trang thêm danh mục bao gồm nút "Xác nhận" và các trường thông tin trống:
- Thông tin bắt buộc: tên danh mục.
A3. Actors nhập các trường thông tin. 
A4. Actors nhấn nút “Xác nhận”.
A5. Hệ thống kiểm tra thông tin Actors nhập.
A6. Hệ thống hiển thị thông báo thêm danh mục thành công.

B. Sửa danh mục:
B1. Actors nhấn vào biểu tượng chỉnh sửa ở phần hành động.
B2. Hệ thống chuyển hướng đến trang chỉnh sửa danh mục bao gồm nút "Xác nhận" và các trường thông tin:
- Thông tin chỉ được xem: mã danh mục.
- Thông tin bắt buộc có thể chỉnh sửa: tên danh mục.
B3. Actors chỉnh sửa các trường thông tin.
B4. Actors nhấn nút “Xác nhận”.
B5. Hệ thống kiểm tra thông tin Actors chỉnh sửa.
B6. Hệ thống hiển thị thông báo chỉnh sửa thành công.

C. Xóa danh mục:
C1. Actors nhấn vào biểu tượng xóa ở phần hành động.
C2. Hệ thống hiển thị thông báo hỏi Actors có chắc muốn xóa danh mục “mã danh mục - tên danh mục” không.
C3. Actors nhấn nút “Ok”.
C4. Hệ thống xóa danh mục khỏi hệ thống.
C5. Hệ thống hiển thị thông báo xóa thành công.
Alternative Flow	C3.1. Actors nhấn nút “Cancel” để hủy yêu cầu xóa danh mục.
Quay lại bước 2.
Exception Flow	A5.1. Một trong các trường thông tin bắt buộc bị bỏ trống thì hiển thị thông báo yêu cầu Actors nhập đầy đủ thông tin bắt buộc.
Quay lại bước A2.
B5.1. Một trong các trường thông tin bắt buộc bị bỏ trống thì hiển thị thông báo yêu cầu Actors nhập đầy đủ thông tin bắt buộc.
Quay lại bước B2.
B5.1. Một trong các trường thông tin bắt buộc đã tồn tại thì thông báo thông tin đã tồn tại và yêu cầu nhập lại.
Quay lại bước B2.
2.16. UC-1.16 Use case quản lý sản phẩm
Use Case ID	UC-1.16
Use Case Name	Quản lý sản phẩm.
Actors	Nhân viên, quản lý.
Short Description	Cho phép Actors quản lý các sản phẩm.
Pre-Conditions	Tài khoản Actors đã được đăng nhập thành công.
Post-Conditions	Actors thực hiện thêm, xóa, sửa sản phẩm thành công.
Main Flow	1. Nhấn nút “Quản lý sản phẩm” ở menu trái của trang quản lý.
2. Hệ thống chuyển hướng đến trang quản lý sản phẩm.
Có thể chọn các chức năng sau:
A. Thêm sản phẩm:
A1. Actors nhấn nút “Thêm sản phẩm mới”.
A2. Hệ thống chuyển hướng đến trang thêm sản phẩm bao gồm nút “Thêm ảnh”, "Xác nhận" và các trường thông tin:
- Thông tin bắt buộc: tên sản phẩm, giá, mô tả, danh mục, hình ảnh…
A3. Actors nhập các trường thông tin.
A4. Actors nhấn nút “Tạo sản phẩm mới” để thực hiện việc thêm sản phẩm.
A6. Hệ thống kiểm tra thông tin Actors nhập.
A7. Hệ thống hiển thị thông báo thêm thành công và quay lại danh sách sản phẩm.

B. Sửa sản phẩm:
B1. Actors chọn sản phẩm cần sửa ở danh sách sản phẩm và nhấn vào biểu tượng chỉnh sửa ở bên cạnh mỗi sản phẩm.
B2. Hệ thống chuyển hướng đến trang chứa thông tin sản phẩm cho phép actors chỉnh sửa, gồm các trường thông tin:
- Thông tin chỉ được xem: mã sản phẩm.
- Thông tin bắt buộc và được chỉnh sửa: tên sản phẩm, giá, mô tả danh mục, hình ảnh.
B3. Actors chỉnh sửa các trường thông tin.
B4. Actors nhấn nút “Cập nhật sản phẩm” để cập nhật các thông tin thay đổi.
B6. Hệ thống kiểm tra thông tin Actors nhập.
B7. Hệ thống hiển thị thông báo chỉnh sửa thành công và quay lại danh sách sản phẩm.

C. Xóa sản phẩm:
C1. Actors chọn sản phẩm cần xóa ở danh sách sản phẩm và nhấn vào biểu tượng xóa ở bên cạnh mỗi sản phẩm.
C2. Hệ thống hiển thị thông báo hỏi Actors về việc xác nhận xóa sản phẩm. 
C3. Actors nhấn nút “Ok”.
C4. Hệ thống xóa sản phẩm khỏi hệ thống.
C5. Hệ thống hiển thị thông báo xóa thành công và cập nhật lại danh sách sản phẩm.
Alternative Flow	A4.1. Actors muốn hủy bỏ quá trình thêm sản phẩm thì có thể nhấn vào “Quản lý sản phẩm” và quay lại trang giao diện quản trị.
B4.1.Actors nếu muốn hủy bỏ việc chỉnh sửa sản phẩm thì nhấn nút “Trở về”. Hệ thống sẽ không chỉnh sửa thông tin sản phẩm và quay lại trang danh sách sản phẩm.
C3.1. Actors nhấn nút “Cancel” để hủy yêu cầu xóa sản phẩm.
Quay lại bước 2.
Exception Flow	A6.1. Một trong các trường thông tin bắt buộc bị bỏ trống thì hiển thị thông báo yêu cầu Actors nhập đầy đủ thông tin bắt buộc.
Quay lại bước A2.
B6.1. Một trong các trường thông tin bắt buộc bị bỏ trống thì hiển thị thông báo yêu cầu Actors nhập đầy đủ thông tin bắt buộc.
Quay lại bước B2.
Nếu có lỗi kỹ thuật hoặc hệ thống, hệ thống hiển thị thông báo lỗi và yêu cầu người dùng thử lại sau.
2.17. UC-1.17 Use case quản lý đơn hàng
Use Case ID	UC-1.17
Use Case Name	Quản lý đơn hàng.
Actors	Nhân viên, quản lý.
Short Description	Cho phép Actors quản lý các đơn hàng.
Pre-Conditions	Tài khoản Actors đã được đăng nhập thành công vào tài khoản admin.
Đơn hàng đã được tạo và lưu trong hệ thống.
Post-Conditions	Actors quản lý đơn hàng thành công.
Main Flow	1. Nhấn nút “Quản lý đơn hàng” ở menu trái của trang quản lý.
2. Hệ thống chuyển hướng đến trang quản lý đơn hàng và hiển thị danh sách các đơn hàng.
Có thể chọn các chức năng sau:
A. Xem chi tiết đơn hàng:
A1. Actors nhấn vào biểu tượng xem chi tiết của đơn hàng muốn xem.
A2. Hệ thống chuyển hướng đến trang chi tiết đơn hàng bao gồm các trường thông tin chi tiết của đơn hàng.

B. Xác nhận đơn hàng:
B1. Actors chọn đơn hàng cần xác nhận, kiểm tra thông tin và nhấn vào biểu tượng xác nhận đơn hàng.
B2. Hệ thống hiển thị thông báo hỏi Actors để xác nhận đơn hàng
B3. Actors nhấn nút “Ok”.
B4. Hệ thống cập nhật trạng thái đơn hàng.
B5. Gửi email thông báo đơn hàng đã được xác nhận cho khách hàng.
B6. Hệ thống hiển thị thông báo cập nhật đơn hàng thành công.
Alternative Flow	B3.1. Actors nhấn nút “Cancel” để hủy yêu cầu xác nhận đơn hàng.
Quay lại bước 2.
Exception Flow	
2.18. UC-1.18 Use case quản lý khách hàng
Use Case ID	UC-1.18
Use Case Name	Quản lý khách hàng.
Actors	Quản lý.
Short Description	Cho phép Actors quản lý khách hàng.
Pre-Conditions	Tài khoản Actors đã được đăng nhập thành công.
Post-Conditions	Actors quản lý các tài khoản, thông tin khách hàng thành công.
Main Flow	1. Nhấn nút “Quản lý khách hàng” ở menu trái của trang quản lý.
2. Hệ thống chuyển hướng đến trang quản lý khách hàng.
Có thể chọn các chức năng sau:
A. Xem thông tin khách hàng:
A1. Actors nhấn vào biểu tượng xem chi tiết  của khách hàng muốn xem.
A2. Hệ thống chuyển hướng đến trang chi tiết khách hàng bao gồm các trường thông tin chi tiết của khách hàng đó. 

B. Khoá tài khoản khách hàng:
B1. Actors nhấn vào biểu tượng khóa tài khoản ở phần hành động của khách hàng muốn khóa.
B2. Hệ thống hiển thị thông báo hỏi Actors có chắc muốn khóa tài khoản khách hàng “mã khách hàng - email khách hàng” không.
B3. Actors nhấn nút “Ok”.
B4. Hệ thống khóa tài khoản của khách hàng tương ứng.
B5. Hệ thống hiển thị thông báo khóa tài khoản khách hàng “mã khách hàng - email khách hàng” thành công.

C. Tra cứu tài khoản khách hàng:
C1. Actors nhập tên người dùng muốn tìm vào thanh tìm kiếm.
C2. Hệ thống sẽ tìm kiếm và hiển thị kết quả tra cứu là thông tin chi tiết về khách hàng đó.
Alternative Flow	B3.1. Actors nhấn nút “Cancel” để hủy yêu cầu khóa tài khoản khách hàng.
Quay lại bước 2.
C2.1. Với yêu cầu tra cứu, nếu không có kết quả phù hợp, hệ thống sẽ hiển thị bảng trống.
Exception Flow	Nếu có lỗi xảy ra, hệ thống sẽ hiển thị thông báo lỗi và yêu cầu người dùng thử lại sau.


