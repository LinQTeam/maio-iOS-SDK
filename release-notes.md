# Release Notes

## v1.6.3 (2022-10-27)
- 排他制御の問題で、一部予期せぬクラッシュが発生する問題に対応しました。

## v1.6.2 (2022-06-02)
- プレイアブル広告におけるアプリ内ストア表示の振る舞いについて、一部修正しました。

## v1.6.1 (2022-03-29)
- 多数のゾーンを利用しているメディアにおいて、広告リソースを多重にダウンロードしてしまう場合がある問題を修正しました。

## v1.6.0 (2021-12-09)
- SKAdNetwork View Through トラッキングに必要な対応を実施しました。
- アプリケーションがバックグラウンドに入った際の通信量を削減する対応を実施しました。

## v1.5.8 (2021-06-15)
- アプリケーションに登録されているSKAdNetworkIdが多数にわたる場合に、不具合が発生する問題を修正しました。

## v1.5.7 (2021-06-10)
- SKAdNetworkに対応するため、内部の挙動を更新しました。

## v1.5.6 (2020-11-26)
- 特定の場面で、稀にクラッシュが発生する問題を修正しました。

## v1.5.5 (2020-08-27)
- iOS 14の仕様変更により、従来の挙動ではIDFAの取得ができなくなる問題を解決します。
- プレイアブル広告の新しい挙動に対応します。

## v1.5.4 (2020-05-21)
- 広告のエンドカードを連打した際、稀にクラッシュしてしまう問題を修正しました。

## v1.5.3 (2020-01-28)
- 特定の、特殊な環境下においてクラッシュする問題に対処しました。

## v1.5.2 (2019-12-16)
- 特定のプレイアブル広告からアプリ内ストアを開いた場合に、進行不能になる問題を修正しました。
- 音声の出力先情報を取得するようになりました。

## v1.5.1 (2019-11-18)
- iOS 13にて、maioDidClosedが二重に呼ばれる問題を修正しました。
- 横向き専用のアプリでエンドカードのインストールボタンをタップするとクラッシュする問題を修正しました。
    - 横向き専用のアプリでアプリ内ストア表示を行わないようにしました。

## v1.5.0 (2019-10-15)
- Xcode11でビルドした場合、iOS13で画面上に出ないまま広告が再生されてしまう問題を修正しました。
    - Xcode11(iOS Base SDK 13)からライフサイクルに関する仕様変更によるものです。
    - 本バージョン以降の利用にはXcode11が必要になります。

## v1.4.8 (2019-09-18)
- Xcode11におけるStoreKitの仕様変更により、iOS13でクラッシュしてしまう問題を修正。

## v1.4.7 (2019-06-27)
- 広告リソースのダウンロードにおいて、稀にNSFileHandleOperationExceptionがthrowされる現象に対応しました。

## v1.4.6 (2019-04-22)
- アプリ内ストアを閉じた際に画面が意図しない向きになる場合がある問題を修正。

## v1.4.5 (2019-02-14)
- v1.4.2以降、アプリ内でのストア表示を再度行った場合に表示が崩れることがある問題を修正。

## v1.4.4 (2019-01-29)
- v1.4.3にて、iOS 10未満の環境でクラッシュが発生してしまう問題を修正。

## v1.4.3 (2019-01-24)
- WebViewをWKWebViewに統一しました。

## v1.4.2 (2018-12-04)
- アプリ内でストアを表示する際のユーザー体験を改善しました。
- 特定の条件下において、クリック数値の計測に不足が発生する場合がある不具合を修正しました。

## v1.4.1 (2018-09-28)
- iOS 8.xかつ、プレイアブルアドの場合において、特定の操作を行うと広告の再生終了ボタンが隠れてしまう不具合を修正しました。
- iPhoneXS MaxおよびXRにおいてプレイアブルアドの表示が一部崩れてしまう不具合を修正しました。
- 端末の回転ロックをかけた状態で、横向き固定のアプリケーションからmaioを再生した場合に天地が逆さまに再生されることがある不具合を修正しました。

## v1.4.0 (2018-08-28)
- canShowAtZoneId:,showAtZoneIdに間違ったゾーンIDを与えた場合の挙動を変更しました。
  テストモードが有効な場合において、`throw exception`を実施しておりましたが、
  テストモードに関わらず、didFail:reason: を用いて通知するようになりました。
- deprecatedな処理に由来する、稀にクラッシュが発生する現象に対処しました。

## v1.3.2 (2018-07-10)
- 稀に発生する不具合を修正しました。
- プレイアブルアド機能を拡充しました。

## v1.3.1 (2018-06-11)
- SSZipArchive, minizip利用環境下で、duplicate symbolエラーが発生してしまう現象に対処しました。

