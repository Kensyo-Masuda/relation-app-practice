# relation-app-practice

## 概要

COACHTECH 教材 Tutorial 9-5「リレーション ハンズオン演習」で作成した成果物です。

Post・Comment・TagなどのModel間のリレーションを設定し、関連するデータの取得や表示を行いました。

## 使用技術

* PHP 8.x
* Laravel 10.x
* Eloquent ORM（hasMany / belongsTo / belongsToMany）
* MySQL
* Docker / Laravel Sail

## 学んだこと

* `hasMany`、`belongsTo`、`belongsToMany`を使ってModel同士の関係を設定する方法を学びました。
* `with()`を使ったEager Loadingや、`withCount()`で関連データの件数を取得する方法を学びました。
* `whereHas()`や`whereDoesntHave()`を使って、リレーション先の条件でデータを絞り込む方法を学びました。

## 動作確認

### 1. プロジェクトへ移動

```bash
cd ~/laravel-practice/9-5-5_hands-on/relation-app-practice
```

### 2. Laravelを起動

```bash
./vendor/bin/sail up -d
```

### 3. ブラウザで確認

ブラウザで以下にアクセスします。

```text
http://localhost/posts
```

投稿一覧が表示され、コメント数やタグなどの関連データが確認できます。

### 4. Tinkerでリレーションを確認

```bash
./vendor/bin/sail artisan tinker
```

TinkerでModelを読み込みます。

```php
use App\Models\Post;
use App\Models\Tag;
use App\Models\Comment;
```

### 5. 作業終了

```bash
./vendor/bin/sail down
```
