# 演習: 会話アクションを作成する

この演習では、"Project ABC" というタイトルの架空の組織プロジェクトに関する情報を提供する会話アクションを作成します。

演習タスク:

- Copilot Studio で会話アクションを作成する
- 会話アクションを Microsoft Copilot に発行する。
- Microsoft Copilot での会話アクション

## タスク 1: (省略可能) 既定のエクスペリエンスをテストする

まず、Microsoft 365 Copilot の Project ABC について質問します。

1. **Microsoft Teams** を開き、職場または学校アカウントでサインインします。

1. サイドバーで **[Chat]** を選択します。

1. チャット メニューで **[Copilot]** を選択します。

1. メッセージ作成ボックスに「`Who should I contact for questions about Project ABC?`」と入力します

1. Microsoft 365 Copilot には現在、Project ABC に関する情報がないことに注意します。

## タスク 2: 新しい会話アクションを作成する

まず、Microsoft Copilot で新しい会話アクションの名前、ソリューション、スキーマを構成します。

1. Web ブラウザーで、[Copilot Studio](https://copilotstudio.microsoft.com) に移動し、メッセージが表示されたら、職場または学校アカウントでサインインします。  ウェルカム メッセージをスキップするには **[skip]** を選択します。

    **注:** 初めて Copilot Studio を開くと、最初のコパイロットを作成するためのチャット インターフェイスが表示されることがあります。 この場合は、**[…]** を選択します。 右上のメニュー (**[作成]** ボタンの横) をクリックし、**[コーパイロット作成のキャンセル]**、**[終了]** を順に選択してチャット インターフェイスを終了し、Copilot Studio のホーム ページを表示します。
1. 左のナビゲーションで、**[Library]** を選択します。 ここでは、既存のアクションとコネクタの一覧を表示し、新しいアクションとコネクタを作成できます。
1. 上部にある **[Add an item]** を選択します。  メニューには、Copilot for Microsoft 365 を拡張するための 2 つのオプションが一覧表示されます。
:::image type="content" source="../Media/extend copilot options.png" alt-text="ウィンドウには、Copilot を拡張するための 2 つのオプションが一覧表示されます。コパイロットを作成するか、アクションを作成します。":::
1. **新しいアクション** を選択します。

1. **[Conversational]** を選択して会話アクションを作成します。

1. **[name]** フィールドに「`Project ABC`」と入力し、既定のソリューションとスキーマをそのまま使用します。

1. **[Create]** を選択して続行します。 新しい会話アクションが作成されます。 これには数秒かかる場合があります。 完了すると、アクションの構成を続行するために、作成キャンバスにドロップされます。

## タスク 3: トピックを構成する

次に、トピックの名前とトリガーを構成します。

1. 会話アクションの作成ウィンドウで、**[Topics]** タブに移動します。

1. ウィンドウの上部にある [**Topic name]** テキスト ボックスを選択します。既定では名前として「`"Untitled"`」、トピックの名前として「`Project ABC info`」と入力します。

1. トピック内の **[Trigger]** ノードで、"トピックの内容を説明する" テキストの下にあるテキスト ボックスを選択し、「`Answers questions and provides information about Project ABC, including questions about objectives, points of contact, and rollout timeline.`」と入力します。

## タスク 4: メッセージの送信

次に、Project ABC に関するメッセージを送信するノードをトピックに追加します。

1. [Trigger] ノードで、**+** アイコンを選択して新しいノードを追加します。

1. 表示されるメニューで、**[Send a message]** を選択します。  メッセージ ノードが作成されました。

1. メッセージ ノードでテキスト ボックスを選択し、「`Project ABC is an initiative aimed at improving the culture and engagement within the company.  Objectives of the project include improved morale, increased employee survey results, and improved culture ratings.  For more information about Project ABC, contact Devon Torres.`」と入力します。

1. 作成キャンバスの上にある **[Save]** を選択して変更を保存します。

## タスク 5: アクションの発行

次に、Microsoft 365 Copilot でアクションを発行します。

1. ページ上部にある**発行**を選択します。

1. **[Publish Plugin]** ページで、**[発行]** を選択します。

1. **[Publish latest content?**] ページで、Project ABC Info プラグインが有効になっていることを確認し、**[Publish]** を選択します。  アプリケーションの公開は、数分かかる場合があります。  発行が完了すると、ウィンドウの上部に通知が表示されます。

## タスク 6: アクションを有効にしてテストする

Microsoft 365 Copilot でアクションをテストします。

1. **Microsoft Teams** を開きます。

1. サイドバーで **[Chat]** を選択します。

1. チャット メニューで **[Copilot]** を選択します。

1. メッセージ作成領域で、**[Copilot 応答の管理]** ボタンを選択します。

1. ポップアップで、**Copilot Studio** を検索し **[追加]** を選択して Copilot Studio を追加します。
 
2. **Project ABC info** アクションがポップアップに一覧表示されます。  **Project ABC info** が有効になっていることを確認し、ポップアップを閉じます。

:::image type="content" source="../Media/projectABCInfo-action-enabled.png" alt-text="[Project ABC Info]\(プロジェクト ABC 情報\) アクションのスクリーンショット"Manage Copilot response" flyout in Teams.":::

3. メッセージ作成ボックスに「`Who should I contact for questions about Project ABC?`」と入力します

4. Microsoft 365 Copilot は、会話アクションを呼び出すことによって Project ABC に関する情報を返すことに注意してください。

追加のノードを使用して、この会話アクションをカスタマイズまたは展開できます。  たとえば、新しい **[生成型の回答]** ノードを作成し、ファイルをアップロードして、アクションで使用可能な知識を拡張できます。

**注:** Copilot でアクションをテストするときは、次の点に注意してください。
- Copilot は常に自分自身の回答であなたの回答を書き換えます。 このプレビューでは、コンテンツを変更せずにエンド ユーザーに渡すことはできません。
- 会話プラグインの説明は、会話プラグインを確実に呼び出すために重要です。 説明は、アクションが何が得意とし、どのような回答を提供できるかをオーケストレーターに伝えます。 説明を記述する際は必ず明確な散文を使用し、最良の結果を得るために変更を試すことを検討してください。
- これらの手順を正確に実行しても、Copilot が毎回予想される結果を返すという保証はありません。  Copilot は、プラグインを呼び出すタイミングと結果を返す方法を決定します。

## (省略可能) 課題:あなた自身を作成する

学習した内容を適用して、選択したシナリオに合わせて新しい会話アクションを作成、公開、テストします。  必要に応じて、この演習の手順を確認します。