## v1.3.0 (2018-05-29)
- プレイアブルアドに対応しました。
- 複数のdelegateに対して通知を送れるようになりました。（詳細はAPIリファレンスを参照）

## v1.2.19 (2018-01-16)
- 広告の再生時、ステータスバーが見えてしまう現象が発生していたため、これを修正。

## v1.2.18 (2017-11-01)
- v1.2.17の改修において、iOS 9.1未満でクラッシュしてしまう不具合が発生したため、これを修正。

## v1.2.17 (2017-10-18)
- 環境によって広告再生中にステータスバーが表示されてしまう不具合があったため、これを修正。
- 稀に正しくない矩形情報で広告が再生される場合があったため、これに対処。

## v1.2.16 (2017-10-05)
- iPhoneXにて広告が大きく崩れる場合があったため、これを修正。

## v1.2.15 (2017-09-25)
- Xcode8にてビルドできない不具合があったため、これを修正。

## v1.2.14 (2017-09-22)
- iOS 11 にて、エンドカードの表示が崩れる不具合があったため、これを修正。

## v1.2.13 (2017-09-11)
- iOS SDK v1.2.8以前からアップデートした際、`Other Linker Flags`に`-Wl,-no_compact_unwind`が指定されている場合に、クラッシュしてしまうことがあったため、ごれを修正。
- 広告リソースをダウンロードした際に、破損してしまう事があったため、これを修正。
- iOS8.xでのみ、広告の表示が崩れる場合があったため、これを修正。

## v1.2.12 (2017-06-15)
- iOS8未満の端末にて、広告の描画が崩れる不具合があったため、これを修正。
- まれにクラッシュするケースがあったため、これを修正。

## v1.2.11 (2017-06-05)
- 意図しない画面の回転を防ぐため、内部の設計を一部変更しました。

## v1.2.10 (2017-04-25)
- 軽微な不具合を修正しました。

## v1.2.9 (2017-04-19)
- まれにキャッシュ消失による広告動画再生失敗エラーが発生する場合があったため、これを修正しました。
- ディスクの空き容量が足りない場合にクラッシュしてしまう点を修正しました。

## v1.2.8 (2017-03-10)
- 縦向きの動画広告がフルスクリーンではない状態で再生が開始される場合があったため、これを修正しました。

## v1.2.7 (2017-02-28)
- エラーログディレクトリの生成処理に不具合があったため、これを修正しました。

## v1.2.6 (2017-02-17)
- テストモードにおいて、SDK初期化開始直後にcanShowAtZoneId:を呼んでもクラッシュしないようにしました。
- 動画広告を再生できなかった場合に、エラーログを残すようにしました。

## v1.2.5 (2017-01-19)
- 横向き固定のアプリケーションにて、エンドカードのダウンロードボタンをタップするとクラッシュしてしまう不具合があったため、これを修正。
- SDK初期化中において、全てのゾーンの準備が整うのを待たずにmaioDidChangeCanShow:newValue:イベントを呼ばれるよう、これを改善しました。

## v1.2.4 (2016-12-22)
- iOS7以下において、広告からストアに遷移した場合、アプリに戻っても操作できなくなる不具合があったため、これを修正。

## v1.2.3 (2016-12-21)
- 内部でダウンロードした広告リソースの検証に一部不具合があったため、これを修正。
- 動画広告の再生準備中、クラッシュする可能性があったので、これを修正。

## v1.2.2 (2016-12-15)
- 動画広告の再生エラーにより広告が閉じられる際にクラッシュする可能性があったので、これを修正。
- スレッドセーフにデザインされたクラス内に一部スレッドセーフでない処理が入っていたので、これを修正。

## v1.2.1 (2016-12-09)
- 動画広告の再生準備に失敗し再生が行われないケースがあったので、これを修正。

## v1.2.0 (2016-12-09)
- ストア遷移時に、アプリ内でストアを開くように変更。

## v1.1.7 (2016-11-09)
- UINavigationController 等から広告を表示すると、広告クローズ時に正しい InterfaceOrientation に戻れない場合があるので、これが端末向きとなるよう修正。
- 同一メディアに多数のゾーンが存在する場合、SDK の初期化に必要以上の時間がかかる事があるので、これを修正。
- [Maio showAtZoneId:vc:] メソッドの vc に渡された値が、v1.1.3 以降 使用されていなかった不具合を修正。

## v1.1.6 (2016-08-25)
- ビルド時に「warning: /var/folders/xxx: No such file or directory」が大量に生じる問題を修正。
- SDK のファイルサイズを最適化。

