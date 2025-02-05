---
title: ロールと権限
---

Cloudcraft チームのメンバーには、3 種類の異なるユーザーロールのいずれかが割り当てられます。

- アカウントオーナー
- 管理者
- ユーザー

## ユーザーロールとデフォルトの権限

**注**: ブループリントへの読み取り専用アクセスを許可するには、共有可能なブループリントリンクを作成し、内部 wiki ページにブループリントを埋め込むことができます。

### アカウントオーナー

アカウントオーナーは、Cloudcraft アカウントのすべての要素にアクセスでき、サブスクリプション設定の変更や、請求情報の表示および変更ができる唯一のロールになります。

デフォルトでは、Cloudcraft の有料サブスクリプションにサインアップした人がアカウントオーナーになります。チームの他のメンバーにロールを割り当てるには、[サポートにご連絡ください][1]。

**権限:**

- プライベートおよびチーム共有のブループリントの作成、編集、削除
- サブスクリプション設定の管理
- SSO 設定の管理 (Enterprise)
- チーム設定の管理
  - 新規チームの作成 (Enterprise)
  - 新規管理者とユーザーの招待
  - 管理者とユーザーの削除
  - Cloudcraft チームへの招待の取り消し
- AWS アカウントの管理
  - 新しい AWS アカウントの接続
  - AWS アカウントの削除
  - チーム共有 AWS アカウントの管理
- API キーの管理
  - API キーの作成
  - API キーの削除
  - チーム共有 API キーの管理

### 管理者

管理者は Cloudcraft で 2 番目に特権的なロールで、請求とサブスクリプション情報以外のすべてにアクセスできます。

このロールは、Cloudcraft 内でチームやサブチームの管理権限を必要とするプロジェクトリーダー向けです。

**権限:**

- プライベートおよびチーム共有のブループリントの作成、編集、削除
- チーム設定の管理 (担当チームのみ)
  - 新規管理者とユーザーの招待
  - 管理者とユーザーの削除
  - Cloudcraft チームへの招待の取り消し
- AWS アカウントの管理
  - 新しい AWS アカウントの接続
  - AWS アカウントの削除
  - チーム共有の AWS アカウントの管理
- API キーの管理
  - API キーの作成
  - API キーの削除
  - チーム共有の API キーの管理

### ユーザー

ユーザーは Cloudcraft で最も権限の少ないロールタイプです。ユーザーはチームのメンバーであり、ブループリントを共有したり、AWS アカウントで共同作業したり、一般的な共同作業を行うことができます。

**権限:**

- プライベートおよびチーム共有のブループリントの作成、編集、削除
- 所属するチームへの閲覧専用アクセス
- アカウントオーナーまたは管理者がチームと共有した AWS アカウントのライブスキャン
- API キーの存在に対する閲覧専用アクセス (アクティブな API キーの生成や閲覧は不可)

## 組織横断型チーム

Cloudcraft では、Enterprise をご利用のお客様に、組織横断型チームを作成する機能も提供しています。組織横断型チームのメンバーは、非組織横断型チームのメンバーリストに追加され、すでに別のチームのメンバーでない限り、組織横断型チームのロールを継承します。

このことを理解しやすいように、以下にその一例を示します。

- 会社 A
  - 組織横断型チーム 1
    - ユーザー 1
  - チーム 2
    - ユーザー 2
    - [組織横断型チーム 1 のユーザー 1]
  - チーム 3
    - ユーザー 3
    - ユーザー 1
    - [組織横断型チーム 1 のユーザー 1、ただし、チームにおけるロールは明示的なメンバーシップによって決まる]。

この例では、「チーム 1」が読み取り専用メンバーを持つ監査チームである場合、「ユーザー 1」は暗黙的に「チーム 2」への読み取り専用アクセス権を持つが、「チーム 3」のユーザーに明示的に割り当てられたロールが優先される。

[1]: https://app.cloudcraft.co/support
[2]: https://app.cloudcraft.co/app/support