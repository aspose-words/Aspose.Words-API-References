---
title: HtmlSaveOptions.ReplaceBackslashWithYenSign
linktitle: ReplaceBackslashWithYenSign
articleTitle: ReplaceBackslashWithYenSign
second_title: Aspose.Words for .NET
description: 了解 HtmlSaveOptions ReplaceBackslashWithYenSign 属性如何通过将反斜杠转换为日元符号来增强 HTML 输出效果。默认值为 false。
type: docs
weight: 420
url: /zh/net/aspose.words.saving/htmlsaveoptions/replacebackslashwithyensign/
---
## HtmlSaveOptions.ReplaceBackslashWithYenSign property

指定是否应将反斜杠字符替换为日元符号。 默认值为`错误的`.

```csharp
public bool ReplaceBackslashWithYenSign { get; set; }
```

## 评论

默认情况下，Aspose.Words 会模仿 MS Word 的行为，不会在生成的 HTML 文档中将反斜杠字符替换为日元符号。然而，Aspose.Words 的早期版本在某些特定情况下会执行此类替换。此标志可实现与 Aspose.Words 早期版本的向后兼容性。

## 例子

展示如何用日元符号替换反斜杠字符（Html）。

```csharp
Document doc = new Document(MyDir + "Korean backslash symbol.docx");

// 默认情况下，Aspose.Words 模仿 MS Word 的行为，不会用日元符号替换反斜杠字符
// 生成的 HTML 文档。然而，Aspose.Words 的早期版本在某些
// 场景。此标志可实现与 Aspose.Words 先前版本的向后兼容性。
HtmlSaveOptions saveOptions = new HtmlSaveOptions();
saveOptions.ReplaceBackslashWithYenSign = true;

doc.Save(ArtifactsDir + "HtmlSaveOptions.ReplaceBackslashWithYenSign.html", saveOptions);
```

### 也可以看看

* class [HtmlSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
