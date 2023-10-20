---
title: Document.ShowSpellingErrors
linktitle: ShowSpellingErrors
articleTitle: ShowSpellingErrors
second_title: 用于 .NET 的 Aspose.Words
description: Document ShowSpellingErrors 财产. 指定是否在此文档中显示拼写错误 在 C#.
type: docs
weight: 400
url: /zh/net/aspose.words/document/showspellingerrors/
---
## Document.ShowSpellingErrors property

指定是否在此文档中显示拼写错误。

```csharp
public bool ShowSpellingErrors { get; set; }
```

## 例子

显示如何显示/隐藏文档中的错误。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 插入两个有错误会被拾取的句子
// 通过 Microsoft Word 中的拼写和语法检查器。
builder.Writeln("There is a speling error in this sentence.");
builder.Writeln("Their is a grammatical error in this sentence.");

// 如果启用了这些选项，则拼写错误将带有下划线
// 在输出文档中由一条锯齿状的红线和一条双蓝线将语法错误突出显示。
doc.ShowGrammaticalErrors = showErrors;
doc.ShowSpellingErrors = showErrors;

doc.Save(ArtifactsDir + "Document.SpellingAndGrammarErrors.docx");
```

### 也可以看看

* class [Document](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
