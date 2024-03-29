---
title: SaveOptions.FlatOpcXmlMappingOnly
second_title: Aspose.Words for .NET API 参考
description: SaveOptions 财产. 获取或设置值确定允许映射哪些文档格式XmlMapping. 仅默认FlatOpc允许映射文档格式
type: docs
weight: 90
url: /zh/net/aspose.words.saving/saveoptions/flatopcxmlmappingonly/
---
## SaveOptions.FlatOpcXmlMappingOnly property

获取或设置值，确定允许映射哪些文档格式[`XmlMapping`](../../../aspose.words.markup/structureddocumenttag/xmlmapping/). 仅默认FlatOpc允许映射文档格式。

```csharp
public bool FlatOpcXmlMappingOnly { get; set; }
```

### 评论

此选项与[`FlatOpcXmlMappingOnly`](../../../aspose.words.loading/loadoptions/flatopcxmlmappingonly/). 通常您需要将它们都设置为 false 以允许映射任意文档格式。

### 例子

展示如何将结构化文档标签绑定到任何格式。

```csharp
// 如果为 true - SDT 将包含原始 HTML 文本。
// 如果为 false - 将解析映射的 HTML，并将生成的文档插入到 SDT 内容中。
LoadOptions loadOptions = new LoadOptions { FlatOpcXmlMappingOnly = isFlatOpcXmlMappingOnly };
Document doc = new Document(MyDir + "Structured document tag with HTML content.docx", loadOptions);

SaveOptions saveOptions = SaveOptions.CreateSaveOptions(SaveFormat.Pdf);
saveOptions.FlatOpcXmlMappingOnly = isFlatOpcXmlMappingOnly;

doc.Save(ArtifactsDir + "LoadOptions.FlatOpcXmlMappingOnly.pdf", saveOptions);
```

### 也可以看看

* class [SaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../saveoptions/)
* 部件 [Aspose.Words](../../../)


