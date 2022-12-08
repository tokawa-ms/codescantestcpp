# codescantest
GitHub Code Scanning に引っかかるコードのサンプルです。

# How to use
1. Visual Studio の C++ コンソールアプリプロジェクトを作成
2. GitHub に発行
3. Public Repositry に変換
4. Security - Code Scanning から codeql.yml を作成
5. autobuild は失敗するので、Windows Runner を利用する設定に変更し、Visual Studio でコードをビルドできるようにする（本リポジトリの codeql.yml を参照）
6. とりあえず CodeQL のアクションが通るのを確認
7. メインのコードを、本リポジトリにある cpp ファイルのものに変更して push (#define _CRT_SECURE_NO_WARNINGS の設定忘れずに)
8. Security - Code Scanning に OverRun の警告などが検出されていたら OK
