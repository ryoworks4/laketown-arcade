# LAKETOWN ARCADE

イベント会場デモ集の公開ページ（ https://laketown-game.vercel.app/ ）。
※ 旧 laketown-arcade.vercel.app は別アカウントの旧スタブが占有しているため laketown-game に改名（2026-07-23）。Vercelプロジェクト名は laketown-arcade のまま。
開催日ごとの棚に、AIと作ったゲームを並べる。ゲーム本体は
[natsu-game-land](https://github.com/ryoworks4/natsu-game-land)（GitHub Pages）でホストし、ここからは直リンクする。

## イベント当日にゲームを足す手順

1. ゲームを作って `natsu-game-land` に push（従来どおり。verify.sh PASS を確認）
2. この `index.html` の `DAYS` 配列に1行足す（新しい開催日は配列の**先頭**にブロックを追加し、前回の `isNew: true` を外す）
3. push → Vercel が自動デプロイ（数十秒）→ QRを見せてその場で遊んでもらう

## ルール

- TSUTAYA・店舗名は書かない（会場の個別情報を公開物に出さない）
- ゲームの表示名にIP名（マイクラ等）を使わない（2026-06-25 決定）
- 1ファイル自己完結（外部CDN・fetch禁止はゲームと同じ方針）
