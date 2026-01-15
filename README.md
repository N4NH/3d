# Unity 3D – Coordinate System Exercise

## Thông tin
- Sinh viên: Phạm Nhật Anh
- Mã SV: BCS230012 
- Công cụ: Unity 2022.3.62f3  
- Render Pipeline: Built-in Render Pipeline  
- Nền tảng: Windows  

---

## Mục tiêu bài học
- Hiểu cách Unity chuyển đổi từ không gian 3D sang hiển thị 2D
- Sử dụng hệ tọa độ Cartesian (X, Y, Z)
- Phân biệt Left-Handed Coordinate System trong Unity
- Phân biệt Local Space, World Space và Screen Space
- Sử dụng Camera để chuyển World Space sang Screen Space

---

## PHẦN A – Coordinate System & World Space

**<img width="1919" height="1022" alt="image" src="https://github.com/user-attachments/assets/1bfc1a84-c469-4b2b-a86f-8cfce3f41ab5" />**

- Trục **Y** hướng lên trên  
- Trục **-Z** hướng về phía Camera  

---

## PHẦN B – Left-Handed Coordinate System

- Cube quay theo **chiều kim đồng hồ** khi xoay Rotation Y = 90  
- Unity sử dụng **Left-Handed Coordinate System** theo quy tắc bàn tay trái:
  - Trục **+X**: ngón cái  
  - Trục **+Y**: ngón trỏ  
  - Trục **+Z**: ngón giữa  

---

## PHẦN C – Local Space & World Space

- Local Position của Cube **không đổi** vì vị trí được tính tương đối so với Parent  
- Khi Parent di chuyển, **World Position của Cube thay đổi** thành: (8,2,0)

---

## PHẦN D – Graphics Pipeline & Camera

- Khi Camera tiến gần vật thể hơn, vật thể chiếm nhiều diện tích màn hình hơn nên **trông to hơn**
- **Field of View (FOV)**:
- FOV lớn → góc nhìn rộng → vật thể trông **nhỏ hơn** (zoom out)
- FOV nhỏ → góc nhìn hẹp → vật thể trông **to hơn** (zoom in)
- Vật thể có thể **biến mất** nếu nằm ngoài tầm hiển thị của Camera (clipping hoặc ngoài frustum)

---

## PHẦN E – Screen Space

**<img width="1919" height="1018" alt="image" src="https://github.com/user-attachments/assets/08d1e84a-0842-48ce-ae28-4fe06a0321c5" /> – Cube ở giữa màn hình**  
**<img width="1919" height="1019" alt="image" src="https://github.com/user-attachments/assets/b69c1bf3-d1e8-430a-a73b-f5e8a97e3c0e" /> – Cube ở góc dưới bên trái**

- Gốc tọa độ của **Screen Space** nằm ở **góc dưới bên trái** màn hình  
- **World Space**: mô tả thế giới 3D trong Unity  
- **Screen Space**: hiển thị vị trí 2D trên màn hình theo **pixel**, phụ thuộc vào Camera và độ phân giải

---

## Kết luận
Sau khi hoàn thành bài tập này, em đã hiểu rõ hơn về cách Unity sử dụng hệ tọa độ trong không gian 3D cũng như quá trình hiển thị từ World Space lên Screen Space thông qua Camera. Thông qua bài tập, em nhận ra rằng việc nắm vững các khái niệm này là nền tảng quan trọng để làm việc hiệu quả với các đối tượng 3D trong Unity. Bài tập cũng giúp em hiểu rõ hơn về Left-Handed Coordinate System mà Unity sử dụng, đặc biệt là cách vật thể xoay và định hướng trong không gian. Việc quan sát sự thay đổi của Cube khi xoay quanh trục Y giúp em liên hệ trực tiếp giữa lý thuyết và thực tế, từ đó tránh được những nhầm lẫn khi lập trình hoặc thiết kế scene. Ngoài ra, phần làm việc với Camera, Field of View và Clipping Plane giúp em hiểu vì sao cùng một vật thể nhưng có thể trông to, nhỏ hoặc thậm chí biến mất khỏi màn hình. 
