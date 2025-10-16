# 📚 書籍管理アプリ（Spring Boot）

## 📝 概要
このプロジェクトは **Spring Boot** を使った簡単な書籍管理アプリです。  
基本的な CRUD 操作（登録・更新・削除・一覧表示）を行い、  
テンプレートには **Thymeleaf**、デザインには **Bootstrap 5** を使用しています。  

デフォルトでは **H2（インメモリデータベース）** で動作し、  
本番環境では **MySQL** に切り替えて運用することも可能です。

---

## ⚙️ 機能一覧
- 書籍の一覧表示  
- 書籍の登録・編集・削除  
- マイリストへの追加・削除  

---

## 🧩 技術スタック
- Java 17  
- Spring Boot 3  
- Spring MVC / Spring Data JPA  
- Thymeleaf  
- Bootstrap 5  
- データベース: H2（デフォルト）、MySQL（切替可能）

---

## 📁 ディレクトリ構成（抜粋）
- src/main/java/com/bookStore
```bash
・BookStoreApplication.java

・controller/
　　- BookController.java
　　- MyBookListController.java

・entity/
   - Book.java
   - MyBookList.java

・repository/
   -BookRepository.java
   - MyBookRepository.java

・service/
   - BookService.java
   - MyBookListService.java
```

- src/main/resources
```bash
・templates/
   - home.html
   - bookList.html
   - bookRegister.html
   - myBooks.html

・application.properties
```


---

## 🚀 起動手順

### 1️⃣ プロジェクトをクローン

```bash
git clone https://github.com/misakikato-dev/bookstore.git
cd bookstore
```

### 2️⃣ ビルド & 実行（H2使用時

```bash
mvn spring-boot:run
```
・ブラウザで以下にアクセスしてアプリを確認できます：
http://localhost:1010/

・H2コンソールも利用可能です👇
http://localhost:1010/h2-console

☁️ 環境切り替え（H2 → MySQL）
・application.properties 内のH2設定をコメントアウト
・MySQL用設定を有効化
・環境変数で以下を設定
　　DB_URL、DB_USER、DB_PASSWORD

🌐 主なエンドポイント一覧
| エンドポイント    | 説明       |
| ---------------- | -------- |
| `/`              | ホーム画面    |
| `/books`         | 書籍一覧表示   |
| `/book_register` | 書籍登録フォーム |
| `/save`          | 書籍の保存    |
| `/delete/{id}`   | 書籍の削除    |
| `/edit/{id}`     | 書籍の編集    |
| `/my_books`      | マイリスト表示  |
