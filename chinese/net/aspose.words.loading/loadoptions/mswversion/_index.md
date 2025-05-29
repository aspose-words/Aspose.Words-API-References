---
title: LoadOptions.MswVersion
linktitle: MswVersion
articleTitle: MswVersion
second_title: Aspose.Words for .NET
description: 使用 LoadOptions MswVersion 优化文档加载。确保与特定版本的 MS Word 兼容，默认与 Word 2019 兼容，实现无缝集成。
type: docs
weight: 100
url: /zh/net/aspose.words.loading/loadoptions/mswversion/
---
## LoadOptions.MswVersion property

允许指定文档加载过程应与特定的 MS Word 版本匹配。 默认值为Word2019

```csharp
public MsWordVersion MswVersion { get; set; }
```

## 评论

在加载过程中，不同版本的 Word 对文档内容和格式的某些方面可能略有不同 ，这可能会导致文档对象模型出现细微差别。

## 例子

展示如何在文档加载期间模拟特定 Microsoft Word 版本的加载过程。

```csharp
// 默认情况下，Aspose.Words 根据 Microsoft Word 2019 规范加载文档。
LoadOptions loadOptions = new LoadOptions();

Assert.AreEqual(MsWordVersion.Word2019, loadOptions.MswVersion);

// 此文档缺少默认的段落格式样式。
// 当我们使用 Microsoft Word 或 Aspose.Words 加载文档时，将重新生成此默认样式。
loadOptions.MswVersion = MsWordVersion.Word2007;
Document doc = new Document(MyDir + "Document.docx", loadOptions);

// 当通过 Microsoft Word 2007 规范加载时，样式的行距将具有此值。
Assert.AreEqual(12.95d, doc.Styles.DefaultParagraphFormat.LineSpacing, 0.01d);
```

### 也可以看看

* enum [MsWordVersion](../../../aspose.words.settings/mswordversion/)
* class [LoadOptions](../)
* 命名空间 [Aspose.Words.Loading](../../../aspose.words.loading/)
* 部件 [Aspose.Words](../../../)
