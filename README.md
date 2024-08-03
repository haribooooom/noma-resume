# のまの職務経歴書

- これはのまの職務経歴書です。
- [職務経歴書ファイル](https://github.com/haribooooom/noma-resume/tree/master/docs#readme)をご覧ください。
- [Figmaで作成したポートフォリオ](https://www.figma.com/proto/wIMQNDaQqofZsygtwIC4pI/%E3%83%AC%E3%82%B8%E3%83%A5%E3%83%A1?page-id=3126%3A4902&node-id=3384-2783&viewport=242%2C1380%2C0.07&t=K4bjmys7MN2d8oxZ-9&scaling=min-zoom&content-scaling=fixed&starting-point-node-id=3384%3A2783&show-proto-sidebar=1)も用意していますので、よろしければご覧ください。

## Data

- [GitHub Pages](https://github.com/haribooooom/noma-resume)  
- [PDF](https://github.com/haribooooom/noma-resume/releases)  
- [File](https://github.com/haribooooom/noma-resume/tree/master/docs#readme)  

## Features

### 💅 Lint text

[textlint](https://github.com/textlint/textlint) での自動校正しています。

```
$ yarn lint --fix
```

[husky](https://github.com/typicode/husky) によってcommit前にも自動で実行されます。  
校正のルールは`.textlintrc`に記載しています。

### 📝 Convert Markdown to PDF

[md-to-pdf](https://www.npmjs.com/package/md-to-pdf) でのPDF生成が可能です。

```
$ yarn build:pdf
```

出力されるPDFはCSSで任意のスタイルを設定可能です。`pdf-configs/style.css`を編集してください。  

### 🛠 Create release

`v**` tagをつけてpushするとGitHub Actionsでビルドが走り、PDFの生成、Releaseの作成、AssetsへPDFの登録が実行されます。

```
$ git commit -m "add job"
$ git tag v1.0
$ git push origin --tags
```

### 📆 Remind update

GitHub Actionsのschedule triggerで3ヶ月に1回、職務経歴書の内容更新を促すissueが自動生成されます。

期間の変更、Jobの停止は[.github/workflows/create-issue.yml](https://github.com/kawamataryo/resume/blob/master/.github/workflows/create-issue.yml) を編集してください。
