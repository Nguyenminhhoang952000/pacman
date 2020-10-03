# pacman
Bài 1-->4: Tìm kiếm đường đi tối giữa 2 điểm 
Bài 5-->6: 
Bài 1:
+ Depth First Search là một thuật toán duyệt hoặc tìm kiếm một phần tử trên một cấu trúc dữ liệu dạng cây hay một đồ thị.

+ Bắt đầu đi từ một đỉnh của cây, sau đó từ đỉnh đó tìm ra node đầu tiên và cứ tìm các note tiếp theo

cho đến khi không đi được nữa, thì lại quay về node trước đó và tìm sang node bên cạnh để đi tiếp.

Giải thuật tìm kiếm theo chiều sâu (Depth First Search – viết tắt là DFS), còn được gọi là giải thuật tìm kiếm ưu tiên chiều sâu, là giải thuật duyệt hoặc tìm kiếm trên một cây hoặc một đồ thị và sử dụng stack (ngăn xếp) để ghi nhớ đỉnh liền kề để bắt đầu việc tìm kiếm khi không gặp được đỉnh liền kề trong bất kỳ vòng lặp nào. Giải thuật tiếp tục cho tới khi gặp được đỉnh cần tìm hoặc tới một nút không có con. Khi đó giải thuật quay lui về đỉnh vừa mới tìm kiếm ở bước trước.

Qui tắc 1: Duyệt tiếp tới đỉnh liền kề mà chưa được duyệt. Đánh dấu đỉnh mà đã được duyệt. Hiển thị đỉnh đó và đẩy vào trong một ngăn xếp (stack).

Qui tắc 2: Nếu không tìm thấy đỉnh liền kề, thì lấy một đỉnh từ trong ngăn xếp (thao tác pop up). (Giải thuật sẽ lấy tất cả các đỉnh từ trong ngăn xếp mà không có các đỉnh liền kề nào)

Qui tắc 3: Lặp lại các qui tắc 1 và qui tắc 2 cho tới khi ngăn xếp là trống.


Bài 2:

Giải thuật tìm kiếm theo chiều rộng (Breadth First Search – viết tắt là BFS) duyệt qua một đồ thị theo chiều rộng và sử dụng hàng đợi (queue) để ghi nhớ đỉnh liền kề để bắt đầu việc tìm kiếm khi không gặp được đỉnh liền kề trong bất kỳ vòng lặp nào.

Qui tắc 1: Duyệt tiếp tới đỉnh liền kề mà chưa được duyệt. Đánh dấu đỉnh mà đã được duyệt. Hiển thị đỉnh đó và đẩy vào trong một hàng đợi (queue)..

Qui tắc 2: Nếu không tìm thấy đỉnh liền kề, thì xóa đỉnh đầu tiên trong hàng đợi.

Qui tắc 3: Lặp lại Qui tắc 1 và 2 cho tới khi hàng đợi là trống.

Xét duyệt tất cả các đỉnh để trả về kết quả.
Nếu số đỉnh là hữu hạn, thuật toán chắc chắn tìm ra kết quả.
Khuyết điểm
Mang tính chất vét cạn, không nên áp dụng nếu duyệt số đỉnh quá lớn.
Mang tính chất mù quáng, duyệt tất cả đỉnh, không chú ý đến thông tin trong các đỉnh để duyệt hiệu quả, dẫn đến duyệt qua các đỉnh không cần thiết.

Bài 3:
Định nghĩa: Hàng đợi ưu tiên PQ là cấu trúc dữ liệu lưu trữ các phần tử cùng với độ ưu tiên của nó và khi lấy phần tử ra khỏi hàng đợi sẽ căn cứ vào độ ưu tiên nhỏ nhất.

Cho một trạng thái n, ký hiệu g(n) là tổng chi phí đường đi ngắn nhất (hiện có) từ trạng thái ban đầu S đến trạng thái n. Thuật toán UCS sử dụng một hàng đợi ưu tiên (Priority Queue – PQ) để lưu trữ và duyệt các trạng thái trên đường đi. Thuật toán dùng thêm một danh sách CLOSE để lưu trữ các trạng thái đã được xét.

 thuật toán tìm kiếm với chi phí cực tiểu (UCS) là một cách duyệt cây dùng cho việc duyệt hay tìm kiếm trên cây có trọng lượng chi phí. Thuật toán sẽ phát triển các nút chưa xét có chi phí thấp nhất – các nút được xét theo thứ tự chi phí tăng dần.Khi đồ thi có chi phí ở mỗi bước là như nhau thì thuật toán trở thành phương pháp tìm kiếm theo chiều rông.
 Bài 4:
 Heuristic và hàm Heuristic là gì?
Heuristic là phương pháp giải quyết vấn đề dựa trên phỏng đoán, ước chừng, kinh nghiệm, trực giác để tìm ra giải pháp gần như là tốt nhất và nhanh chóng.

Hàm Heuristic là hàm ứng với mỗi trạng thái hay mỗi sự lựa chọn một giá trị ý nghĩa đối với vấn đề dựa vào giá trị hàm này ta lựa chọn hành động.

A* là gì?
A* là giải thuật tìm kiếm trong đồ thị, tìm đường đi từ một đỉnh hiện tại đến đỉnh đích có sử dụng hàm để ước lượng khoảng cách hay còn gọi là hàm Heuristic.


A* lưu giữ một tập các lời giải chưa hoàn chỉnh, nghĩa là các đường đi qua đồ thị, bắt đầu từ nút xuất phát. Tập lời giải này được lưu trong một hàng đợi ưu tiên (priority queue). Thứ tự ưu tiên gán cho một đường đi x được quyết định bởi hàm f(x) = g(x) + h(x).

Trong đó, g(x) là chi phí của đường đi cho đến thời điểm hiện tại, nghĩa là tổng trọng số của các cạnh đã đi qua. h(x) là hàm đánh giá heuristic về chi phí nhỏ nhất để đến đích từ x. Ví dụ, nếu "chi phí" được tính là khoảng cách đã đi qua, khoảng cách đường chim bay giữa hai điểm trên một bản đồ là một đánh giá heuristic cho khoảng cách còn phải đi tiếp.

Hàm f(x) có giá trị càng thấp thì độ ưu tiên của x càng cao (do đó có thể sử dụng một cấu trúc heap tối thiểu để cài đặt hàng đợi ưu tiên này).
Bài 5: Yêu cầu dùng Depth First Search chỉ cần trạng thái ban đầu của nó
Ví dụ một bản đồ cần khoảng 2000 nốt thì con pacman cũng chạy ngần ấy nốt nên khá là ok.
Bài 6: Yêu cầu sử dụng A* chỉ việc thêm hàm cornersHeuristic 
Ý tưởng la: Giả thiết rằng pacman có thể đi xuyên tường được 
Cũng khá giống bài toán người giao hàng 
Bài 7:
Tìm được đường đi tối ưu ăn hết thức ăn trên bản đồ (Map này không có quái nên search khá là đơn giản)
Không phải là tối ưu vì trong trường hợp nó ăn để lại thức ăn ở góc bên trái bỏ lại rồi ăn thức ăn ở góc bên phải rồi cuối cùng lại phải quay lại ăn thức ăn ở góc bên trái cho nên nó không được tối ưu 
Bài 8: Tìm thức ăn gần vớ trạng thái hiện tại của Pacman nhất 

