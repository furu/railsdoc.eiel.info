---
title: ActionDispatch::Cookies
---

```
$ ruby -v
ruby 2.1.0p0 (2013-12-25 revision 44422) [x86_64-darwin13.0]
```

```
bundle exec ruby -r action_pack -e 'puts ActionPack::VERSION::STRING'
4.1.0.rc1
```

* [ソースコード](https://github.com/rails/rails/blob/v4.1.0.rc1/actionpack/lib/action_dispatch/middleware/cookies.rb)

ActionDispatch::Request に #cookie_jar メソッドを追加する。
このメソッドは `env['action_dispatch.cookies']` に CookieJar のインスタンスを格納する。


ActionDispatch::Cookies::ChainedCookieJars
--------------------------------------------------------------------------------

### permament

20年間保持するクッキーを生成できる模様。

### signed

署名された情報をクッキーに保存できる模様

### encrypted

暗号化された情報をクッキーに保存できる模様。

### signed_or_encrypted

秘密鍵があれば暗号化に、そうでなければ署名になる。

ActionDispatch::Cookies::VerifyAndUpgradeLegacySignedMessage
--------------------------------------------------------------------------------

古いタイプの署名をアップグレードするための仕組みがはいってるみたい。


ActionDispatch::Cookies::CookieJar
--------------------------------------------------------------------------------

オブジェクトを作成するヘルパーとして .build がある。
env より値を取り出してオブジェクトを構築する。

Enumerable になっていて複数の cookie として保存した値を渡りあるける。

ActionDispatch::Cookies::PermanentCookieJar
--------------------------------------------------------------------------------

ChainedCookieJars をミックスインしてる。永続化したことを考えると「なるほどな」と思った。
コンストラクタで渡してる key_generator はなにに使うんだ…

ActionDispatch::Cookies::JsonSerializer
--------------------------------------------------------------------------------

クラスメソッドしかなくて JSON へのラッパしかない。
.load と .dump がシリアライザとの規約になってるんだろうと思われる。

ActionDispatch::Cookies::NullSerializer
--------------------------------------------------------------------------------

なにもしない。 .load と .dump というメソッドがあるだけ。


ActionDispatch::Cookies::SerializedCookieJars
--------------------------------------------------------------------------------

シリアライズできる CookieJar をつくるときミックスインするんじゃないかと思う。
シリアライザーは options[:serializer] で指定することができてデフォルトでは Marshal を利用する。

:hypbrid や :json を指定すると JsonSerializer が使用されます。

ActionDispatch::Cookies::SignedCookieJar
--------------------------------------------------------------------------------

署名された CookieJar を作りたいときに使用する


ActionDispatch::Cookies::UpgradeLegacySignedCookieJar
--------------------------------------------------------------------------------

古い SingendCookieJar で作成されたものアップグレードする模様。


ActionDispatch::Cookies::EncryptedCookieJar
--------------------------------------------------------------------------------

暗号化した CookieJar を作りたいときに使用する。

ActionDispatch::Cookies::UpgradeLegacyEncryptedCookieJar
--------------------------------------------------------------------------------

古い EncryptedCookieJar で作成されたものをアップグレードする模様。
