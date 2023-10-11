---
title: Document.ShowSpellingErrors
second_title: Aspose.Words for .NET API 参考
description: Document 财产. 指定是否显示本文档中的拼写错误
type: docs
weight: 400
url: /zh/net/aspose.words/document/showspellingerrors/
---
## Document.ShowSpellingErrors property

指定是否显示本文档中的拼写错误。

```csharp
public bool ShowSpellingErrors { get; set; }
```

### 例子

演示如何显示/隐藏文档中的错误。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 插入两个有错误的句子，会被拾取
// 通过 Microsoft Word 中的拼写和语法检查器。
builder.Writeln("There is a speling error in this sentence.");
builder.Writeln("Their is a grammatical error in this sentence.");

// 如果启用这些选项，则拼写错误将带有下划线
// 在输出文档中用锯齿状红线和双蓝线突出显示语法错误。
doc.ShowGrammaticalErrors = showErrors;
doc.ShowSpellingErrors = showErrors;

doc.Save(ArtifactsDir + "Document.SpellingAndGrammarErrors.docx");
```

### 也可以看看

* class [Document](../)
* 命名空间 [Aspose.Words](../../document/)
* 部件 [Aspose.Words](../../../)


