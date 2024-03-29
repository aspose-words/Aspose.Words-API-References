---
title: SaveOptions.UpdateSdtContent
second_title: Aspose.Words for .NET API 参考
description: SaveOptions 财产. 获取或设置值确定内容是否StructuredDocumentTag在保存之前更新
type: docs
weight: 200
url: /zh/net/aspose.words.saving/saveoptions/updatesdtcontent/
---
## SaveOptions.UpdateSdtContent property

获取或设置值确定内容是否[`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/)在保存之前更新。

```csharp
public bool UpdateSdtContent { get; set; }
```

### 评论

默认值为`真的`.

### 例子

展示如何在将文档保存为 PDF 时更新结构化文档标签。

```csharp
Document doc = new Document();

// 插入一个下拉列表结构化文档标签。
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.DropDownList, MarkupLevel.Block);
tag.ListItems.Add(new SdtListItem("Value 1"));
tag.ListItems.Add(new SdtListItem("Value 2"));
tag.ListItems.Add(new SdtListItem("Value 3"));

// 下拉列表当前显示“选择一个项目”作为默认文本。
// 将“SelectedValue”属性设置为列表项之一以获取标签
// 显示该列表项的值而不是默认文本。
tag.ListItems.SelectedValue = tag.ListItems[1];

doc.FirstSection.Body.AppendChild(tag);

// 创建一个“PdfSaveOptions”对象以传递给文档的“Save”方法
// 修改该方法如何将文档保存为 .PDF。
PdfSaveOptions options = new PdfSaveOptions();

// 将“UpdateSdtContent”属性设置为“false”不更新结构化文档标签
// 同时将文档保存为 PDF。它们将显示它们在构建时的默认值。
// 将“UpdateSdtContent”属性设置为“true”以确保标签在 PDF 中显示更新的值。
options.UpdateSdtContent = updateSdtContent;

doc.Save(ArtifactsDir + "StructuredDocumentTag.UpdateSdtContent.pdf", options);
```

### 也可以看看

* class [SaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../saveoptions/)
* 部件 [Aspose.Words](../../../)


