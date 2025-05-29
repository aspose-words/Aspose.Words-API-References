---
title: SaveOptions.UpdateLastPrintedProperty
linktitle: UpdateLastPrintedProperty
articleTitle: UpdateLastPrintedProperty
second_title: Aspose.Words for .NET
description: 使用 SaveOptions UpdateLastPrintedProperty 优化文档管理。控制 LastPrinted 的更新，实现高效保存并增强工作流程。
type: docs
weight: 180
url: /zh/net/aspose.words.saving/saveoptions/updatelastprintedproperty/
---
## SaveOptions.UpdateLastPrintedProperty property

获取或设置一个值，确定[`LastPrinted`](../../../aspose.words.properties/builtindocumentproperties/lastprinted/)属性在保存之前更新。

```csharp
public bool UpdateLastPrintedProperty { get; set; }
```

## 例子

显示如何在保存时更新文档的“上次打印”属性。

```csharp
Document doc = new Document();

DateTime lastPrinted = new DateTime(2019, 12, 20);
doc.BuiltInDocumentProperties.LastPrinted = lastPrinted;

// 此标志确定最后打印的日期（内置属性）是否已更新。
// 如果是，则为文档最近一次保存操作的日期
// 将此 SaveOptions 对象作为参数传递，用作打印日期。
DocSaveOptions saveOptions = new DocSaveOptions();
saveOptions.UpdateLastPrintedProperty = isUpdateLastPrintedProperty;

// 在 Microsoft Word 2003 中，可以通过文件 -> 属性 -> 统计信息 -> 已打印找到此属性。
// 它还可以通过使用 PRINTDATE 字段显示在文档正文中。
doc.Save(ArtifactsDir + "DocSaveOptions.UpdateLastPrintedProperty.doc", saveOptions);

// 打开已保存的文档，然后验证属性的值。
doc = new Document(ArtifactsDir + "DocSaveOptions.UpdateLastPrintedProperty.doc");

if (isUpdateLastPrintedProperty)
    Assert.AreNotEqual(lastPrinted, doc.BuiltInDocumentProperties.LastPrinted);
else
    Assert.AreEqual(lastPrinted, doc.BuiltInDocumentProperties.LastPrinted);
```

### 也可以看看

* class [SaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
