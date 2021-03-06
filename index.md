---
title: Home
---

Rails メモ
--------------------------------------------------------------------------------

ここは Rails の勉強メモとかになる予定です。
自分のメモなので間違いなどもたくさんあるかもしれませんので、参考にする程度にしておくことをオススメします。

基本的に Rails4 を想定しています。

広島Ruby勉強会での資料として利用したものを日々更新中。

* [更新履歴](https://github.com/eiel/railsdoc.eiel.info/commits/master)

### ActiveSupport Core Ext のメソッド紹介。

* [Core Ext - Array](/active_support/core_ext/array)
* [Core Ext - Benchmark](/active_support/core_ext/benchmark)
* [Core Ext - BigDecimal](/active_support/core_ext/big_decimal)
* [Core Ext - Class](/active_support/core_ext/class)
* [Core Ext - Date](/active_support/core_ext/date)
* [Core Ext - DateTime](/active_support/core_ext/date_time)
* [Core Ext - Date and Time](/active_support/core_ext/date_and_time)
* [Core Ext - Enumerable](/active_support/core_ext/enumerable)
* [Core Ext - File](/active_support/core_ext/file)
* [Core Ext - Hash](/active_support/core_ext/hash)
* [Core Ext - InfiniteComparable](/active_support/core_ext/infinite_comparable)
* [Core Ext - integer](/active_support/core_ext/integer)
* [Core Ext - Kernel](/active_support/core_ext/kernel)
* [Core Ext - LoadError](/active_support/core_ext/load_error)
* [Core Ext - Marshal](/active_support/core_ext/marshal)
* [Core Ext - Module](/active_support/core_ext/module)
* [Core Ext - Numeric](/active_support/core_ext/numeric)
* [Core Ext - NameError](/active_support/core_ext/name_error)
* [Core Ext - Object](/active_support/core_ext/object)
* [Core Ext - Range](/active_support/core_ext/range)
* [Core Ext - Regexp](/active_support/core_ext/regexp)
* [Core Ext - String](/active_support/core_ext/string)
* [Core Ext - Struct](/active_support/core_ext/struct)
* [Core Ext - Thead](/active_support/core_ext/thread)
* [Core Ext - Time](/active_support/core_ext/time)
* [Croe Ext - URI](/active_support/core_ext/uri)

### ActiveSupport の機能

ActiveSupport は Rails で利用されるユーティリティ集です。
他の rails の gem には依存していません。

* [Lazy Load Hooks](/active_support/lazy_load_hooks)
* [LoggerSilencer](/active_support/logger_silencer)

### ActiveSupport に定義されているクラス/モジュール

* [ActiveSupport::Autoload モジュール](/active_support/dependencies/autoload/)
* [ActiveSupport::BacktraceCleaner クラス](/active_support/backtrace_cleaner)
* [ActiveSupport::Benchmarkable](/active_support/benchmarkable)
* [ActiveSupport::Cache モジュール](/active_support/cache)
* [ActiveSupport::Callbacks モジュール](/active_support/callbacks)
* [ActiveSupport::Concern モジュール](/active_support/concern)
* [ActiveSupport::Configuration モジュール](/active_support/configuration)
* [ActiveSupport::Dependencies モジュール](/active_support/dependencies)
* [ActiveSupport::Deprecation クラス](/active_support/deprecation)
* [ActiveSupport::DescendantsTracker モジュール](/active_support/descendants_tracker)
* [ActiveSupport::FileUpdateChecker クラス](/active_support/file_update_checker)
* [ActiveSupport::Gzip クラス](/active_support/gzip)
* [ActiveSupport::Inflection モジュール](/active_support/inflection)
* [ActiveSupport::Inflector モジュール](/active_support/inflector)
* [ActiveSupport::I18n モジュール](/active_support/i18n)
* [ActiveSupport::JSON モジュール](/active_support/json)
* [ActiveSupport::KeyGenerator](/active_support/key_generator)
* [ActiveSupport::Logger クラス](/active_support/logger)
* [ActiveSupport::LogSubscriber クラス](/active_support/log_subscriber)
* [ActiveSupport::MessageEncrypt](/active_support/message_encrypt)
* [ActiveSupport::MessageVerifier](/active_support/message_verifier)
* [ActiveSupport::Multibyte](/active_support/multibyte)
* [ActiveSupport::Notifications クラス](/active_support/notifications)
* [ActiveSupport::OptionMerger クラス](/active_support/option_merger)
* [ActiveSupport::OrderedOptions クラス](/active_support/ordered_options)
* [ActiveSupport::OrderedHash クラス](/active_support/ordered_hash)
* [ActiveSupport::PerThreadRegistry モジュール](/active_support/per_thread_registry)
* [ActiveSupport::ProxyObject](/active_support/proxy_object)
* [ActiveSupport::Rescuable](/active_support/rescuable)
* [ActiveSupport::StringInquirer](/active_support/string_inquiry)
* [AcitveSupport::Subscribers クラス](/active_support/subscriber)
* [ActiveSupport::TaggedLogging クラス](/active_support/tagged_logging)
* [ActiveSupport::TimeWithZone クラス](/active_support/time_with_zone)
* [ActiveSupport::XmlMini クラス](/active_support/xml_mini)

### ActionPack

ActionPack は ActiveSupport に依存しています。
また

* `AbstractController`
* `ActienController`
* `ActienDispatch`
* `ActienView`

をまとめたものになってます。

### AbstarctController

ActionController と ActionMailer の同一コード部分をまとめたものと聞いたことがある。
[AbstractController::Base](https://github.com/rails/rails/blob/4-0-stable/actionpack/lib/abstract_controller/base.rb) からみていくと良い。

* [AbstractController::Base](/abstarct_controller/base)
* [AbstractController::Callbacks](/abstarct_controller/callbacks)
* [AbstractController::Collector](/abstarct_controller/collector)
* [AbstractController::Helpers](/abstarct_controller/helpers)
* [AbstractController::Layouts](/abstract_controller/layouts)
* [AbstroctController::Rendering](/abstract_controller/rendering)
* [AbstractController::ViewPaths](/abstract_controller/view_paths)

### ActionView

* [ActionView::Resolver](/action_view/template/resolver)

### 勉強会資料

* [広島Ruby勉強会 #32](/hiroshimarb/22)
* [広島Ruby勉強会 #33](/hiroshimarb/23)