## v1.1.5 (2016-08-03)
- HTTP ステータス 503 などで無効なメディア情報をダウンロードすると、ダウンロードマネージャの最大同時リクエスト数設定が 0 となり配信サーバへのリクエストが行われなくなる場合があるので、これを修正。
- 動画画面を閉じた後も dealloc が呼ばれず、直ぐに関連リソースが解放されない場合があるので、明示的に解放するよう修正。
- アプリを再起動しないとメモリ上にキャッシュしたメディア情報を使い続ける不具合を修正。
- 一部処理の最適化と、軽微な不具合の修正。

## v1.1.4 (2016-07-28)
- cocos2d-x-3.12 未満では AppDelegate に window プロパティが実装されていない為、"[AppController window]: unrecognized selector" となりクラッシュするので、それを回避。
https://github.com/cocos2d/cocos2d-x/issues/13285

## v1.1.3 (2016-07-15)
- Unity 経由で maio の動画広告を再生完了させた際、アプリをバックグラウンド→フォアグラウンドで遷移させると、エンドカードの裏側で勝手に動画が再開されてしまう不具合を修正。
- UIViewController の存在しない、または window ヒエラルキーに存在しない UIWindow から [Maio show] 系メソッドを呼び出すと、動画広告に遷移できない不具合を修正。（e.g. UIAlertView）
- テスト配信モード(adTestMode=YES)時、SDK セットアップが完了する前に [MaioInstance canShow:] を呼び出すと例外となる不具合を修正。

## v1.1.2 (2016-05-18)
- Apple/Reachability を IPv6 に対応した v5.0 に更新。
- [Test for IPv6 DNS64/NAT64 Compatibility Regularly]に従って動作確認。
- 動画広告の再生準備中に着信割込み等でアプリが非アクティブになると、動画が再生されず操作できなくなってしまう不具合を修正。
- バックグラウンド時に行っていた動画の一時停止処理を非アクティブ時に行うよう修正。
- 動画広告表示中にアプリがバックグラウンドに遷移した際、広告が閉じられるよう制御するオプション機能を実装。

## v1.1.1 (2016-05-06)
- bitcode を含めるよう対応。

## v1.1.0 (2016-05-06)
- 複数の maio Media ID を設定できるよう、クラス構造をリファクタリングし対応。
- 動画再生準備完了時に、次のクリエイティブをプリロードするよう対応。
- 何らかの事由で動画広告が一時停止された際に、画面に再生ボタンを表示するよう対応。
- その他内部挙動・軽微なバグの微修正。

## v1.0.7 (2016-04-29)
- 動画制御 UI ファイルが破損していた場合に、動画が停止し操作できなくなってしまうので、速やかにエラー通知しアプリに戻るよう修正。
- MD5 ハッシュ値によるクリエイティブ検証処理を追加。
- 動画再生中に Siri により割り込まれた後、動画が停止してしまう不具合を修正。
- SDK のバージョンを返すメソッドを追加。

## v1.0.6 (2016-04-15)
- 動画が破損等により再生途中で停止した場合に、再生エラーとして処理されなかった不具合を修正。
- ダウンロードしたクリエイティブリソースが破損していた場合にリトライするよう修正。
- オフラインとオンラインが頻繁に切り替わると、クリエイティブのダウンロードが一時的に停止してしまう不具合を修正。

## v1.0.5 (2016-02-04)
- 動画再生エラー時に動画広告が閉じない不具合を修正。
- info.plist の CFBundleShortVersionString が無い状態で SDK をセットアップするとクラッシュする不具合を修正。

## v1.0.4 (2015-11-25)
- 一枚画像のエンドカード時にオリエンテーションが固定されるよう修正
- iOS9 以降のデバイスから canOpenUrl が呼ばれた際にエラーログが出力されないよう修正
- メインスレッド外から動画広告を再生するとエラーとなる不具合を修正

## v1.0.3 (2015-10-21)
- 動画再生後に、AudioSession の設定が初期化されてしまう不具合を修正
- 回転検出時、UIDeviceOrientationUnknown を正常に処理できていなかったので対応。
- iOS9 から supportedInterfaceOrientations の返値の型が微妙に変わったので修正。

## v1.0.2 (2015-09-01)
- アクティブなクリエイティブキャッシュまで削除されてしまう不具合を修正
- 動画再生毎にメモリリークしてしまう不具合を修正

## v1.0.1 (2015-08-27)
- window.rootViewController 以外の UIViewController から [Maio show] をコールするとエラーとなり広告が表示されない不具合を修正
- 配信優先度の高いキャンペーンが、キャッシュアウトされても優先的に選ばれてしまい、広告が表示されない不具合を修正
- アプリ起動中に動画キャッシュファイルがシステムによって削除されてしまった場合、暫くの間広告表示が行えなくなる不具合を修正

## v1.0.0 (2015-08-21)
