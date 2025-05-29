---
title: OoxmlSaveOptions.SaveFormat
linktitle: SaveFormat
articleTitle: SaveFormat
second_title: Aspose.Words for .NET
description: 探索 OoxmlSaveOptions 的 SaveFormat 属性，轻松选择文档格式（如 Docx、Docm、Dotx、Dotm 或 FlatOpc）以实现无缝保存。
type: docs
weight: 70
url: /zh/net/aspose.words.saving/ooxmlsaveoptions/saveformat/
---
## OoxmlSaveOptions.SaveFormat property

指定如果使用此保存选项对象，文档将以哪种格式保存。 可以是Docx，Docm , Dotx，Dotm或者FlatOpc.

```csharp
public override SaveFormat SaveFormat { get; set; }
```

## 例子

展示如何设置已保存文档所遵循的 OOXML 合规性规范。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 如果我们配置兼容性选项以符合 Microsoft Word 2003，
// 插入图像将使用 VML 定义其形状。
doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2003);
builder.InsertImage(ImageDir + "Transparent background logo.png");

Assert.AreEqual(ShapeMarkupLanguage.Vml, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).MarkupLanguage);

// “ISO/IEC 29500:2008” OOXML 标准不支持 VML 形状。
// 如果我们将 SaveOptions 对象的“Compliance”属性设置为“OoxmlCompliance.Iso29500_2008_Strict”，
 // 我们在传递此对象时保存的任何文档都必须遵循该标准。
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions
{
    Compliance = OoxmlCompliance.Iso29500_2008_Strict,
    SaveFormat = SaveFormat.Docx
};

doc.Save(ArtifactsDir + "OoxmlSaveOptions.Iso29500Strict.docx", saveOptions);

// 我们保存的文档使用 DML 定义形状以遵守“ISO/IEC 29500:2008”OOXML 标准。
doc = new Document(ArtifactsDir + "OoxmlSaveOptions.Iso29500Strict.docx");

Assert.AreEqual(ShapeMarkupLanguage.Dml, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).MarkupLanguage);
```

### 也可以看看

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [OoxmlSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
