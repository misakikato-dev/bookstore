# 📚 書籍管理アプリ（Spring Boot）

## 🌐 公開アプリ
🚀 **デプロイ先（Render）**  
👉 [https://bookstore-3wpn.onrender.com](https://bookstore-3wpn.onrender.com)

> 初回アクセス時は Render Free プランのため、起動に数十秒かかる場合があります。

## 📝 概要
このプロジェクトは **Spring Boot** を使った書籍管理アプリです。  
基本的な CRUD 操作（登録・更新・削除・一覧表示）を行い、  
テンプレートエンジンに **Thymeleaf**、デザインに **Bootstrap 5** を使用しています。  

デフォルトでは **H2（インメモリデータベース）** で動作し、  
本番環境では **MySQL** に切り替えて運用することも可能です。

---

## ⚙️ 機能一覧
- 書籍の一覧表示  
- 書籍の登録・編集・削除  
- マイリストへの追加・削除  

---

## 🧩 技術スタック
| 分類 | 使用技術 |
|------|-----------|
| 言語 | Java 17 |
| フレームワーク | Spring Boot 3 / Spring MVC / Spring Data JPA |
| テンプレート | Thymeleaf |
| デザイン | Bootstrap 5 |
| データベース | H2（デフォルト） / MySQL（切替可） |
| ビルドツール | Maven |
| デプロイ先 | Render（Docker） |

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
- ブラウザで以下にアクセスしてアプリを確認できます：
http://localhost:1010/

- H2コンソールも利用可能です👇
http://localhost:1010/h2-console

☁️ 環境切り替え（H2 → MySQL）
application.properties 内の設定を切り替えて使用します。
- H2設定（デフォルト）
```bash
spring.datasource.url=jdbc:h2:mem:testdb
spring.datasource.driver-class-name=org.h2.Driver
spring.datasource.username=sa
```

- MySQL設定（コメントアウトを解除）
```bash
spring.datasource.url=${DB_URL}
spring.datasource.username=${DB_USER}
spring.datasource.password=${DB_PASSWORD}
```

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
