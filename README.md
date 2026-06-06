# BÀI TẬP LỚN - PHÁT TRIỂN ỨNG DỤNG TRÊN THIẾT BỊ DI ĐỘNG
**Môn học:** TEE0419  
**Họ tên:** Lương Quang Hà  
**MSSV:** K225480106010  
**Lớp:** 58KTPM (K58KTP.K01)


## MỤC LỤC
1. [Phần 1 - MIT App Inventor](#phần-1---mit-app-inventor)
2. [Phần 2 - Android Studio](#phần-2---android-studio)
3. [Kết quả chạy thử](#kết-quả-chạy-thử)

---

# PHẦN 1 - MIT APP INVENTOR

## 1.1 Thanh công cụ MIT App Inventor

MIT App Inventor có giao diện chia thành 4 vùng chính:

| Vùng | Tên | Chức năng |
|------|-----|-----------|
| Trái | Palette | Danh sách các component (Button, Label, TextBox, WebViewer...) |
| Giữa | Viewer | Màn hình preview dạng điện thoại, kéo thả component vào đây |
| Phải | Properties | Bảng thuộc tính của component đang được chọn |
| Dưới | Components | Danh sách tất cả component đã thêm vào screen |
| Trên | Thanh menu | Screens, Connect, Build, Settings |

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/83814010-cef0-4e78-acc6-dd7253088339" />


---

## 1.2 Kéo thả và thay đổi thuộc tính

**Cách kéo thả:**
1. Chọn component trong Palette bên trái (ví dụ: Button)
2. Giữ chuột trái, kéo component sang vùng Viewer giữa
3. Thả ra vị trí mong muốn trên màn hình điện thoại ảo
4. Component xuất hiện trong Viewer và được thêm vào danh sách Components

**Cách thay đổi thuộc tính:**
1. Click vào component cần chỉnh (trên Viewer hoặc Components)
2. Bảng Properties bên phải tự động hiện thuộc tính của component đó
3. Click vào giá trị cần đổi → nhập giá trị mới
4. Thay đổi hiển thị ngay trên Viewer (real-time preview)

**Tại sao phải thay đổi thuộc tính:**
- **Text**: thay đổi nội dung hiển thị
- **Width/Height**: chỉnh kích thước (Fill parent / Wrap content / px cụ thể)
- **BackgroundColor**: đổi màu nền
- **FontSize, FontBold**: định dạng chữ
- **Hint** (TextBox): chữ mờ trong hộp nhập
- **HomeUrl** (WebViewer): URL trang web sẽ tải

<img width="1920" height="1067" alt="image" src="https://github.com/user-attachments/assets/42637289-c01a-4515-b9cc-2f16efca0504" />

---

## 1.3 Blocks — Lập trình bằng kéo thả

**Bản chất của Block:**  
Mỗi block là một lệnh lập trình được trực quan hóa bằng hình ảnh. Thay vì viết code bằng chữ, người dùng kéo các block ra và snap (gắn) chúng vào nhau. Các block gắn vào nhau sẽ thực thi theo thứ tự từ trên xuống dưới.

**Cách sử dụng Blocks:**
1. Nhấn nút **Blocks** góc trên phải để chuyển sang màn hình lập trình
2. Bên trái hiện danh sách tất cả component và nhóm lệnh (Logic, Math, Text, Control...)
3. Click vào tên component → chọn block cần dùng
4. Kéo block ra vùng trắng giữa → snap vào các block khác

**Ưu điểm so với viết code:**
- Không cần nhớ cú pháp (syntax) — không bị lỗi syntax
- Trực quan, dễ hiểu logic
- Block chỉ snap đúng kiểu — hạn chế lỗi ngữ nghĩa
- Phù hợp người mới bắt đầu lập trình

**Nhược điểm:**
- Khó làm app phức tạp, nhiều chức năng
- Không linh hoạt bằng code thực
- Khó tái sử dụng code (copy block phức tạp)
- Hiệu năng thấp hơn app native Android/iOS

**Backpack (sao chép block giữa các Screen):**
- Biểu tượng ba lô góc trên phải màn hình Blocks
- Kéo block vào Backpack để lưu tạm
- Chuyển sang Screen khác → kéo block từ Backpack ra để dùng lại
- Tương đương Copy-Paste nhưng hoạt động qua các Screen khác nhau

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/e5cd2f01-f101-4358-848e-b072418c2a6f" />


---

## 1.4 Mô tả 3 Screen đã tạo

### Screen 1 — Giới thiệu

**Giao diện (Designer):**
- Label: Họ tên — "Lương Quang Hà" (FontSize 18, Bold, Center)
- Label: MSSV — "K225480106010" (FontSize 16, Center)
- Label: Lớp — "58KTPM" (FontSize 16, Center)
- Button: "Giải toán" (Width Fill parent, BackgroundColor Cyan)
- Button: "Xem trang web" (Width Fill parent, BackgroundColor Orange)

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/a56f5e1a-6fb5-4d13-ac2b-e0d04875feec" />


**Blocks:**
```
when Button1.Click
  open another screen screenName: "Screen2"

when Button2.Click
  open another screen screenName: "Screen3"
```

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/71dc0b5b-61db-469f-87ad-919a33f0c0f4" />

---

### Screen 2 — Giải phương trình bậc 2

**Giao diện (Designer):**
- Label tiêu đề: "Giải phương trình bậc 2: ax² + bx + c = 0"
- TextBox3: Hint "Nhập a", NumbersOnly = true
- TextBox4: Hint "Nhập b", NumbersOnly = true
- TextBox5: Hint "Nhập c", NumbersOnly = true
- Button1: "Giải" (Width Fill parent)
- Label1: hiện kết quả (để trống ban đầu)

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/b5e661c3-b7ee-44b5-9119-d0f00c8e16ef" />

**Blocks — Logic giải phương trình:**
```
initialize global a to 0
initialize global b to 0
initialize global c to 0
initialize global delta to 0

when Button1.Click
  set global a to TextBox3.Text
  set global b to TextBox4.Text
  set global c to TextBox5.Text
  set global delta to (b×b) - (4×a×c)

  if global delta < 0
    then  set Label1.Text to "Vô nghiệm"
  else if global delta = 0
    then  set Label1.Text to join ["Nghiệm kép: x = "] [(-b)/(2a)]
  else
    set Label1.Text to join ["x1 = "] [x1] ["  x2 = "] [x2]
```

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/653fcecc-89e1-4231-b1ce-9d4da7ea65ce" />


---

### Screen 3 — WebView

**Giao diện (Designer):**
- WebViewer: Width = Fill parent, Height = Fill parent
- HomeUrl: `https://www.apple.com/vn/shop/buy-iphone`

*(Screen3 không có Blocks vì WebViewer tự động tải trang web khi mở Screen)*

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/85a1823b-b03c-4d90-91e2-e94557550838" />

---
## Kết quả sau khi test app
<img width="1290" height="2796" alt="image" src="https://github.com/user-attachments/assets/f3782d8f-a745-46be-aa0e-4703dbbdddaa" />
<img width="1290" height="2796" alt="image" src="https://github.com/user-attachments/assets/9847ebc4-8aa0-41be-9a96-33b8443625e2" />
<img width="1290" height="2796" alt="image" src="https://github.com/user-attachments/assets/9cbe4201-9824-4bcf-b79a-b21a53a14fe3" />
---

# PHẦN 2 - ANDROID STUDIO

## 2.1 AndroidManifest.xml

**AndroidManifest.xml là gì:**  
File cấu hình trung tâm của mọi ứng dụng Android. Nó khai báo mọi thứ Android cần biết trước khi chạy app: tên app, icon, danh sách Activity, quyền truy cập, phiên bản tối thiểu...

**Các thành phần chính:**

| Thẻ XML | Ý nghĩa |
|---------|---------|
| `<manifest>` | Thẻ gốc, khai báo package name (tên duy nhất của app) |
| `<uses-permission>` | Xin quyền từ hệ điều hành (INTERNET, CAMERA, LOCATION...) |
| `<application>` | Thông tin chung: icon, label, theme |
| `<activity>` | Khai báo từng Activity có trong app |
| `<intent-filter>` | Xác định Activity nào là màn hình khởi động đầu tiên |

**Khai báo quyền — cú pháp và ý nghĩa:**

App cần khai báo quyền trong Manifest để hệ điều hành biết app sẽ dùng tài nguyên gì. Ví dụ app này cần INTERNET để gọi API và tải trang web:

```xml
<uses-permission android:name="android.permission.INTERNET"/>
```

Có 2 loại quyền:
- **Normal permission** (như INTERNET): khai báo trong Manifest là đủ, hệ thống tự cấp, không hỏi người dùng
- **Dangerous permission** (như CAMERA, LOCATION, READ_CONTACTS): phải khai báo trong Manifest **và** phải hỏi người dùng lúc runtime

**Kiểm tra quyền runtime (dangerous permission) trong Java:**
```java
if (ContextCompat.checkSelfPermission(this, Manifest.permission.CAMERA)
        != PackageManager.PERMISSION_GRANTED) {
    // Chưa có quyền → xin quyền
    ActivityCompat.requestPermissions(this,
        new String[]{Manifest.permission.CAMERA}, REQUEST_CODE);
} else {
    // Đã có quyền → dùng camera
    moCamera();
}
```

Ý nghĩa: tránh app bị crash khi người dùng chưa cấp quyền; đảm bảo người dùng biết app dùng tài nguyên gì và có thể từ chối.

**File AndroidManifest.xml của dự án:**

```xml
<?xml version="1.0" encoding="utf-8"?>
<manifest xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:tools="http://schemas.android.com/tools">

    <uses-permission android:name="android.permission.INTERNET"/>

    <application
        android:allowBackup="true"
        android:icon="@mipmap/ic_launcher"
        android:label="@string/app_name"
        android:theme="@style/Theme.Luongquangha">
        <activity android:name=".WebViewActivity" android:exported="false" />
        <activity android:name=".GiaiToanActivity" android:exported="false" />
        <activity android:name=".MainActivity" android:exported="true">
            <intent-filter>
                <action android:name="android.intent.action.MAIN" />
                <category android:name="android.intent.category.LAUNCHER" />
            </intent-filter>
        </activity>
    </application>

</manifest>
```

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/71b329a8-210c-4f14-a8e9-c73279c996e1" />


---

## 2.2 Vòng đời Activity (Activity Lifecycle)

**Vòng đời là gì:**  
Mỗi Activity Android trải qua các trạng thái từ khi tạo ra đến khi bị hủy. Hệ điều hành gọi các phương thức tương ứng khi Activity đổi trạng thái.

**Sơ đồ vòng đời:**
```
onCreate() → onStart() → onResume() → [ĐANG CHẠY]
                                            |
                          người dùng rời app
                                            |
                       onPause() → onStop() → onDestroy()
```

**Tại sao phải có onCreate():**
- `onCreate()` là phương thức chạy đầu tiên khi Activity được tạo
- Đây là nơi để: đặt layout (`setContentView`), tìm các View (`findViewById`), gắn sự kiện (`setOnClickListener`), khởi tạo dữ liệu ban đầu
- Nếu không có `onCreate()` → app không biết hiển thị gì, không biết lấy dữ liệu từ đâu
- Android Studio tự sinh sẵn `onCreate()` khi tạo project vì đây là phương thức bắt buộc của mọi Activity

---

## 2.3 XML Layout và Tham chiếu thuộc tính

**Cấu trúc file layout XML:**
- Mỗi file `.xml` trong `res/layout/` mô tả giao diện của 1 Activity
- Thẻ gốc là ViewGroup (LinearLayout, ConstraintLayout...) — chứa các View con bên trong
- Mỗi View/ViewGroup có thể có thuộc tính: `id`, `layout_width`, `layout_height`, `text`, `hint`...

**ViewGroup phổ biến:**

| ViewGroup | Sắp xếp con |
|-----------|-------------|
| LinearLayout | Xếp chồng dọc (vertical) hoặc ngang (horizontal) |
| ConstraintLayout | Neo vị trí bằng ràng buộc (constraint) |
| RelativeLayout | Đặt vị trí tương đối với nhau hoặc với parent |
| FrameLayout | Xếp chồng lên nhau (layered) |

**Thuộc tính quan trọng:**
- `android:id="@+id/tenId"` — định danh để Java tìm thấy View này
- `android:layout_width` / `android:layout_height`: `match_parent` (đầy ra), `wrap_content` (vừa đủ)
- `android:text` — nội dung chữ
- `android:hint` — chữ mờ trong EditText
- `android:orientation` — hướng sắp xếp của LinearLayout
- `android:gravity` — căn chỉnh nội dung bên trong View (center, left, right...)

**Tham chiếu thuộc tính — tránh hardcode:**

Thay vì ghi thẳng chuỗi vào XML (hardcode), nên lưu giá trị vào file `res/values/strings.xml` rồi tham chiếu tới:

```xml
<!-- res/values/strings.xml -->
<resources>
    <string name="app_name">BaiTapLon</string>
    <string name="btn_giai_toan">Giải toán</string>
</resources>
```

Cú pháp tham chiếu trong XML:
```xml
<Button android:text="@string/btn_giai_toan" />
```

Cú pháp tham chiếu trong Java (tránh hardcode):
```java
String label = getString(R.string.btn_giai_toan);
tvName.setText(getString(R.string.ten_sinh_vien));
```

**Ưu điểm của tham chiếu:**
- Thay đổi 1 chỗ → cập nhật toàn bộ app
- Dễ dịch đa ngôn ngữ
- Hệ điều hành tự lấy đúng giá trị theo LOCATION / LANGUAGE / THEME của người dùng

**OS hỗ trợ auto theo LOCATION / LANGUAGE / THEME:**

Android tự động chọn đúng file resource dựa trên thiết lập của người dùng:

| Thư mục | Khi nào dùng |
|---------|-------------|
| `res/values/strings.xml` | Mặc định |
| `res/values-vi/strings.xml` | Khi điện thoại đặt tiếng Việt |
| `res/values-en/strings.xml` | Khi điện thoại đặt tiếng Anh |
| `res/values-night/colors.xml` | Khi bật Dark Mode |
| `res/layout-land/` | Khi xoay ngang màn hình |

→ App tự hiển thị đúng ngôn ngữ, đúng màu sắc dark/light, đúng layout ngang/dọc mà **không cần lập trình thêm**.

**Tham chiếu trong Java bằng `findViewById`:**
```java
// Trong XML đã khai báo: android:id="@+id/btnGiai"
// Trong Java tìm lại bằng:
Button btnGiai = findViewById(R.id.btnGiai);
```

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/57b3224d-0e53-41d6-9f5a-2b6c8d841cc0" />
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/9d5e7f92-a965-4912-9ff3-a5307030d7b4" />

---

## 2.4 Xử lý sự kiện (Event Handling)

**Sự kiện là gì:**  
Sự kiện xảy ra khi người dùng tác động vào app: click button, nhập text, vuốt màn hình... Mỗi sự kiện có thể gắn một đoạn code để xử lý.

**Layout cần làm gì:**  
View cần có `android:id` để Java tìm được; với Cách 2 cần thêm `android:onClick`.

**2 cách gắn sự kiện cho Button:**

**Cách 1 — setOnClickListener trong Java (dùng trong dự án này):**
```java
Button btnGiaiToan = findViewById(R.id.btnGiaiToan);
btnGiaiToan.setOnClickListener(v -> {
    Intent intent = new Intent(this, GiaiToanActivity.class);
    startActivity(intent);
});
```

**Cách 2 — thuộc tính onClick trong XML:**
```xml
<Button
    android:id="@+id/btnGiaiToan"
    android:onClick="moGiaiToan"
    android:text="@string/btn_giai_toan"/>
```
Sau đó trong Java khai báo phương thức:
```java
public void moGiaiToan(View v) {
    startActivity(new Intent(this, GiaiToanActivity.class));
}
```

**So sánh:**
- Cách 1: linh hoạt hơn, viết trong Java, rõ ràng ai xử lý gì, dễ debug
- Cách 2: ngắn gọn hơn trong XML, nhưng phương thức phải là `public` và nhận tham số `View`

---

## 2.5 Thư mục Assets

**Assets là gì:**  
Thư mục `app/src/main/assets/` dùng để chứa các file tĩnh (static) cần dùng trong app: ảnh, âm thanh, font chữ, file JSON, file HTML... Khi build app, toàn bộ file trong Assets được đóng gói vào file APK — app có thể đọc được kể cả khi offline.

**Lợi ích của việc có sẵn file trong Assets:**
- App hoạt động offline — không cần internet để tải dữ liệu
- Tốc độ đọc nhanh — dữ liệu nằm ngay trong app
- Ứng dụng: từ điển offline, sách hướng dẫn, bản đồ offline, câu hỏi trắc nghiệm...

**Khác với `res/`:**

| | assets/ | res/ |
|-|---------|------|
| Truy cập | `AssetManager`, đường dẫn chuỗi | `R.drawable.xxx`, `R.raw.xxx` |
| Cấu trúc thư mục | Tự do, lồng nhiều cấp | Phải đúng theo quy tắc |
| Loại file | Bất kỳ | Có quy định theo loại |
| Use case | File phức tạp, thư mục lồng nhau | Ảnh icon, string, layout |

**Cú pháp truy cập Assets trong Java:**
```java
AssetManager am = getAssets();
InputStream is = am.open("data/myfile.json");  // đường dẫn tương đối từ assets/
BufferedReader br = new BufferedReader(new InputStreamReader(is));
StringBuilder sb = new StringBuilder();
String line;
while ((line = br.readLine()) != null) sb.append(line);
String json = sb.toString();
```

---

## 2.6 App 1 — Ứng dụng dùng Assets

**Vấn đề đặt ra:** Xây dựng app hướng dẫn học từ vựng tiếng Anh hoạt động hoàn toàn offline, dữ liệu từ vựng được chuẩn bị sẵn trong Assets.

**Đặc thù dữ liệu:** File JSON chứa danh sách từ vựng, mỗi từ có nghĩa tiếng Việt và ví dụ. Không cần kết nối mạng — phù hợp cho học sinh vùng sâu vùng xa hoặc khi không có wifi.

**Cấu trúc Assets:**
```
assets/
  data/
    vocabulary.json
```

**Nội dung vocabulary.json:**
```json
[
  {
    "id": 1,
    "word": "Mobile",
    "meaning": "Di động, điện thoại di động",
    "example": "I use a mobile phone every day."
  },
  {
    "id": 2,
    "word": "Application",
    "meaning": "Ứng dụng",
    "example": "This application helps me learn English."
  }
]
```

**Thuật toán xử lý:**
1. Đọc file JSON từ Assets bằng `AssetManager`
2. Parse JSON thành danh sách đối tượng `Vocabulary` bằng `JSONArray`
3. Hiển thị danh sách bằng `ListView` hoặc `RecyclerView`

**Đối tượng dùng để hiển thị:** `ListView` với custom `ArrayAdapter` — mỗi item hiển thị từ, nghĩa và ví dụ.

**Đọc và parse dữ liệu:**
```java
// Đọc file
AssetManager am = getAssets();
InputStream is = am.open("data/vocabulary.json");
BufferedReader br = new BufferedReader(new InputStreamReader(is));
StringBuilder sb = new StringBuilder();
String line;
while ((line = br.readLine()) != null) sb.append(line);

// Parse JSON
JSONArray arr = new JSONArray(sb.toString());
List<String> danhSach = new ArrayList<>();
for (int i = 0; i < arr.length(); i++) {
    JSONObject item = arr.getJSONObject(i);
    danhSach.add(item.getString("word") + " — " + item.getString("meaning"));
}

// Hiển thị
ListView lv = findViewById(R.id.listView);
lv.setAdapter(new ArrayAdapter<>(this,
    android.R.layout.simple_list_item_1, danhSach));
```

---

## 2.7 App 2 — Tương đương MIT App Inventor (3 Activity)

**Cấu trúc dự án:**
```
app/
  src/main/
    java/com/example/luongquangha/
      MainActivity.java
      GiaiToanActivity.java
      WebViewActivity.java
    res/layout/
      activity_main.xml
      activity_giai_toan.xml
      activity_web_view.xml
    AndroidManifest.xml
```

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/f95a699e-08e2-4641-84aa-ad198fee5387" />


### Activity 1 — About (MainActivity.java)

```java
package com.example.luongquangha;

import android.content.Intent;
import android.os.Bundle;
import android.widget.Button;
import androidx.appcompat.app.AppCompatActivity;

public class MainActivity extends AppCompatActivity {
    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        Button btnGiaiToan = findViewById(R.id.btnGiaiToan);
        Button btnWebView  = findViewById(R.id.btnWebView);

        btnGiaiToan.setOnClickListener(v ->
            startActivity(new Intent(this, GiaiToanActivity.class)));

        btnWebView.setOnClickListener(v ->
            startActivity(new Intent(this, WebViewActivity.class)));
    }
}
```
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/0c1d3ece-b811-4753-b9f8-410598cd19ec" />

<img width="1456" height="819" alt="image" src="https://github.com/user-attachments/assets/cb767ead-2eef-43e7-a8c0-85a100626cb3" />


---

### Activity 2 — Giải toán (GiaiToanActivity.java)

Logic giải phương trình bậc 2 ax² + bx + c = 0:
- Tính delta = b² − 4ac
- Nếu delta < 0: vô nghiệm
- Nếu delta = 0: nghiệm kép x = −b/(2a)
- Nếu delta > 0: hai nghiệm x1, x2

Sau khi tính xong, gửi kết quả lên API `https://k58kmt.tdh.io.vn/api` và nhận lại phản hồi.

**JSON gửi lên:**
```json
{
  "app_by": "K225480106010",
  "input": { "a": 1, "b": -5, "c": 6, "name": "Luong Quang Ha" },
  "output": { "ketluan": "Hai nghiem phan biet", "abc": "x1=3.0 x2=2.0", "nghiem": 3.0 }
}
```

**JSON nhận về:**
```json
{ "ok": 1, "stt": 1234 }
```

**Code gọi API và nhận phản hồi:**
```java
void guiAPI(double a, double b, double c, String ketluan, String abc, double nghiem) {
    new Thread(() -> {
        try {
            URL url = new URL("https://k58kmt.tdh.io.vn/api");
            HttpURLConnection conn = (HttpURLConnection) url.openConnection();
            conn.setRequestMethod("POST");
            conn.setRequestProperty("Content-Type", "application/json");
            conn.setDoOutput(true);

            JSONObject input = new JSONObject();
            input.put("a", a); input.put("b", b);
            input.put("c", c); input.put("name", "Luong Quang Ha");

            JSONObject output = new JSONObject();
            output.put("ketluan", ketluan);
            output.put("abc", abc);
            output.put("nghiem", nghiem);

            JSONObject body = new JSONObject();
            body.put("app_by", "K225480106010");
            body.put("input", input);
            body.put("output", output);

            OutputStream os = conn.getOutputStream();
            os.write(body.toString().getBytes());
            os.flush();

            // Đọc phản hồi: {"ok":1,"stt":1234}
            BufferedReader br = new BufferedReader(
                new InputStreamReader(conn.getInputStream()));
            StringBuilder sb = new StringBuilder();
            String line;
            while ((line = br.readLine()) != null) sb.append(line);

            JSONObject response = new JSONObject(sb.toString());
            int ok  = response.getInt("ok");
            int stt = response.getInt("stt");

            // Hiển thị kết quả trên UI thread
            runOnUiThread(() ->
                tvKetQua.append("\nServer: ok=" + ok + ", stt=" + stt));

        } catch (Exception e) { e.printStackTrace(); }
    }).start();
}
```
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/d3fd5eff-285a-4470-9e4b-6ab784c7bb35" />

<img width="1456" height="819" alt="image" src="https://github.com/user-attachments/assets/0e60c13f-0205-4d81-be29-6e9ea3a72a3d" />


---

### Activity 3 — WebView (WebViewActivity.java)

Load trang web: `https://k58kmt.tdh.io.vn?masv=K225480106010`

```java
WebView webView = findViewById(R.id.webView);
webView.getSettings().setJavaScriptEnabled(true);
webView.setWebViewClient(new WebViewClient());
webView.loadUrl("https://k58kmt.tdh.io.vn?masv=K225480106010");
```
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/87f54fe5-c536-4468-904c-06a545fd6d3e" />

<img width="1456" height="819" alt="image" src="https://github.com/user-attachments/assets/88723b91-d379-4f5c-813f-4f7a34325542" />


*Lưu ý: Emulator không có kết nối internet thực nên hiển thị lỗi ERR_NAME_NOT_RESOLVED — trên điện thoại thật app sẽ tải đúng trang `k58kmt.tdh.io.vn`.*

---


