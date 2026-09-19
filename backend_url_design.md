|                    機能                    | メソッド |                          URL 　                           | 認証 |
| :----------------------------------------: | :------: | :-------------------------------------------------------: | :--: |
|                 サインイン                 |   POST   |                   /ap1/v1/auth/sign_in                    |      |
|             サインイン(Github)             |   GET    |                    /api/v1/auth/github                    |      |
|          サインイン(コールバック)          |   GET    |               /api/v1/auth/github/callback                |      |
| コールバック後の処理(コントローラーへ転送) |   無し   |                /api/v1/omniauth_callbacks                 |      |
|                ユーザー登録                |   POST   |                       /api/v1/auth                        |      |
|     登録後の処理(コントローラーへ転送)     |   無し   |                   /api/v1/registrations                   |      |
|                サインアウト                |  DELETE  |                   /api/v1/auth/sign_out                   |      |
| サインアウト後の処理(コントローラーへ転送) |   無し   |                     /api/v1/sessions                      |      |
|                githubと連携                | GET/POST |        /api/v1/users/{id}/setting/github/authorize        |  ◯   |
| リポジトリ取込開始(レビュー取込・問題生成) |   POST   |           /api/v1/users/{id}/setting/repository           |  ◯   |
|                Slackと連携                 |   GET    |        /api/v1/users/{id}/setting/slack/authorize         |  ◯   |
|         Slackと連携(コールバック)          | GET/POST |         /api/v1/users/{id}/setting/slack/redirect         |  ◯   |
|                  Top画面                   |   GET    |                    /api/v1/users/{id}                     |  ◯   |
|              レビュー実績一覧              |   GET    |                /api/v1/users/{id}/reviews                 |  ◯   |
|              レビュー実績詳細              |   GET    |              /api/v1/users/{id}/reviews/{id}              |  ◯   |
|             レビュー実績(編集)             |   PUT    |           /api/v1/users/{id}/reviews/{id}/edit            |  ◯   |
|             レビュー実績(削除)             |  DELETE  |          /api/v1/users/{id}/reviews/{id}/delete           |  ◯   |
|                学習問題一覧                |   GET    |               /api/v1/users/{id}/questions                |  ◯   |
|                学習問題詳細                |   GET    |             /api/v1/users/{id}/questions/{id}             |  ◯   |
|               学習問題(編集)               |   PUT    |          /api/v1/users/{id}/questions/{id}/edit           |  ◯   |
|               学習問題(削除)               |  DELETE  |         /api/v1/users/{id}/questions/{id}/delete          |  ◯   |
|         項目別レコード(実績) - tag         |   GET    |            /api/v1/users/{id}/reviews?tags=◯◯             |  ◯   |
|         項目別レコード(問題) - tag         |   GET    |           /api/v1/users/{id}/questions?tags=◯◯            |  ◯   |
|                プロフィール                |   GET    |                      /api/v1/profile                      |  ◯   |
|             プロフィール(更新)             |   PUT    |                      /api/v1/profile                      |  ◯   |
|           プロフィール(自分以外)           |   GET    |                    /api/v1/users/{id}                     |      |
|                  所属組織                  |   GET    |                 /api/v1/organization/{id}                 |  ◯   |
|                  組織登録                  |   POST   |                   /api/v1/organization                    |  ◯   |
|              問い合わせ(送信)              |   POST   |                      /api/v1/inquiry                      |      |
|                    設定                    |   GET    |                /api/v1/users/{id}/setting                 |  ◯   |
|            設定(リポジトリ削除)            |  DELETE  |     /api/v1/users/{id}/setting/repository/{id}/delete     |  ◯   |
|              設定(プラン変更)              |   POST   |              /api/v1/users/{id}/setting/plan              |  ◯   |
|              設定(退会手続き)              |  DELETE  |           /api/v1/users/{id}/setting/withdrawal           |  ◯   |
|          設定(自動復習) - ON/OFF           |   PUT    |          /api/v1/users/{id}/setting/auto-reviews          |  ◯   |
|       設定(自動復習) - 通知時間設定        |   PUT    | /api/v1/users/{id}/setting/auto-reviews/notification-time |  ◯   |
|      設定(自動復習) - 覆手問題数設定       |   PUT    | /api/v1/users/{id}/setting/auto-reviews/max-daily-reviews |  ◯   |
|       設定(自動復習) - 通知方法設定        |   PUT    |   /api/v1/users/{id}/setting/auto-reviews/hot-to-notify   |  ◯   |
|                    タグ                    |   GET    |                        /api/v1/tag                        |      |
|                 タグ(編集)                 |   PUT    |                   /api/v1/tag/{id}/edit                   |      |
|                 タグ(削除)                 |  DELETE  |                  /api/v1/tag/{id}/delete                  |      |
|                 ランキング                 |   GET    |                      /api/v1/ranking                      |      |
|                    称号                    |   GET    |                    /users/{id}/titles                     |  ◯   |
|            ブックマーク - 一覧             |   GET    |                     /users/bookmarks                      |  ◯   |
|       ブックマーク - 登録(学習問題)        |   POST   |              /users/bookmarks/questions/{id}              |  ◯   |
|      ブックマーク - 登録(脆弱性課題)       |   POST   |       /users/bookmarks/vulnerability_questions/{id}       |  ◯   |
|     ブックマーク - 登録解除(学習問題)      |  DELETE  |              /users/bookmarks/questions/{id}              |  ◯   |
|      ブックマーク - 登録(脆弱性課題)       |  DELETE  |       /users/bookmarks/vulnerability_questions/{id}       |  ◯   |
|               脆弱性課題生成               |   POST   |                 /vulnerability-questions                  |      |
|             脆弱性課題一覧表示             |   GET    |                 /vulnerability-questions                  |      |
|             脆弱性課題詳細表示             |   GET    |               /vulnerability-questions/{id}               |      |
|             管理者 - 課題編集              |   PUT    |         /root/vulnerability-questions/{id}/modify         |  ◯   |
|          管理者 - ステータス変更           |   PUT    |         /root/vulnerability-questions/{id}/status         |  ◯   |
