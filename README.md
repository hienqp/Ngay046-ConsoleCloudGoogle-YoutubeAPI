__YOUTUBE API - TẠO PROJECT GOOGLE CONSOLE__

- hướng dẫn tạo Project Google Console để sử dụng các API của Google
- hướng dẫn sử dụng Youtube API để play video từ Youtube mà không cần phải import file video vào project app (vì sẽ làm tăng dung lượng ứng dụng)
- thông thường nếu không muốn import file video vào app (play offline) ta có thể upload video đó lên server và sử dụng URL đến video đó để phát (play online)
- nếu không có server để upload thì có thể sử dụng server của Youtube để upload video lên server Youtube, sau đó sử dụng Youtube API để phát video đó (play online)
- Youtube API cho phép ta phát video được lưu trữ trên server của Youtube

___

__HƯỚNG DẪN SỬ DỤNG DEVELOPERS CONSOLE GOOGLE__

- để sử dụng Google Developer Console ta thực hiện theo các bước sau
	- trong Project, xin quyền Internet ở AndroidManifest
    <img src="https://github.com/hienqp/Ngay046-ConsoleCloudGoogle-YoutubeAPI/blob/main/1_xin_quyen_internet.png"> <br/>

	- download library Youtube Android Player API
    <img src="https://github.com/hienqp/Ngay046-ConsoleCloudGoogle-YoutubeAPI/blob/main/2_download_youtube_android_player_api.png"> <br/>
    
	- giải nén folder chứa YoutubeAndroidPlayer API, sau đó copy file
    <img src="https://github.com/hienqp/Ngay046-ConsoleCloudGoogle-YoutubeAPI/blob/main/3_giai_nen_copy_file_jar.png"> <br/>
    
	- paste file jar vào folder libs của Project ở View Project
    <img src="https://github.com/hienqp/Ngay046-ConsoleCloudGoogle-YoutubeAPI/blob/main/4_paste_file_jar_vao_folder_libs.png"> <br/>
    
	- chuột phải vào file jar chọn Add As Library để add library này vào module:app
    <img src="https://github.com/hienqp/Ngay046-ConsoleCloudGoogle-YoutubeAPI/blob/main/5_add_as_library.png"> <br/>
    
	- kết quả sau khi add as library
    <img src="https://github.com/hienqp/Ngay046-ConsoleCloudGoogle-YoutubeAPI/blob/main/6_kq_sau_khi_add_as_library.png"> <br/>
    
	- để có thể play video từ youtube, ta tiến hành lấy YOUTUBE_API_KEY, api key này dùng để gửi package name và SHA1 certificate fingerprint lên Google Developer Consonle
	- truy cập Google Developer Console [https://console.developers.google.com](https://console.developers.google.com)
	- đăng nhập tài khoản google
    <img src="https://github.com/hienqp/Ngay046-ConsoleCloudGoogle-YoutubeAPI/blob/main/7_login_google.png"> <br/>
    
	- click chọn country và các term của Google API, ta sẽ vào giao diện DASHBOARD của Google Developer Console
    <img src="https://github.com/hienqp/Ngay046-ConsoleCloudGoogle-YoutubeAPI/blob/main/8_check_terms.png"> <br/>
    
	- copy package name của Project
    <img src="https://github.com/hienqp/Ngay046-ConsoleCloudGoogle-YoutubeAPI/blob/main/9_copy_package_name_of_project.png"> <br/>
    
	- ở DashBoard của GDC click SELECT A PROJECT
    <img src="https://github.com/hienqp/Ngay046-ConsoleCloudGoogle-YoutubeAPI/blob/main/10_click_select_a_project_on_dashboard_of_google_developer_console.png"> <br/>
    
	- cửa sổ quản lý Project hiện lên, chọn NEW PROJECT
    <img src="https://github.com/hienqp/Ngay046-ConsoleCloudGoogle-YoutubeAPI/blob/main/11_click_new_project.png"> <br/>
    
	- paste package name của project android vào ô project name của GDC project, GDC sẽ tự Generate Project ID (ta có thể tự EDIT lại theo nhu cầu, sau khi CREATE thì không thể thay đổi), sau đó click CREATE
    <img src="https://github.com/hienqp/Ngay046-ConsoleCloudGoogle-YoutubeAPI/blob/main/12_paste_package_name_project_into_name_project_field.png"> <br/>
    
	- DashBoard hiển thị Project GDC vừa CREATE (hoặc ta có thể tự click chọn Project), click chọn mục CREDENTIALS
    <img src="https://github.com/hienqp/Ngay046-ConsoleCloudGoogle-YoutubeAPI/blob/main/13_after_create_project_gdc.png"> <br/>
    
	- sau khi chọn CREDENTIALS, cửa sổ Credentials hiển thị, click chọn CREATE CREDENTIALS, chọn API KEY, GDC tự sinh API KEY và hiển thị Popup chứa chuỗi API KEY
    <img src="https://github.com/hienqp/Ngay046-ConsoleCloudGoogle-YoutubeAPI/blob/main/14_create_credentials.png"> <br/>
    
    <img src="https://github.com/hienqp/Ngay046-ConsoleCloudGoogle-YoutubeAPI/blob/main/15_content_api_key.png"> <br/>
    
	- tiến hành edit API KEY
    <img src="https://github.com/hienqp/Ngay046-ConsoleCloudGoogle-YoutubeAPI/blob/main/16_edit_api_key.png"> <br/>
    
	- Application restrictions chọn Android apps
    <img src="https://github.com/hienqp/Ngay046-ConsoleCloudGoogle-YoutubeAPI/blob/main/17_application_restrictioins_select_android.png"> <br/>
    
	- mục Restrict usage to your Android Apps click ADD
    <img src="https://github.com/hienqp/Ngay046-ConsoleCloudGoogle-YoutubeAPI/blob/main/17_1_Restrict_usage_to_your_Android_Apps_click_ADD.png"> <br/>
    
	- copy full package name app trong Gradle Script module app
    <img src="https://github.com/hienqp/Ngay046-ConsoleCloudGoogle-YoutubeAPI/blob/main/18_copy_full_package_name_app.png"> <br/>
    
	- paste full package name app
    <img src="https://github.com/hienqp/Ngay046-ConsoleCloudGoogle-YoutubeAPI/blob/main/19_paste_full_package_name.png"> <br/>
    
	- mở Gradle tab trong Android Studio, double click signingReport
    <img src="https://github.com/hienqp/Ngay046-ConsoleCloudGoogle-YoutubeAPI/blob/main/20_run_signingReport_inGradle_tab.png"> <br/>
    
	- copy SHA1 Key
    <img src="https://github.com/hienqp/Ngay046-ConsoleCloudGoogle-YoutubeAPI/blob/main/21_copy_SHA1_key.png"> <br/>
    
    - để mở được Gradle Task List, ta bỏ chọn __Do not build Gradle task list during Gradle sync__ sau đó apply OK
    <img src="https://github.com/hienqp/Ngay046-ConsoleCloudGoogle-YoutubeAPI/blob/main/21_1_turn_on_Gradle_task_list.png"> <br/>
    
	- paste SHA1 Key vào cửa sổ EDIT API KEY, sau đó click DONE
    <img src="https://github.com/hienqp/Ngay046-ConsoleCloudGoogle-YoutubeAPI/blob/main/22_paste_SHA1_key_on_GDC.png"> <br/>
    
	- click SAVE để lưu lại quá trình EDIT API KEY của project trên GDC, quay trở lại cửa sổ Credentials
    <img src="https://github.com/hienqp/Ngay046-ConsoleCloudGoogle-YoutubeAPI/blob/main/23_click_SAVE_to_comple_editting_API_KEY.png"> <br/>
    
	- click SHOW API KEY và copy API KEY
    <img src="https://github.com/hienqp/Ngay046-ConsoleCloudGoogle-YoutubeAPI/blob/main/24_click_SHOW_KEY_and_copy_API_KEY.png"> <br/>
    
	- trong Project App, tạo class __config__ chứa thông tin của API Key
    <img src="https://github.com/hienqp/Ngay046-ConsoleCloudGoogle-YoutubeAPI/blob/main/25_create_class_contain_api_key.png"> <br/>
    
	- quay trở lại GDC, ở giao diện API & Service, click chọn mục Library
    <img src="https://github.com/hienqp/Ngay046-ConsoleCloudGoogle-YoutubeAPI/blob/main/26_goto_library.png"> <br/>
    
	- trong list các Library, chọn Youtube Data API V3
    <img src="https://github.com/hienqp/Ngay046-ConsoleCloudGoogle-YoutubeAPI/blob/main/27_goto_youtube_api_v3.png"> <br/>
    
	- click ENABLE để kích hoạt Youtube Data API V3
    <img src="https://github.com/hienqp/Ngay046-ConsoleCloudGoogle-YoutubeAPI/blob/main/28_click_enable.png"> <br/>
    
	- nếu ``targetApi`` trong thẻ ``application`` của AndroidManifest là 30 hoặc cao hơn, việc truy vấn thông tin về các ứng dụng khác được cài đặt trên thiết bị, hệ thống sẽ lọc các thông tin này theo mặc định, được gọi là tính năng LỌC HẠN CHẾ KHẢ NĂNG HIỂN THỊ GÓI, Khả năng hiển thị ứng dụng hạn chế ảnh hưởng đến kết quả trả về của các phương thức cung cấp thông tin về các ứng dụng khác, chẳng hạn như queryIntentActivities(), getPackageInfo() và getInstalledApplications(). Khả năng hiển thị hạn chế cũng ảnh hưởng đến các tương tác rõ ràng với các ứng dụng khác, chẳng hạn như bắt đầu dịch vụ của ứng dụng khác.
	- ở đây để sử dụng dịch vụ của Youtube, ta cần khai báo Package cần được hiển thị trong AndroidManifest, bằng cách thêm đoạn code khai báo sau
```xml
<?xml version="1.0" encoding="utf-8"?>
<manifest xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:tools="http://schemas.android.com/tools">
    //...

    <queries>
        <intent>
            <action android:name="com.google.android.youtube.api.service.START" />
        </intent>
    </queries>

    //...
</manifest>
```
- như vậy ta đã hoàn thành việc chuẩn bị sử dụng dịch vụ của Google, ở đây là Youtube API thông qua Google Developer Console

___

__THIẾT KẾ GIAO DIỆN ỨNG DỤNG__

- __activity_main.xml__
```xml
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">

    <view
        android:id="@+id/youtubeplay"
        class="com.google.android.youtube.player.YouTubePlayerView"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent" />

    <Button
        android:id="@+id/buttonplay"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginBottom="36dp"
        android:text="Button"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.498"
        app:layout_constraintStart_toStartOf="parent" />

</androidx.constraintlayout.widget.ConstraintLayout>
```

___

__LOGIC CỦA ỨNG DỤNG__

- đầu tiên __MainActivity__ sẽ __extends YouTubeBaseActivity__

```java
public class MainActivity extends YouTubeBaseActivity {
    //...
}
```

- __implements YouTubePlayer.OnInitializedListener__ đồng thời override 2 method của __YouTubePlayer.OnInitializedListener__
- việc implements __YouTubePlayer.OnInitializedListener__ để triển khai 2 method lắng nghe sự kiện khởi tạo connect đến Youtube Success hay Failure

```java
public class MainActivity extends YouTubeBaseActivity implements YouTubePlayer.OnInitializedListener {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

    }

    @Override
    public void onInitializationSuccess(YouTubePlayer.Provider provider, YouTubePlayer youTubePlayer, boolean b) {
        
    }

    @Override
    public void onInitializationFailure(YouTubePlayer.Provider provider, YouTubeInitializationResult youTubeInitializationResult) {
        
    }
}
```

- khai báo và ánh xạ YouTubePlayerView và Button play

```java
public class MainActivity extends YouTubeBaseActivity implements YouTubePlayer.OnInitializedListener {
	YouTubePlayerView mYouTubePlayerView;
    Button btnPlay;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        mYouTubePlayerView = findViewById(R.id.youtubeplay);
        btnPlay = findViewById(R.id.buttonplay);

    }

    @Override
    public void onInitializationSuccess(YouTubePlayer.Provider provider, YouTubePlayer youTubePlayer, boolean b) {
        
    }

    @Override
    public void onInitializationFailure(YouTubePlayer.Provider provider, YouTubeInitializationResult youTubeInitializationResult) {
        
    }
}
```

- viết 1 method __private void__ dùng để khởi tạo init connect đến Youtube bằng API_KEY ở Context hiện tại
- khi method này được gọi, nó sẽ thực hiện việc khởi tạo YoutubePlayer dùng để phát và điều khiển video Youtube, việc khởi tạo thành công hay thất bại thông qua việc 
	- kiểm tra kết nối INTERNET 
	- kiểm tra đã tạo Project trên GDC hay chưa
	- kiểm tra __YOUTUBE_API_KEY__ đã kích hoạt Youtube Data API V3 hay chưa
- việc khởi tạo thành công hay thất bại, nó đều gọi đến 1 trong 2 callback của __YouTubePlayer.OnInitializedListener__ mà __MainActivity__ đã __implements__
```java
    private void initializationYoutubeConnect() {
        mYouTubePlayerView.initialize(Config.getYoutubeApiKey(), MainActivity.this);
    }
```

- trong __onCreate()__ tiến hành bắt sự kiện của Button Play, khi user click vào Button, sẽ gọi đến method khởi tạo kết nối Youtube
```java
    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        mYouTubePlayerView = findViewById(R.id.youtubeplay);
        btnPlay = findViewById(R.id.buttonplay);

        btnPlay.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                initializationYoutubeConnect();
            }
        });
    }
```

- nếu __initialize()__ thành công, callback __onInitializationSuccess()__ sẽ được gọi, trong callback này ta sẽ thực hiện loadvide Youtube với tham số truyền vào là ID của video đó trên Youtube thông qua đối số __youTubePlayer__ được truyền vào callback
- ID của video trên Youtube chính là chuỗi String nằm sau chuỗi URL ``https://www.youtube.com/watch?v=``
- ví dụ URL ``https://www.youtube.com/watch?v=YNOTOktaS7s`` ta có ID là ``YNOTOktaS7s``
- callback __onInitializationSuccess()__ sẽ được viết như sau với ID như trên

```java
    @Override
    public void onInitializationSuccess(YouTubePlayer.Provider provider, YouTubePlayer youTubePlayer, boolean b) {
        youTubePlayer.loadVideo("YNOTOktaS7s");
    }
```

- nếu __initialize()__ thất bại, callback __onInitializationFailure()__ sẽ được gọi, trong callback này trả về đối tượng là kết quả của việc khởi tạo thất bại __youTubeInitializationResult__, ta sẽ sử dụng đối tượng này để kiểm tra việc khởi tạo thất bại có phải từ phía user hay không
	- nếu là lỗi từ user, từ đối tượng __youTubeInitializationResult__ ta gọi hiển thị Error Dialog, với 2 tham số truyền vào cho nó là
		- Context
		- số kiểu ``int`` (là 1 REQUEST_CODE, giá trị này sẽ được gửi đi để thử khởi tạo lại lần nữa, và dùng để kiểm tra kết quả trả về)
	- nếu không phải lỗi từ user, ta có thể xử lý đơn giản là Toast thông báo cho user
- ta sẽ khai báo 1 REQUEST_VIDEO kiểu ``int``
```java
public class MainActivity extends YouTubeBaseActivity implements YouTubePlayer.OnInitializedListener {
    YouTubePlayerView mYouTubePlayerView;
    Button btnPlay;

    final int REQUEST_VIDEO = 123;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        // ...
    }
    // ...
}
```

- callback __onInitializationFailure()__
```java
    @Override
    public void onInitializationFailure(YouTubePlayer.Provider provider, YouTubeInitializationResult youTubeInitializationResult) {
        if (youTubeInitializationResult.isUserRecoverableError()) {
            youTubeInitializationResult.getErrorDialog(MainActivity.this, REQUEST_VIDEO);
        } else {
            Toast.makeText(this, "Error !!!", Toast.LENGTH_SHORT).show();
        }
    }
```

- với REQUEST_VIDEO gửi đi được dùng để thử khởi tạo lại, ta sẽ gọi callback ``onActivityResult()`` để lấy kết quả trả về, nếu __requestCode__ trả về trùng với __REQUEST_VIDEO__ ta sẽ khởi tạo lại lần nữa việc kết nối đến Youtube
```java
    @Override
    protected void onActivityResult(int requestCode, int resultCode, Intent data) {
        if (requestCode == REQUEST_VIDEO) {
            initializationYoutubeConnect();
        }

        super.onActivityResult(requestCode, resultCode, data);
    }
```