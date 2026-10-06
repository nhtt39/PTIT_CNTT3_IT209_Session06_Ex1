# Session 06 - Exercise 1

## 1. Các lệnh tạo thư mục

Tạo thư mục `/var/www/my-app` gồm hai thư mục `public` và `logs`:

```bash
sudo mkdir -p /var/www/my-app/public
sudo mkdir -p /var/www/my-app/logs
```

### Hình ảnh thực hiện

(./images/tao-thu-muc.png)
## 2. Gán quyền và Owner/Group

### Gán quyền cho thư mục `public`

```bash
sudo chmod 750 /var/www/my-app/public
```

Quyền:

```text
drwxr-x---
```

### Gán quyền cho thư mục `logs`

```bash
sudo chmod 770 /var/www/my-app/logs
```

Quyền:

```text
drwxrwx---
```

### Gán Owner và Group

```bash
sudo chown -R $USER:www-data /var/www/my-app
```

### Hình ảnh thực hiện

(./images/gan-quyen.png) 
## 3. Kết quả kiểm tra

Kiểm tra Owner, Group và quyền của các thư mục:

```bash
ls -la /var/www/my-app
```

Kết quả mong muốn:

```text
drwxr-x--- 750 <owner> www-data /var/www/my-app/public
drwxrwx--- 770 <owner> www-data /var/www/my-app/logs
```

### Hình ảnh kết quả

(./images/ket-qua.png)
