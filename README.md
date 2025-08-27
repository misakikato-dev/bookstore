# Bookstore (Spring Boot)

## 概要
Spring Bootで作成したシンプルな本棚アプリです。  
書籍の **登録・一覧表示・削除・編集・マイ本棚管理** ができるCRUDアプリケーション。  
フロントには **Thymeleaf** と **Bootstrap** を利用し、見やすいUIを実現しています。  
DBは **MySQL** を利用（デモ用途ではH2に切り替え可能）。

---

## 主な機能
- 書籍を新規登録（タイトル、著者、価格を入力）
- 書籍一覧の表示
- 書籍の削除・編集
- マイ本棚画面でお気に入り書籍を管理

---

## 技術スタック
- Java 17  
- Spring Boot  
- Spring MVC  
- Spring Data JPA  
- Thymeleaf  
- Bootstrap 5  
- MySQL（H2 Databaseにも対応）

---

 ## プロジェクト構成
 src/main/java/com/bookStore
├─ BookStoreApplication.java # メインアプリケーション
├─ controller/
│ ├─ BookController.java
│ └─ MyBookListController.java
├─ entity/
│ ├─ Book.java
│ └─ MyBookList.java
├─ repository/
│ ├─ BookRepository.java
│ └─ MyBookRepository.java
└─ service/
├─ BookService.java
└─ MyBookListService.java

src/main/resources
├─ templates/
│ ├─ home.html
│ ├─ bookList.html
│ ├─ bookEdit.html
│ ├─ bookRegister.html
│ └─ myBooks.html
└─ application.properties

---

## 実行方法（ローカル）
1. リポジトリをclone  
   ```bash
   git clone https://github.com/jdshhg58djkshK/bookstore.git
   cd bookstore

2. データベース設定（例: H2を使う場合は application.properties を修正）

spring.datasource.url=jdbc:h2:mem:testdb
spring.datasource.driverClassName=org.h2.Driver
spring.jpa.database-platform=org.hibernate.dialect.H2Dialect
spring.h2.console.enabled=true

3. アプリを起動
./mvnw spring-boot:run
# または
mvn spring-boot:run


4. ブラウザでアクセス
http://localhost:1010/

---

##主なエンドポイント

/ … ホーム画面
/books … 書籍一覧
/book_register … 書籍登録フォーム
/save … 書籍保存処理
/delete/{id} … 書籍削除
/edit/{id} … 書籍編集
/my_books … マイ本棚

