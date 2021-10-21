## Hướng Dẫn Sử Dụng Hệ Thống Trắc Nghiệm Online

Thực hiện: Võ Huy Khang - Email: huykhangvo02092000@gmail.com

Thời gian bắt đầu: Ngày 21 tháng 10 năm 2021

##### http://vohuykhang.freevnn.com/

### Giới thiệu

- Tôi đang học đầu năm 4 khoa CNTT. Tôi làm web này để phục vụ cho việc ôn tập, ôn thi các môn học trong thời gian tôi học Đại học..
- Mục tiêu: Xây dựng ✨hệ thống trắc nghiệm online✨ , thay thế cách thức làm bài tập và kiểm tra truyền thống.

##### Tính Năng

```
- Dễ dàng cài đặt và quản lý, không cần kiến thức lập trình
- Giao diện làm bài trực quan, hỗ trợ hiển thị công thức LaTeX
- Tự động lưu trạng thái làm bài của học sinh, thoát ra vào lại không bị mất bài đang làm
- Có thể xem điểm và xem lại bài thi sau khi nộp bài
- Hỗ trợ nhập công thức bằng LaTeX
- Hỗ trợ nhập liệu bằng file Excel
- Có thể xuất file Excel điểm của từng bài thi
- Câu hỏi phân loại theo mức độ: dễ, khó, trung bình, và phân loại theo chương: 1, 2, 3,...
```

#### Sắp Có

```
- Thêm tùy chọn nhập bộ câu hỏi từ file word. (Cảm ơn bạn tranphong965@gmail.com)
- Giáo viên có thể thêm câu hỏi vào ngân hàng đề (admin sẽ duyệt câu hỏi)
- Thêm người dùng mới "Giáo viên bộ môn" (formype@gmail.com)
- Hiển thị số tin nhắn chat, thông báo chưa đọc
- Thêm tự động cập nhật phiên bản phần mềm
- Thêm logs lưu vết tất cả các thông tin liên quan đến việc thay đổi dữ liệu trong cơ sở dữ liệu
- Thêm nhiều dạng bài tập trắc nghiệm hơn
- Hỡ trợ nhiều dạng thông tin có trong câu hỏi hơn như âm thanh, video...
```

This text you see here is *actually- written in Markdown! To get a feel
for Markdown's syntax, type some text into the left window and
watch the results in the right.

## Tech

Dillinger uses a number of open source projects to work properly:

- [AngularJS] - HTML enhanced for web apps!
- [Ace Editor] - awesome web-based text editor
- [markdown-it] - Markdown parser done right. Fast and easy to extend.
- [Twitter Bootstrap] - great UI boilerplate for modern web apps
- [node.js] - evented I/O for the backend
- [Express] - fast node.js network app framework [@tjholowaychuk]
- [Gulp] - the streaming build system
- [Breakdance](https://breakdance.github.io/breakdance/) - HTML
to Markdown converter
- [jQuery] - duh

And of course Dillinger itself is open source with a [public repository][dill]
 on GitHub.

## Installation

Dillinger requires [Node.js](https://nodejs.org/) v10+ to run.

Install the dependencies and devDependencies and start the server.

```sh
cd dillinger
npm i
node app
```

For production environments...

```sh
npm install --production
NODE_ENV=production node app
```

## Plugins

Dillinger is currently extended with the following plugins.
Instructions on how to use them in your own application are linked below.

| Plugin | README |
| ------ | ------ |
| Dropbox | [plugins/dropbox/README.md][PlDb] |
| GitHub | [plugins/github/README.md][PlGh] |
| Google Drive | [plugins/googledrive/README.md][PlGd] |
| OneDrive | [plugins/onedrive/README.md][PlOd] |
| Medium | [plugins/medium/README.md][PlMe] |
| Google Analytics | [plugins/googleanalytics/README.md][PlGa] |

## Development

Want to contribute? Great!

Dillinger uses Gulp + Webpack for fast developing.
Make a change in your file and instantaneously see your updates!

Open your favorite Terminal and run these commands.

First Tab:

```sh
node app
```

Second Tab:

```sh
gulp watch
```

(optional) Third:

```sh
karma test
```

#### Building for source

For production release:

```sh
gulp build --prod
```

Generating pre-built zip archives for distribution:

```sh
gulp build dist --prod
```

## Docker

Dillinger is very easy to install and deploy in a Docker container.

By default, the Docker will expose port 8080, so change this within the
Dockerfile if necessary. When ready, simply use the Dockerfile to
build the image.

```sh
cd dillinger
docker build -t <youruser>/dillinger:${package.json.version} .
```

This will create the dillinger image and pull in the necessary dependencies.
Be sure to swap out `${package.json.version}` with the actual
version of Dillinger.

Once done, run the Docker image and map the port to whatever you wish on
your host. In this example, we simply map port 8000 of the host to
port 8080 of the Docker (or whatever port was exposed in the Dockerfile):

```sh
docker run -d -p 8000:8080 --restart=always --cap-add=SYS_ADMIN --name=dillinger <youruser>/dillinger:${package.json.version}
```

> Note: `--capt-add=SYS-ADMIN` is required for PDF rendering.

Verify the deployment by navigating to your server address in
your preferred browser.

```sh
127.0.0.1:8000
```

## License

MIT

**Free Software, Hell Yeah!**

[//]: # (These are reference links used in the body of this note and get stripped out when the markdown processor does its job. There is no need to format nicely because it shouldn't be seen. Thanks SO - http://stackoverflow.com/questions/4823468/store-comments-in-markdown-syntax)

   [dill]: <https://github.com/joemccann/dillinger>
   [git-repo-url]: <https://github.com/joemccann/dillinger.git>
   [john gruber]: <http://daringfireball.net>
   [df1]: <http://daringfireball.net/projects/markdown/>
   [markdown-it]: <https://github.com/markdown-it/markdown-it>
   [Ace Editor]: <http://ace.ajax.org>
   [node.js]: <http://nodejs.org>
   [Twitter Bootstrap]: <http://twitter.github.com/bootstrap/>
   [jQuery]: <http://jquery.com>
   [@tjholowaychuk]: <http://twitter.com/tjholowaychuk>
   [express]: <http://expressjs.com>
   [AngularJS]: <http://angularjs.org>
   [Gulp]: <http://gulpjs.com>

   [PlDb]: <https://github.com/joemccann/dillinger/tree/master/plugins/dropbox/README.md>
   [PlGh]: <https://github.com/joemccann/dillinger/tree/master/plugins/github/README.md>
   [PlGd]: <https://github.com/joemccann/dillinger/tree/master/plugins/googledrive/README.md>
   [PlOd]: <https://github.com/joemccann/dillinger/tree/master/plugins/onedrive/README.md>
   [PlMe]: <https://github.com/joemccann/dillinger/tree/master/plugins/medium/README.md>
   [PlGa]: <https://github.com/RahulHP/dillinger/blob/master/plugins/googleanalytics/README.md>
