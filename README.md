# 書店アプリ (Spring Boot)

## 概要
このプロジェクトは Spring Boot を使った簡単な書店デモアプリです。
基本的な CRUD 操作をサポートし、テンプレートには Thymeleaf、スタイルには Bootstrap を使用しています。
デフォルトはポートフォリオ用に H2（インメモリ）で動作しますが、MySQL に切り替えて運用することもできます。
---

## 機能
- 書籍の一覧表示、登録、編集、削除
- マイリストへの追加／削除

## 技術スタック
- Java 17
- Spring Boot
- Spring MVC / Spring Data JPA
- Thymeleaf
- Bootstrap 5
- データベース: H2（デフォルト）、MySQL（切替可能）

---

## 謚陦薙せ繧ｿ繝?繧ｯ
- Java 17  
- Spring Boot  
- Spring MVC  
- Spring Data JPA  
- Thymeleaf  
- Bootstrap 5  
- MySQL?ｼ?H2 Database縺ｫ繧ょｯｾ蠢懶ｼ?
---

## ディレクトリ構成（抜粋）

```
src/main/java/com/bookStore
   BookStoreApplication.java
   controller/
      BookController.java
      MyBookListController.java
   entity/
      Book.java
      MyBookList.java
   repository/
      BookRepository.java
      MyBookRepository.java
   service/
      BookService.java
      MyBookListService.java

src/main/resources
   templates/
      home.html
      bookList.html
      bookEdit.html
      bookRegister.html
      myBooks.html
   application.yml (profile based)
```

## 螳溯｡梧婿豕包ｼ医Ο繝ｼ繧ｫ繝ｫ?ｼ?
1. 繝ｪ繝昴ず繝医Μ繧団lone  
 ```text
   git clone https://github.com/misakikato-dev/bookstore.git
   cd bookstore
```

2. 起動（H2 デフォルト）

```
./mvnw spring-boot:run
```

H2 コンソールを有効にしておくとブラウザでデータを確認できます（デフォルト設定を application-h2.yml に記載）。

3. ローカルアクセス例

```
http://localhost:8080/
```

4. 繝悶Λ繧ｦ繧ｶ縺ｧ繧｢繧ｯ繧ｻ繧ｹ
 ```text
   http://localhost:1010/
```
---

## 荳ｻ縺ｪ繧ｨ繝ｳ繝峨?昴う繝ｳ繝?
   
   ```python
   / 窶ｦ 繝帙?ｼ繝?逕ｻ髱｢
   /books 縲縲縲縲縲窶ｦ 譖ｸ邀堺ｸ隕ｧ
   /book_register  窶ｦ 譖ｸ邀咲匳骭ｲ繝輔か繝ｼ繝?
   /save           窶ｦ 譖ｸ邀堺ｿ晏ｭ伜?ｦ逅?
   /delete/{id}    窶ｦ 譖ｸ邀榊炎髯､
   /edit/{id}      窶ｦ 譖ｸ邀咲ｷｨ髮?
   /my_books       窶ｦ 繝槭う譛ｬ譽?
   ```

