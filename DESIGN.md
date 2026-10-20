---
version: alpha
name: LOOP THREAD
description: 循環型ファッションのブランドサイト。深いグリーンとライムを軸にしたエディトリアル調のレイアウト。
colors:
  primary: "#163D35"
  primary-hover: "#1D5247"
  primary-pressed: "#112E28"
  secondary: "#D5ED75"
  secondary-hover: "#CDEA5C"
  secondary-pressed: "#C6E743"
  surface: "#FFFFFF"
typography:
  hero:
    fontFamily: Noto Sans JP
    fontSize: 76px
    fontWeight: 500
    lineHeight: 1.3
  brand-large:
    fontFamily: Space Grotesk
    fontSize: 119px
    fontWeight: 500
    lineHeight: 1.05
  logo:
    fontFamily: Space Grotesk
    fontSize: 39px
    fontWeight: 700
    lineHeight: 1.35
  h1:
    fontFamily: Noto Sans JP
    fontSize: 39px
    fontWeight: 500
    lineHeight: 1.45
  h2:
    fontFamily: Noto Sans JP
    fontSize: 31px
    fontWeight: 500
    lineHeight: 1.35
  h3:
    fontFamily: Noto Sans JP
    fontSize: 25px
    fontWeight: 500
    lineHeight: 1.35
  product:
    fontFamily: Noto Sans JP
    fontSize: 20px
    fontWeight: 500
    lineHeight: 1.35
  body-md:
    fontFamily: Noto Sans JP
    fontSize: 16px
    fontWeight: 400
    lineHeight: 1.6
  label-action:
    fontFamily: Noto Sans JP
    fontSize: 16px
    fontWeight: 500
    lineHeight: 1.35
  caption:
    fontFamily: Noto Sans JP
    fontSize: 13px
    fontWeight: 400
    lineHeight: 1.35
  overline:
    fontFamily: Space Grotesk
    fontSize: 13px
    fontWeight: 400
    lineHeight: 1.35
rounded:
  full: 9999px
spacing:
  xs: 4px
  sm: 8px
  md: 16px
  lg: 32px
  xl: 64px
components:
  button-primary:
    backgroundColor: "{colors.secondary}"
    textColor: "{colors.primary}"
    typography: "{typography.label-action}"
    rounded: "{rounded.full}"
    padding: 16px
  button-primary-hover:
    backgroundColor: "{colors.secondary-hover}"
  button-primary-pressed:
    backgroundColor: "{colors.secondary-pressed}"
  button-dark:
    backgroundColor: "{colors.primary}"
    textColor: "{colors.surface}"
    typography: "{typography.label-action}"
    rounded: "{rounded.full}"
    padding: 16px
  button-dark-hover:
    backgroundColor: "{colors.primary-hover}"
  button-dark-pressed:
    backgroundColor: "{colors.primary-pressed}"
  caption:
    textColor: "{colors.primary}"
    typography: "{typography.caption}"
---

## Overview

LOOP THREAD は、古着の回収と再生をテーマにした循環型ファッションブランドのサイトである。ページ全体はエディトリアル誌面のように、左に見出し・右に本文や商品を置く2カラムの構成で、余白を広く取って落ち着いた印象を作る。深いグリーンの文字と白い背景を基調に、ライムのアクセントでアクションを際立たせる。

## Colors

- **Primary (#163D35):** 本文・見出し・罫線・ダークボタンの背景に使う深いグリーン。
- **Primary hover / pressed (#1D5247 / #112E28):** ダークボタンのホバーと押下状態。
- **Secondary (#D5ED75):** 主要アクションのボタン背景に使うライム。文字色は Primary を重ねる。
- **Secondary hover / pressed (#CDEA5C / #C6E743):** ライムボタンのホバーと押下状態。
- **Surface (#FFFFFF):** ページ背景と、ダークボタン上の文字色。

## Typography

和文は Noto Sans JP、ブランド名・ロゴ・英字ラベルは Space Grotesk を使う。見出しは Medium(500)、本文は Regular(400)、ロゴのみ Bold(700)。サイズは約1.25倍のスケール（13 / 16 / 20 / 25 / 31 / 39 / 76 / 119px）で、ヒーロー見出しとブランド名のみ大きく跳ねる。

## Layout

幅1440pxのデスクトップを基準に、左右64pxの余白で組む。セクションは1pxの罫線で区切り、見出し側352px・コンテンツ側896pxの2カラムを基本にする。カードは3列で並べ、列間は約24pxとする。

## Elevation & Depth

影や重なりは使わない。階層は罫線、余白、文字サイズの差だけで表現する。

## Shapes

ボタンは完全な丸み（pill）。写真は大きな矩形で、コンセプト画像であることを示す注記を添える。

## Components

- **Primary action:** ライム背景に Primary の文字。ホバーで Secondary hover に変える。
- **Dark action:** Primary 背景に白文字。
- **Text link:** Label/Action の文字に矢印（Space Grotesk）を添える。
- **Section label:** 連番（01, 02…）と英字ラベルを `Overline` スタイルで並べ、`uppercase` クラスで大文字表示する。

## Do's and Don'ts

- Do 色は `@theme` のトークン（`brand-accent` など）で指定する。
- Do 見出しと本文の文字サイズは定義済みのスケールから選ぶ。
- Don't 影やグラデーションで階層を作らない。
- Don't ライム背景の上に白文字を置かない（コントラスト不足）。
