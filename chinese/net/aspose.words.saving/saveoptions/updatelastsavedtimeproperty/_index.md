---
title: SaveOptions.UpdateLastSavedTimeProperty
linktitle: UpdateLastSavedTimeProperty
articleTitle: UpdateLastSavedTimeProperty
second_title: Aspose.Words for .NET
description: 使用 UpdateLastSavedTime 属性优化您的 SaveOptions。控制 LastSavedTime 的更新，以实现高效的数据管理并增强性能。
type: docs
weight: 190
url: /zh/net/aspose.words.saving/saveoptions/updatelastsavedtimeproperty/
---
## SaveOptions.UpdateLastSavedTimeProperty property

获取或设置一个值，确定[`LastSavedTime`](../../../aspose.words.properties/builtindocumentproperties/lastsavedtime/)属性在保存之前更新。

```csharp
public bool UpdateLastSavedTimeProperty { get; set; }
```

## 例子

展示如何确定保存时是否保留文档的“上次保存时间”属性。

```csharp
Document doc = new Document(MyDir + "Document.docx");

Assert.AreEqual(new DateTime(2021, 5, 11, 6, 32, 0), 
    doc.BuiltInDocumentProperties.LastSavedTime);

// 当我们将文档保存为 OOXML 格式时，我们可以创建一个 OoxmlSaveOptions 对象
// 然后将其传递给文档的保存方法来修改我们保存文档的方式。
// 将“UpdateLastSavedTimeProperty”属性设置为“true”
// 将输出文档的“上次保存时间”内置属性设置为当前日期/时间。
// 将“UpdateLastSavedTimeProperty”属性设置为“false”
// 保留输入文档的“上次保存时间”内置属性的原始值。
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
saveOptions.UpdateLastSavedTimeProperty = updateLastSavedTimeProperty;

doc.Save(ArtifactsDir + "OoxmlSaveOptions.LastSavedTime.docx", saveOptions);

doc = new Document(ArtifactsDir + "OoxmlSaveOptions.LastSavedTime.docx");
DateTime lastSavedTimeNew = doc.BuiltInDocumentProperties.LastSavedTime;

if (updateLastSavedTimeProperty)
    Assert.IsTrue((DateTime.Now - lastSavedTimeNew).Days < 1);
else
    Assert.AreEqual(new DateTime(2021, 5, 11, 6, 32, 0), 
        lastSavedTimeNew);
```

### 也可以看看

* class [SaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
