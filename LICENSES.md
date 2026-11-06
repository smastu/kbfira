# 権利表記と再配布条件の確認

Kit-Build System v2 / kbfira: **作者 aryoxp**。参照元は [aryoxp/kbfira](https://github.com/aryoxp/kbfira)。ソースに LICENSE の表示はないが、**2026-11-06 までに松本が作者から利用の許可を得て、ソースの提供を受けた**。これにより、kbui、kitbuild、analyzer、logger、general-ui、Core、各アプリ・ビューを含む本体を GitHub Pages の配信物に入れて公開する。**本体を MIT 等とみなしてはいない**。許可の範囲（公開配信、改変、研究・授業での利用）の記録は、許可のやりとりを残した松本の手元にある。

取り込んだファイルの出典、SHA-256、未取得ファイルは `web/upstream-manifest.json`、生成時の変更は `web/native-patches.json` に保存する。原本は書き換えない。配信対象に使う vendor は次のとおり。版がヘッダーにないものも、同梱バイト列の SHA-256 で固定する。

| 部品 | 同梱版／同定 | 確認したライセンス・表記 |
|---|---|---|
| jQuery | 3.6.0 | MIT、jQuery Foundation / contributors |
| Bootstrap（Popper を含む bundle） | 5.0.2 | MIT、Bootstrap Authors / Popper Authors、ソースの表示を保持 |
| Bootstrap Icons | 原本の font/CSS、版表記なし | MIT、Bootstrap Authors。参照したライセンス本文の版と元バイト列の同定は別に記録 |
| Cytoscape.js | 原本同梱バイト列 | MIT、2016–2021 The Cytoscape Consortium。配布 JS 冒頭の全文を保持 |
| fCoSE / cose-base / layout-base | 原本同梱バイト列 | iVis-at-Bilkent / iVis@Bilkent、MIT。layout-base 内の Apache 2.0 部分と著作権表示も保持 |
| Huebee | 2.1.0 | MIT、2020 Metafizzy |
| anime.js | 3.2.1 | MIT、2020 Julian Garnier |
| animate.css | 4.1.1 | MIT、Animate.css contributors、元 CSS の表示を保持 |
| pako | 2.0.4 | MIT AND Zlib。元 JS の表示を保持 |
| Sortable | 1.10.2 | MIT。jQuery binding の同梱ファイルは独立した許諾表示を確認できず、本体と同様に再配布条件の確認対象 |
| Showdown | 1.9.1 | BSD-3-Clause |
| highlight.js | 11.3.1 | BSD-3-Clause、2006–2021 Ivan Sagalaev and contributors |
| SimpleMDE（CodeMirror 等を含む） | 1.11.2 | MIT、Next Step Webs, Inc.。元 JS の各表示を保持 |
| SheetJS Community Edition | 0.19.1 | Apache-2.0、SheetJS。元 JS の表示を保持 |
| DOMPurify（追加） | 3.4.17、package-lock 固定 | Apache-2.0 OR MPL-2.0。パッケージの LICENSE 全文を同梱 |
| Font Awesome（追加・SimpleMDE 用） | 4.7.0、package-lock 固定 | CSS: MIT / font: SIL OFL-1.1。npm パッケージの表記と README を同梱 |

`licenses/third-party/` に取得できた公式ライセンス本文と取得元 URL・ハッシュを保存する。原本の中に含まれる第三者のライセンス／著作権ヘッダーは削除しない。kbui.js に含まれる Google の clipboard polyfill の Apache 2.0 表示も保持する。ライセンス本文をまだ取得できていない場合は `sources.json` の `error` に残し、取得済みとは扱わない。

ブラウザ検査専用の Playwright / axe-core 等は npm の開発依存で、静的配信物へは含めない。各パッケージの LICENSE は node_modules 内にある。通常ビルドと実行時に外部 CDN のライブラリは取得しない。Google Identity Services のログインスクリプトは Google が配信するものを読み込む。

以上はソースと公式の表示を確認した記録であり、本体の未確認の再配布許諾を補うものではない。
