# Object Detection Projects

#1. Hướng dẫn

Kiểm tra xem khi git clone https://github.com/QuyItEngineer/countingcar.git
có thư mục out trong traffic-counting chưa.

Nếu chưa có thì tạo để khi build thì các frame ảnh được save tại đây.
Nếu có rồi thì xóa hết ảnh trong đó đi.

Xóa  file media .mp4,... và thêm file media của bạn vào.

Chạy file traffic.py bằng cmd nha. để có thể nhìn kết quả rõ hơn. Cú pháp: traffic.py

#2. Luồng đi

Khi run file nó sẽ vào hàm main để check folder out có tồn tại không để tạo mới.
Hàm train_bg_subtraction dùng để sau mỗi frame nó sẽ update backgroundSubtraction lại,
nhằm lọc được sạch hơn.

Đoạn: "base = np.zeros() .... (255,255,255)) [:,:, 0]" dùng để xét miền giới hạn màu cho frame.

Process dùng cắt nền của openCV: MOG2

Sau đó nó sẽ gọi các hàm liên quan là:
	a. pipeline
	b. ConntourDetection
	c. VehicleCounter
	
Không hiểu ở đây liên hệ Team Nobles nhé. =)