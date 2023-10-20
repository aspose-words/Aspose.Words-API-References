---
title: Document.SpellingChecked
linktitle: SpellingChecked
articleTitle: SpellingChecked
second_title: 用于 .NET 的 Aspose.Words
description: Document SpellingChecked 财产. 返回真的如果文档已检查拼写 在 C#.
type: docs
weight: 410
url: /zh/net/aspose.words/document/spellingchecked/
---
## Document.SpellingChecked property

返回**真的**如果文档已检查拼写。

```csharp
public bool SpellingChecked { get; set; }
```

## 评论

要重新检查文档中的拼写，请将此属性设置为**错误的**.

## 例子

显示如何设置拼写或语法验证。

```csharp
Document doc = new Document();

// 有拼写错误的字符串。
doc.FirstSection.Body.FirstParagraph.Runs.Add(new Run(doc, "The speeling in this documentz is all broked."));

 // 如果我们将属性设置为 false，则开始拼写/语法检查。
// 我们可以通过 Review 查看 Microsoft Word 中的所有错误 ->拼写与语法。
// 请注意，Microsoft Word 不会自动启动 DOC 和 RTF 文档格式的语法/拼写检查。
doc.SpellingChecked = checkSpellingGrammar;
doc.GrammarChecked = checkSpellingGrammar;

doc.Save(ArtifactsDir + "Document.SpellingOrGrammar.docx");
```

### 也可以看看

* class [Document](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
