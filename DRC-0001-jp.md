# DragonCapsule ガバナンストークン提案 # 
#### DRC-0001（DragonCapsule Request for Comment）####

- Dip: 0001
- タイトル: DragonCapsule ガバナンストークン提案リクエスト
- 著者: @okayama.shatoshi
- タイプ: リクエストトラック
- カテゴリー: DRC
- ステータス: リクエスト
- 作成日: 2023-04-24

## シンプルな要約
DragonCapsule ガバナンストークンの提案リクエストです。

## 概要
以下の提案では、Tally.xyz（オンチェーンDAO用のOpenZeppelinガバナースタンダードに基づく）をサポートすることを提案します。これは、最大のDAO（Uniswap, AAVE, ENS, Nouns, Gitcoin, Compound）に信頼されています。
この提案では、ガバナンストークンがhttps://eips.ethereum.org/EIPS/eip-20 や https://eips.ethereum.org/EIPS/eip-721 などの関連する標準を実装することが期待されます。また、Tally.xyzは、トークンコントラクトが https://eips.ethereum.org/EIPS/eip-5805 を実装することが求められます。これは、委任と投票パワーチェックポイントのためです。

## 動機
DragonCapsule NFTの保有者が、標準のERC721およびERC20ガバナストークンを介してYieldDAOプロポーザルに投票できるように、標準的なガバナンスフレームプロセスを実装します。

## 仕様
## # ERC721-ERC20 ユニバーサルガバナンストークンモデル
Tallyアプリと互換性を持たせるため、この提案ではOpenZeppelinのライブラリ https://docs.openzeppelin.com/contracts/4.x/api/governance を使用することを推奨しており、ERC721-ERC20ガバナンストークンスワップモデルをサポートする予定です。

####  ガバナンストークンの標準
  `“ERC721: ERC20”`
ガバナンストークン実装参照: https://docs.tally.xyz/user-guides/tally-contract-compatibility/tokens-erc20-and-nfts

#### ERC20トークン名
 `“DragonCapsule ガバナンストークン”`

#### ERC20トークンシンボル
  `“DC”`

#### ERC20トークン総供給量
 `“DC totalSupply：1,000,000,000,000 ”`

#### ERC721-ERC20トークンペア為替レート
  `“ERC721:ERC20 - 1:100,000,000”`

## 実装
すでに、イーサリアムネットワーク上にERC721 / ERC20準拠の関連する自動スワップエンティティがいくつか存在しています。
異なる実装は異なるトレードオフがありますが、サードパーティの標準オープンソースアーキテクチャを選択して、ガバナンストークンスワップLEGOインフラを実装することが最善の選択です。
Tally.xyzは、私たちの最初のガバナンスインフラ候補です。また、SudoSwap（完全オンチェーンNFT AMMプロトコル）は、ERC721-ERC20トークンスワップ実装技術ソリューションを提供し、提案の最初のERC721-ERC20スワップ候補となりました。

### 候補の実装は以下で利用可能です
- https://tally.xyz/
- https://sudoswap.xyz/

## 履歴
この標準に関連する歴史的なリンク:
- 最初の提案: https://github.com/DragonCapsule/DRCs/DRC-0001.md

## 著作権
著作権および関連する権利は[CC0]を介して放棄されました。
