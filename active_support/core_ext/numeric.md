---
title: Core Ext Numeric
---

試した環境

```
$ ruby -v
ruby 2.0.0p0 (2013-02-24 revision 39474) [x86_64-darwin12.2.1]
```

```
$ bundle exec ruby -r active_support -e 'puts ActiveSupport::VERSION::STRING'
4.0.0.rc1
```

Module へ機能を追加する方法

```ruby
require 'active_support/core_ext/numeric'
```

Bytes
--------------------------------------------------------------------------------

Byte, KByte などを便利に扱うメソッドが定義されています。

```ruby
require 'active_support/core_ext/numeric/bytes'
```

* [ソースコード](https://github.com/rails/rails/blob/v4.0.0.rc1/activesupport/lib/active_support/core_ext/numeric/bytes.rb)

### #bytes

self バイトが何バイトか返します。

```ruby
10.bytes   # => 10
```

byte というエイリアスがあります。

### #kilobytes

self キロバイトが何バイトか返します。

```ruby
10.kilobytes   # => 10240

kilbyte というエイリアスがあります。
```

### #megabytes

self メガバイトが何バイトか返します。

```ruby
10.megabytes   # => 10485760
```

megabyte というエイリアスがあります。

### #gigabytes

self ギガバイトが何バイトか返します。

```ruby
10.gigabytes   # => 10737418240
```

gigabyte というエイリアスがあります。

### #terabytes

self テラバイトが何バイトか返します。

```ruby
10.terabytes   # => 10995116277760
```

terabyte というエイリアスがあります。

### #petabytes

self ペタバイトが何バイトか返します。

```ruby
10.petabytes   # => 11258999068426240
```

petaabyte というエイリアスがあります。

### #exabytes

self エクサバイトが何バイトか返します。

```ruby
10.exabytes   # => 11529215046068469760
```

exabyte というエイリアスがあります。


Conversions
--------------------------------------------------------------------------------

数値から別の型へ変換するメソッドが定義されています。

この機能だけ読み込む方法

```ruby
require 'active_support/core_ext/numeric/conversions'
```

* [ソースコード](https://github.com/rails/rails/blob/v4.0.0.rc1/activesupport/lib/active_support/core_ext/numeric/conversions.rb)

### to_formatted_s

* to_formatted_s(format = :default, options = {})

数値を文字列に変換します。
引数formatには :phone, :currency, :percentage, :delimited, :rounded, :human, human_size を与えることができます。
それぞれの処理は `ActiveSupport::NumberHelper.number_to_xxxxx` に委譲されます。

Numeric だけでなく Float Fixnum Bignum BigDecimal も同じメソッドが定義されます。

* [ActiveSupport::NumberHelper](/active_support/number_helper)

Infinite Comparable
--------------------------------------------------------------------------------

Float BigDecimal が Float::INFINITY などと比較できるようにします。

この機能のみ利用したい場合は:

```ruby
require 'active_support/core_ext/numeric/infinite_comparable'
```

とします。

* [ソースコード](https://github.com/rails/rails/blob/v4.0.0.rc1/activesupport/lib/active_support/core_ext/numeric/infinite_comparable.rb)

require される ライブラリ

* [active_support/core_ext/infinite_comparable](/active_support/core_ext/infinite_comparable)

Time
--------------------------------------------------------------------------------

数値から`期間`を示す[ActiveSupport::Duraction](/active_support/dulation/)を生成するメソッドが実装されています。
`from_now` や `ago` にメソッドチェインすると日付オブジェクトを生成できます。

この機能のみ利用したい場合は:

```ruby
require 'active_support/Core_ext/numeric/time'
```

### seconds

`self` 秒間を返します。

second というエイリアスがあります。

### minutes

`self` 分間を返します。

minute というエイリアスがあります。

### hours

`self` 時間を返します。

hour というエイリアスがあります。

### days

`self` 日間を返します。

day というエイリアスがあります。

### weeks

`self` 週間を返します。

week というエイリアスがあります。

### fortnights

`self` * 2週間を返します。

fortnight というエイリアスがあります。

### ago

* ago(time = ::Time.current)

引数timeから `self` 秒前を返します。

until というエイリアスがあります。

### since

* since(time = ::Time.current)

引数timeから `self` 秒後を返します。

from_now というエイリアスがあります。
