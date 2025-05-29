---
title: Document.ShowGrammaticalErrors
linktitle: ShowGrammaticalErrors
articleTitle: ShowGrammaticalErrors
second_title: Aspose.Words for .NET
description: 使用 ShowGrammaticalErrors 属性控制文档中语法错误的可见性。轻松提升写作清晰度和专业性。
type: docs
weight: 410
url: /zh/net/aspose.words/document/showgrammaticalerrors/
---
## Document.ShowGrammaticalErrors property

指定是否显示此文档中的语法错误。

```csharp
public bool ShowGrammaticalErrors { get; set; }
```

## 例子

显示如何显示/隐藏文档中的错误。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 插入两个有错误的句子
// 通过 Microsoft Word 中的拼写和语法检查器。
builder.Writeln("There is a speling error in this sentence.");
builder.Writeln("Their is a grammatical error in this sentence.");

// 如果启用这些选项，则拼写错误将被加下划线
// 在输出文档中用锯齿状的红线表示，双蓝线将突出显示语法错误。
doc.ShowGrammaticalErrors = showErrors;
doc.ShowSpellingErrors = showErrors;

doc.Save(ArtifactsDir + "Document.SpellingAndGrammarErrors.docx");
```

### 也可以看看

* class [Document](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
