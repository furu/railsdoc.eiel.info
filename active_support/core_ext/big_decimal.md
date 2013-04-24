---
title: Core Ext BigDecimal
---
ActiveSupport 拡張で追加される BigDecimal のメソッドの紹介
================================================================================

試した環境

```
$ ruby -v
ruby 2.0.0p0 (2013-02-24 revision 39474) [x86_64-darwin12.2.1]
```

```
$ bundle exec ruby -r active_support -e 'puts ActiveSupport::VERSION::STRING'
4.0.0.beta1
```

Array へ機能を追加する方法

```ruby
require 'active_support/core_ext/big_decimal'
```

[BigDecimal](http://rurema.clear-code.com/query:BigDecimal/) は可変長不動小数点クラスです。

Conversion
--------------------------------------------------------------------------------

変換に関するメソッドが集約されてます。他にないけど。

[ソースコード](https://github.com/rails/rails/blob/v4.0.0.beta1/activesupport/lib/active_support/core_ext/big_decimal/conversions.rb)

### encode_with(corder)

YAMLにエンコードする再に呼ばれるメソッドです。
Infinity や NaN への対応処理がされてます。

### to_d

BigDecimal に変換するメソッドです。定義されていない環境の場合に生成します。
self を返すだけ。

### to_formatted_s(*args)

引数を指定しなければ、指数を使わない形式で出力されます。また、symbol を渡した場合は スーパークラスに処理を委譲します。 試したら、結果は同じでした。

また、BigDecimal#to_s のフォーマットの文字列を渡してもちゃんと動作します。

他の to_formatted_s と同様 to_s に差し替えられています。

```ruby
b = BigDecimal.new('0.1')
b.to_formatted_s           # => "0.1"
b.to_s                     # => "0.1"

b.to_s 'E'                 # => "0.1E0"
b.to_s :db                 # => "0.1"
```