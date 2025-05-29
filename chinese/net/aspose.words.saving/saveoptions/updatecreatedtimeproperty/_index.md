---
title: SaveOptions.UpdateCreatedTimeProperty
linktitle: UpdateCreatedTimeProperty
articleTitle: UpdateCreatedTimeProperty
second_title: Aspose.Words for .NET
description: 使用 UpdateCreatedTime 属性优化您的 SaveOptions。在保存前控制 CreatedTime 的更新，以提高数据准确性。默认值为 false。
type: docs
weight: 160
url: /zh/net/aspose.words.saving/saveoptions/updatecreatedtimeproperty/
---
## SaveOptions.UpdateCreatedTimeProperty property

获取或设置一个值，确定[`CreatedTime`](../../../aspose.words.properties/builtindocumentproperties/createdtime/)属性在保存之前更新。 默认值是`错误的`;

```csharp
public bool UpdateCreatedTimeProperty { get; set; }
```

## 例子

展示如何在保存时更新文档的“CreatedTime”属性。

```csharp
Document doc = new Document();

DateTime createdTime = new DateTime(2019, 12, 20);
doc.BuiltInDocumentProperties.CreatedTime = createdTime;

// 此标志决定是否更新创建时间（内置属性）。
// 如果是，则为文档最近一次保存操作的日期
// 将此 SaveOptions 对象作为参数传递，用作创建时间。
DocSaveOptions saveOptions = new DocSaveOptions();
saveOptions.UpdateCreatedTimeProperty = isUpdateCreatedTimeProperty;

doc.Save(ArtifactsDir + "DocSaveOptions.UpdateCreatedTimeProperty.docx", saveOptions);

// 打开已保存的文档，然后验证属性的值。
doc = new Document(ArtifactsDir + "DocSaveOptions.UpdateCreatedTimeProperty.docx");

if (isUpdateCreatedTimeProperty)
    Assert.AreNotEqual(createdTime, doc.BuiltInDocumentProperties.CreatedTime);
else
    Assert.AreEqual(createdTime, doc.BuiltInDocumentProperties.CreatedTime);
```

### 也可以看看

* class [SaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
