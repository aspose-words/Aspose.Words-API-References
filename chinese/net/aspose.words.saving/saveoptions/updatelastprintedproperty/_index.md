---
title: SaveOptions.UpdateLastPrintedProperty
second_title: Aspose.Words for .NET API 参考
description: SaveOptions 财产. 获取或设置一个值确定是否LastPrinted属性在保存之前更新
type: docs
weight: 180
url: /zh/net/aspose.words.saving/saveoptions/updatelastprintedproperty/
---
## SaveOptions.UpdateLastPrintedProperty property

获取或设置一个值，确定是否[`LastPrinted`](../../../aspose.words.properties/builtindocumentproperties/lastprinted/)属性在保存之前更新。

```csharp
public bool UpdateLastPrintedProperty { get; set; }
```

### 例子

显示如何在保存时更新文档的“CreatedTime”属性。

```csharp
Document doc = new Document();
doc.BuiltInDocumentProperties.CreatedTime = new DateTime(2019, 12, 20);

// 此标志确定是否更新了作为内置属性的创建时间。
// 如果是，则文档最近一次保存操作的日期
// 将此 SaveOptions 对象作为参数传递用作创建时间。
DocSaveOptions saveOptions = new DocSaveOptions();
saveOptions.UpdateCreatedTimeProperty = isUpdateCreatedTimeProperty;

doc.Save(ArtifactsDir + "DocSaveOptions.UpdateCreatedTimeProperty.docx", saveOptions);

// 打开保存的文档，然后验证属性的值。
doc = new Document(ArtifactsDir + "DocSaveOptions.UpdateCreatedTimeProperty.docx");

Assert.AreNotEqual(isUpdateCreatedTimeProperty, new DateTime(2019, 12, 20) == doc.BuiltInDocumentProperties.CreatedTime);
```

显示如何在保存时更新文档的“上次打印”属性。

```csharp
Document doc = new Document();
doc.BuiltInDocumentProperties.LastPrinted = new DateTime(2019, 12, 20);

// 此标志确定是否更新上次打印的日期，这是一个内置属性。
// 如果是，则文档最近一次保存操作的日期
// 将此 SaveOptions 对象作为参数传递用作打印日期。
DocSaveOptions saveOptions = new DocSaveOptions();
saveOptions.UpdateLastPrintedProperty = isUpdateLastPrintedProperty;

// 在 Microsoft Word 2003 中，可以通过 File ->找到该属性属性->统计 ->打印。
// 它也可以通过使用 PRINTDATE 字段显示在文档的正文中。
doc.Save(ArtifactsDir + "DocSaveOptions.UpdateLastPrintedProperty.doc", saveOptions);

// 打开保存的文档，然后验证属性的值。
doc = new Document(ArtifactsDir + "DocSaveOptions.UpdateLastPrintedProperty.doc");

Assert.AreNotEqual(isUpdateLastPrintedProperty, new DateTime(2019, 12, 20) == doc.BuiltInDocumentProperties.LastPrinted);
```

### 也可以看看

* class [SaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../saveoptions/)
* 部件 [Aspose.Words](../../../)


