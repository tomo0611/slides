---
marp: true
paginate: true
math: mathjax
theme: tomo0611
footer: 2025/10/05 (Sun) |  山口 未来変革デジタル人材発掘・育成プログラム
header: "メンター LT会 大井 智弘 (@tomo0611_dev)"
title: メンター LT会 大井 智弘 (@tomo0611_dev) | 山口 未来変革デジタル人材発掘・育成プログラム
description: 2025/10/05 (Sun) |  山口 未来変革デジタル人材発掘・育成プログラム
author: 大井 智弘 / tomo0611.dev
---

# スコープを決めることの重要性

<style scoped>
  .profile-icon {
    width: 90px;
    float: left;
    margin-right: 16px;
    margin-top: 12px;
  }
</style>

<img src="https://omusp.jp/wp-content/uploads/2024/10/profile-ot.png" class="profile-icon" width="90px" height="90px" />

<img class="qrcode" src="https://api.qrserver.com/v1/create-qr-code/?size=150x150&color=5685ad&bgcolor=fff&qzone=4&data=https://slides.tomo0611.dev/20251005-yamaguchi-lighting-talk/">

### 大井 智弘（大阪公立大学 工学部・情報工学科 4 年）

<br />

2025 年 10 月 05 日 (日) | 山口 未来変革デジタル人材発掘・育成プログラム

---

# 自己紹介

![bg 90% right:40%](https://omusp.jp/wp-content/uploads/2024/10/profile-ot.png)

## 大井 智弘 / tomo0611.dev

- 大阪公立大学 工学部 情報工学科 4 年
- 22 y.o.
- [コンピューターハウスランダム](https://ch-random.net/) 前部長
- 大学の情シス(情報基盤課)でシステム開発
- SecHack365 2024 年度 優秀修了生
- 関西テック 2024 年度の修了生

---

# Product vision と project scope

Karl Wiegers と Joy Beatty による Software Requirements, 3rd Edition では以下のように書かれています。

> Two core elements of the business requirements are the vision and the scope. The product vision succinctly describes the ultimate product that will achieve the business objectives. The project scope identifies what portion of the ultimate product vision the current project will address. _(ビジネス要件の 2 つの核心要素は、ビジョンとスコープである。プロダクトビジョンは、ビジネス目標を達成する最終的なプロダクトを簡潔に記述するものである。プロジェクトスコープは、現在のプロジェクトが最終的なプロダクトビジョンのどの部分に対処するかを特定するものである)_

---

# Scope and limitations (スコープと制約)

> Many projects suffer from scope creep—rampant growth as more and more functionality gets stuffed into the product. The first step to controlling scope creep is to define the project’s scope.

> _多くのプロジェクトはスコープクリープに悩まされている。スコープクリープとは、ますます多くの機能が製品に詰め込まれることによる無秩序な成長である。スコープクリープを制御するための第一歩は、プロジェクトのスコープを定義することである_

---

# 組み合わせると難しくなる要件

1 つ 1 つの要件はシンプルでも、組み合わせると難しくなることがあります。
例えば、

- 曜日ごとに異なる部屋の開放時間を設定できる

→ これは簡単です。一方、

- 部屋の開放時間は曜日ごとに加えて、月、週、日ごとに設定できる。変更も一括でできる。
- 祝日や休暇期間などの日は別のルールを適用できる。

→ これは大変複雑です。変更が一括でできるという時点で、その開放時間がどのルールに従っているのかを追跡する必要があり、実装が非常に難しくなります。

---

# 大学で行ったプロジェクト (大学アプリ)

自分が関わったプロジェクトです。

時間割や掲示板の通知など様々な機能があり、App Store では教育カテゴリで 2 位を獲得しました。

![bg right:40% w:400](/20251005-yamaguchi-lighting-talk/images/screenshot_01.png)

---

# 大学で行ったプロジェクト (大学アプリ)

大学アプリプロジェクトでは、しっかりとしたイメージができておらず、スコープが曖昧なまま開発を始めてしまいました。
結果として、以下のような問題が発生しました。

- 途中で要件が大きく変わった
- 仕様が不明確なまま開発を進めてしまった
- 途中でやることが変わり、開発が進まなくなった

→ 結果として工数が大幅に増加し、少人数で大量の勤務をすることになった。

---

# 趣味でやってるプロジェクト (ネイティブアプリ)

Discord でもちょこちょこ開発状況を出していますが、
Kotlin (+ Jetpack Compose) でネイティブアプリを開発しています。

![w:380](/20251005-yamaguchi-lighting-talk/images/screenshot_02.png)

<sup>© 日向夏・イマジカインフォス／「薬屋のひとりごと」製作委員会</sup>

---

# 趣味でやってるプロジェクト (ネイティブアプリ)

前からやってるプロジェクトですが、今回の更新に合わせてスコープを見直しました

[Before]

- 最新の公開されたアニメ情報を表示する画面があった
- ジャンルごとのランキング画面があった

→ アプリの存在意義(=アプリでしかできないこと)がぼやけてしまい、開発が長引いてしまった。機能が少ないので、アニメを探しにくかった。

---

# 趣味でやってるプロジェクト (ネイティブアプリ)

[After]

- ランキングや検索はすべて Web に任せることにした
- 最新の公開されたアニメ情報を表示する画面は廃止した
- ブラウザでアニメを選ぶとアプリに遷移する仕組みにした
- アニメの詳細情報と再生機能に集中することにした

→ 結果、詳細画面と再生画面にこだわることができ、1 日 (10 時間程度)で開発できた。

---

# おわりに

今回は、スコープを明確にすることの重要性についてお話ししました。
ウォーターフォール開発モデルでないからこそ、スコープを明確にすることはプロジェクトの成功に不可欠です。

現段階では、作るもののイメージを深めている方が多いと思いますが、ぜひビジョンやスコープも明確にしてみてください。
特に複数人で開発する場合は、全員の意識が一致していることが重要です。<br /><br />

毎日、Discord の方は眺めているので、質問等あればぜひぜひどうぞ〜🙌

<img class="qrcode" src="https://api.qrserver.com/v1/create-qr-code/?size=150x150&color=5685ad&bgcolor=fff&qzone=4&data=https://slides.tomo0611.dev/20251005-yamaguchi-lighting-talk/">
