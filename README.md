# WebRTC 実験室

WebRTC 関連の実験(HTML, JavaScript)を公開します。(MIT ライセンス)

GitHub Pages は[こちら](https://nabehiro.github.io/webrtcexpjp/)

## Qiita記事のサンプル

### WebRTCを試すときにオッサンが映り続ける問題に対処する

Qiitaの記事は[こちら](http://qiita.com/massie_g/items/5a6c4b69374d5997dc37)

* ローカルの映像/音声ファイルをメディアストリームに変換 [file_to_stream.html](/tool/file_to_stream.html)

### WebRTCオッサン問題を超えて。ローカルファイルを自在に操りたい

Qiitaの記事は[こちら](https://qiita.com/massie_g/items/0635a212f5860fe59047)

* ローカルの映像/音声ファイルをメディアストリームに変換するとき、2つの映像を切り替えられるようにする [switch_to_stream.html](/tool/switch_to_stream.html)

* ローカルの映像/音声ファイルを2種類切り替えながら表示する(VJ的なもの)。録画も可能 [switch_to_stream_rec.html](/tool/switch_to_stream_rec.html)

### すべてのオッサンをWebRTCで配信される前に360度映像から消し去りたい

Qiitaの記事は[こちら](https://qiita.com/massie_g/)

* カメラの映像に静止画でマスクをかけて、自分の姿を消す。顔検出も試してみた [mask_face.html](tool/mask_face.html)


### ブラウザの BroadcastChannel を使ってシグナリング

Qiitaの記事は[こちら](https://qiita.com/massie_g/items/925c12076af669106b40)

* BroadcastChannelを使ったシグナリングを行う多人数ビデオチャット [basic2016/multi_bc.html](/basic2016/multi_bc.html)



## HTML5Experts.jp WebRTC入門2016 のサンプル
[WebRTC入門2016はこちら](https://html5experts.jp/series/webrtc2016/)

### (1)カメラを使ってみよう 
* 新しいAPIでカメラをつかってみる [basic2016/camera_new.html](/basic2016/camera_new.html)
* 新旧APIをPromiseでラップしてみる [basic2016/camera_old_new.html](/basic2016/camera_old_new.html)
* CSS3と組み合わせてみる [basic2016/camera_css_wrap.html](/basic2016/camera_css_wrap.html)

### (2)手動でシグナリングをやってみよう 
* 基本の手動シグナリング [basic2016/hand_signaling.html](/basic2016/hand_signaling.html)

### 手動シグナリング番外編
* Safari TP32でも動く、ontrack/addTrack対応版 [basic2016/hand_signaling_track.html](/basic2016/hand_signaling_track.html)
* adapter.jsを使ってEdgeでも動く手動シグナリング [basic2016/hand_signaling_adapter.html](/basic2016/hand_signaling_adapter.html)
* 手動シグナリングでSDPを変更してみる [basic2016/hand_signaling_modify.html](/basic2016/hand_signaling_modify.html)

### (3) WebSocketを使ったシグナリングサーバーを使おう
* WebSocketを使ったシグナリング (Vanilla ICE) [basic2016/ws_signaling_1to1_vanilla.html](/basic2016/ws_signaling_1to1_vanilla.html)
* WebSocketを使ったシグナリング (Trickle ICE) [basic2016/ws_signaling_1to1_trickle.html](/basic2016/ws_signaling_1to1_trickle.html)
* node.js用シグナリングサーバー (ws利用) [basic2016/server/signaling.js](/basic2016/server/signaling.js)
* Chrome appの簡易WebSocketサーバー [Simple Message Server](https://chrome.google.com/webstore/detail/simple-message-server/bihajhgkmpfnmbmdnobjcdhagncbkmmp)

### (4) シグナリングを拡張して、多人数でビデオチャットしよう
* socket.ioを使って、多人数ビデオチャット [basic2016/multi.html](/basic2016/multi.html)
* node.jsとsocket.ioを使った、多会議室、多人数対応のシグナリングサーバー [basic2016/server/signaling_room.js](/basic2016/server/signaling_room.js)

### (5) 番外編：Firebaseで楽々シグナリング
* Firebaseを使ってシグナリングを行う多人数ビデオチャット [basic2016/multi_firebase.html](/basic2016/multi_firebase.html)
* Firebaseを使ってシグナリング、adapter.jsでEdge同志の通信も可能 [basic2016/multi_firebase_adapter.html](/basic2016/multi_firebase_adapter.html)

### (6) 番外編：シグナリングサーバー不要 - BroadcastChannelを使ったシグナリング
* BroadcastChannelを使ったシグナリングを行う多人数ビデオチャット [basic2016/multi_bc.html](/basic2016/multi_bc.html)
* BroadcastChannelを使った多人数ビデオチャット</a> (同一マシンのChrome間, Firefox間で動作）

### (7) 番外編：最新のWebRTCのtrack系処理を、手動＋データチャネルシグナリングで観察してみる
* 手動シグナリング+DataChannelシグナリングでtrackを操る [basic2016/datachannel_signaling_track.html](/basic2016/datachannel_signaling_track.html)
* addTrack()/removeTrack()を使い、ontrack(), onremovetrack()に対応</a> 
* Qiitaの記事： [最新のWebRTCのtrack系処理を、手動＋データチャネルシグナリングで観察してみる](https://qiita.com/massie_g/items/1316eb8c6e0d171307f5)

### (8) 番外編： addTrack()/ontrack()、multi-stream時代の DataChannelシグナリング (2018.08)
*  DataChannelのよる1:1シグナリング、multi-stream、addTrack()/ontrack()対応 [basic2016/dc_signaling_multistream.html](/basic2016/dc_signaling_multistream.html)
* BroadcastChannelを使って初期シグナリングでDataChannelを確立、その後はDataChannelを介してシグナリング
* ※BroadcastChannelのチェックを外せば、手動シグナリングも可能（Chrome - Firefox間）
* addTrack()/removeTrack(), peer.ontrack(), stream.onremovetrack()を利用
* Firefoxと, Chrome 70〜で利用できる、Unified Planを用いたmulti-streamに対応


## WebRTC Meetup 10 のサンプル
Chrome 50 で動作確認
* 音声も含んだ多段中継の実験 [self/relay.html](/self/relay.html)
* 映像のディレイの実験 [self/relay_delay.html](/self/relay_delay.html)
* SDPのbandwidth制限を用いた、MediaRecorderのビットレート調整の実験 [self/record_bandwidth.html](/self/record_bandwidth.html)
* SDPのコーデック指定を用いて、MediaRecorderのVP9録画実験 [self/record_relay_vp9](/self/record_relay_vp9.html)
* オプション指定でのMediaRecordeのVP9録画サンプル [self/record_vp9.html](/self/record_vp9.html)

##  Promise版 手動シグナリング
Firefox 46, Chrome 51 で確認
* Promiseを使った、Vanilla ICEの手動シグナリング [hand/vanilla_promise.html](hand/vanilla_promise.html)

## Canvas.captureStream() を使った擬似Simulcast(手動シグナリング)
Firefox Nightly 49同士, Chrome 51同士で確認 (Firefox - Chrome間では動作しない）
* Canvas.captureStream()の擬似Simulcast 送信側 [hand/canvas_pseudo_simulcast.html](hand/canvas_pseudo_simulcast.html)
 * audio x 1, video x 3 (camera x 1, canvas x 2) を最初からマルチストリーム通信
* 擬似Simulcast 受信側 [hand/receive_pseudo_simulcast.html](hand/receive_pseudo_simulcast.html)
* replaceTrack()を使って、videoTrackを切り替えるデモ(送信側)(FireFox 49) [hand/switch_pseudo_simulcast.html](hand/switch_pseudo_simulcast.html)
 * 受信は [hand/receive_pseudo_simulcast.html](hand/receive_pseudo_simulcast.html) を流用
