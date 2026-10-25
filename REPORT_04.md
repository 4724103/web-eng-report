# 第4回 Webエンジニアリング演習 レポート
## 学籍番号
4724103

## `const`と`let`の宣言・再代入に使用したコード
const courseName = "Web Engineering";
let retryCount = 1;

courseName = "Other Course";
retryCount = 2;
console.log(retryCount);

## VSCodeと`pnpm run check`に表示されたエラー番号・メッセージ
定数であるため、'courseName' に代入することはできません。ts(2588)

src/index.ts:4:1 - error TS2588: Cannot assign to 'courseName' becouse it is constant.

## 修正後の実行結果と`const`・`let`の違いの説明
const courseName = "Web Engineering";
let retryCount = 1;

retryCount = 2;
console.log(retryCount);

結果
tsx src/index.ts
2

constは定数になるので再代入できないが、letは変数なので代入できる。