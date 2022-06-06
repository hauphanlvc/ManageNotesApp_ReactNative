# ManageNotesApp_ReactNative

Bước 1: Clone repo như ở dưỡi
```
    git clone https://github.com/hauphanlvc/ManageNotesApp_ReactNative
    cd ManageNotesApp_ReactNative
```
Bước 2: Đảm bảo điện thoại android đã bật chế độ USB debugging trong phần cài đặt developer option và đã kết nối với máy tính (ta có thể kham khảo ở đây https://reactnative.dev/docs/running-on-device#1-enable-debugging-over-usb-2).

```
    docker run -it -d --network=host --name managenotesapp -v $(pwd)/ManageNotesApp:/managesnotesapp reactnativecommunity/react-native-android
```
Bước 3: Sau khi chạy bước trên,  docker container **managenotesapp** sẽ chạy trong background, để có thể chạy được trên app, ta thực hiện như sau:
```
docker exec -it managenotesapp /bin/bash   
cd /managesnotesapp
npx react-native run-android
```
