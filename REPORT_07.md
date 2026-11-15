# 第7回 Webエンジニアリング演習 レポート
## 学籍番号
4724103
## 2画面の見出しと本文
    if (page === "#detail") {
        app.innerHTML = `
            <h1>詳細な見出し</h1>
            <p>詳細じゃない本文</p>
        `;
    }
    if (page === "#compare") {
        app.innerHTML = `
            <h1>比較する見出し</h1>
            <p>比較してない本文</p>

## クリック後のURLとNetworkの確認
比較をクリック後のURL：https://verbose-spork-97g7q76g4j67hxq6q-3000.app.github.dev/csr/#compare
詳細をクリック後のURL：https://verbose-spork-97g7q76g4j67hxq6q-3000.app.github.dev/csr/#detail
Network：http://10.0.2.170:3000

## 画面を切り替える処理の要点
window.addEventListener("hashchange", () => {
    const page = location.hash;
    console.log(page);
    console.log(location.hash);
