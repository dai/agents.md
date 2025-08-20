# AGENTS.md

<p align="center">
  <img src="https://agents.md/og.png">
</p>

[AGENTS.md](https://agents.md)は、コーディングエージェントをガイドするためのシンプルでオープンなフォーマットです。

AGENTS.mdをエージェントのためのREADMEと考えてください：AIコーディングエージェントがあなたのプロジェクトで作業するのを助けるため、コンテキストと指示を提供する専用の、予測可能な場所です。

以下はAGENTS.mdファイルの最小限の例です：

```markdown
# サンプル AGENTS.md ファイル

## 開発環境のヒント
- `ls`でスキャンする代わりに、`pnpm dlx turbo run where <project_name>`を使用してパッケージにジャンプしてください。
- `pnpm install --filter <project_name>`を実行して、パッケージをワークスペースに追加し、Vite、ESLint、TypeScriptが認識できるようにしてください。
- `pnpm create vite@latest <project_name> -- --template react-ts`を使用して、TypeScriptチェック付きの新しいReact + Viteパッケージを立ち上げてください。
- 正しい名前を確認するために、各パッケージのpackage.json内のnameフィールドを確認してください—トップレベルのものはスキップしてください。

## テスト手順
- .github/workflowsフォルダ内のCIプランを確認してください。
- `pnpm turbo run test --filter <project_name>`を実行して、そのパッケージに定義されたすべてのチェックを実行してください。
- パッケージルートからは`pnpm test`を呼び出すだけです。マージする前にコミットはすべてのテストに合格する必要があります。
- 1つのステップに集中するには、Vitestパターンを追加してください：`pnpm vitest run -t "<test name>"`。
- スイート全体が緑になるまで、テストまたは型エラーを修正してください。
- ファイルを移動したり、インポートを変更した後は、`pnpm lint --filter <project_name>`を実行して、ESLintとTypeScriptルールがまだ通ることを確認してください。
- 誰も頼まなくても、変更したコードのテストを追加または更新してください。

## PR手順
- タイトル形式：[<project_name>] <Title>
- コミットする前に常に`pnpm lint`と`pnpm test`を実行してください。
```

## ウェブサイト

このリポジトリには、プロジェクトの目標をシンプルに説明し、いくつかの例を紹介する https://agents.md/ でホストされている基本的なNext.jsウェブサイトも含まれています。

### アプリをローカルで実行する
1. 依存関係をインストール：
   ```bash
   npm install
   ```
2. 開発サーバーを起動：
   ```bash
   npm run dev
   ```
3. ブラウザを開いて http://localhost:3000 にアクセス