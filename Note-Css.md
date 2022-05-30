# Reset Css

1. Sử dụng nomalizer
   link: https://cdnjs.com/libraries/normalize
2. dùng:
   https://meyerweb.com/eric/tools/css/reset/

# File Css

1. -- root: đặc dùng cho đặc biến.
2. - : Chọn tất cả các phần tử luôn.
3. html: Chỉ chọn các phần tử của html.

# Display: Block, Inline, Inline-Block

1. Inline:

   - Điển hình: thẻ span,
   - Đặc tính: + Không thể set width và hight. + Chỉ chiếm đủ chiều dài của nó. + Sẽ xuống dòng khi hết bề ngang. + Có thể điều chỉnh Margin Left và Right nhưng Top và Bottom là không thể.
     -- Đặc biệt:

2. Block:

   - Điển hiền: thẻ div,
   - Đặc tính: + Chiếm toàn bộ width NẾU không được set trước. + Luôn xuống dòng mới. + Có thể set đầy đủ Margin và Padding với 4 hướng khác nhau.
     -- Đặc biệt:

3. Inline-Block

   - Điển hình: thẻ button, input, select, img, textarea.
   - Đặc tính: là con lai: + Nhận đặc tính nằm cùng 1 dòng của inline. + Nhận đặc tính set đủ Margin, Padding và 4 phía.
     -- Đặc biệt: Thường sử dụng làm Nav. - Không tự động kế thừa chiều ngang của cha nó.

- Ghi chú kèm theo:

  - Đặc tính của thẻ ul li mặc định là list item => nó tương đương với block.
  - Khi 1 thẻ div bị float thì nó sẽ mất đi tính kế thừa của nó.

# font size: rem or fixel

Mặc định trên trình duyệt fontsize 100% là 16px.
Để cho 1 rem là 10px thì cho thẻ html có font-size là 62.5%.

# Chữ

    - Luôn nằm giữa line-hieght => canh giữa.
    - Line height trong tiếng Anh là 1.4 còn tiếng Việt là 1.6.
    - Các thuộc tính thường sử dụng Letter Spacing, Font Style,
    - Canh chữ 2 đầu: text align: justify
    - sans-serif là chủng chữ ko có chân

# Input & Label

    - Label for chỉ dùng được cho thằng id.
    - Sử dụng padding để tăng chiều cao.

# Ảnh

    - Tính chất hình ảnh sẽ không tự co nhỏ theo thẻ cha của nó.=> width: 100%.
    - Do có thuộc tính là inline nên sẽ có margin ẩn. => display:block;
    - object-fit giải quyết đc cắt ảnh.

# Back-Ground

    - background: url(./img/slider.jpg) top center /cover no-repeat;=> url + position + /size + repeat.

# Overlay

    - Dùng position: fixed.Top+ Left+ Right+ Bottom = 0 .

# Nền responsive

---

.grid{
width: 1200px;
max-width: 100%;
margin: 0 auto;
}
.grid**full--width{
width: 100%;
}
.grid**row{
display: flex;
flex-wrap: wrap;

- những phần tử con sẽ nằm ngang và rớt dòng
  }

---

# Responsive

    - Thủ thuật với over play :
        + width: 900px;
        + max-width: calc(100% - 48px);
    - Media queries: chuỗi truy vấn giúp chúng ta khoanh vùng ra được từng vùng để viết css.
    - Các cặp tính chất đi kèm:
        + width: px + max width: %.
        + overflow: hiden.

# Icon

    1. Nguồn: themify.
    2. Có những lọi icon có chiều ngang chiều dọc khác nhau, gây khó sẽ cho ta khi set => set cho icon width hoặc hieght.
    3. link awesome icon : <script src="https://kit.fontawesome.com/c2f6cce2fd.js" crossorigin="anonymous"></script>

# Lưu Ý Khi Code:

    - Làm subnav nhớ margin top để tránh ko tương thích trình duyệt.

# Vấn Đề:

    1. Sử dụng FLoat: khi tất cả thẻ con sử dụng float thì nó sẽ chui ra mặt phẳng khác dẫn đến việc thẻ cha bị co rúm lại.
        => thêm class clear với css clear both.
        => overlow:hiden cho thằng cha nó hay còn gọi là float container.
        => đặt thẻ giả cho thằng cha ::after{
            content:"";
            display:block;
            clear:both;
        }

# Nguyên Tắc

    1. Khi khi nhúng phông chữ hãy nhúng ở thẻ html vì nó mới là nơi chứa chữ.
    2. Khi css cho 1 thẻ nằm sâu thì nên css 3 cấp để chọn đúng thẻ đó.
    3. BEM : Block__Element--Modify

# Qui tắc BEM: Block Element Modify

# Kỹ Thuật Nâng Cao

    1. Copy Id nhanh: select điểm giống => arrow right => Ctrl + Shift + l.
    2. Kỹ thuật Background Image: padding top 50% and width 100%.
    3. Kỹ thuật margin thẻ cha âm, thẻ con padding dương để tạo khối cột cách nhau.
    3. Ngăn sự kiện nổi bọt: stopPropagation()
    4. Selector những thằng có điểm giống nhau:
        + document.querySelectorAll('#nav li a[href*="#"]')
    5. Selector ra thằng có con trong đó trpng js: nextElementSibling
    6. Không cho user copy dùng thuộc tính user-select:none;
    7. CHọn tâm của scale dùng thuộc tính transform-origin.
    8. Làm cái mũi tên chỉa lên. dùng border ko set width height mà dùng độ dày của border left, right, top, bottom.
    9. Sử dụng thuộc tính will-change để tăng tính tối ưu cho animation.
    10. hover vào chạy tới chạy lui: dùng :hover + transition + relative.
    ***

.category\_\_item--link{
display: block;
padding: 8px 12px ;
right: 0;
transition: right ease-in 1s;
position: relative;

}
.category\_\_item--link:hover{
color: #ee4d2d;
right: -4px;
}

---
