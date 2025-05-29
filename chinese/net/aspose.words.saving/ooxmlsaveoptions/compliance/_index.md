---
title: OoxmlSaveOptions.Compliance
linktitle: Compliance
articleTitle: Compliance
second_title: Aspose.Words for .NET
description: 了解 OoxmlSaveOptions 合规性，选择输出文档的 OOXML 版本。使用默认的 Ecma376_2006 设置优化您的文件。
type: docs
weight: 20
url: /zh/net/aspose.words.saving/ooxmlsaveoptions/compliance/
---
## OoxmlSaveOptions.Compliance property

指定输出文档的 OOXML 版本。 默认值为Ecma376_2006.

```csharp
public OoxmlCompliance Compliance { get; set; }
```

## 例子

展示如何将 DML 形状插入文档。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 以下是形状可能具有的两种包装类型。
// 1 - 浮动：
builder.InsertShape(ShapeType.TopCornersRounded, RelativeHorizontalPosition.Page, 100,
        RelativeVerticalPosition.Page, 100, 50, 50, WrapType.None);

// 2 - 内联：
builder.InsertShape(ShapeType.DiagonalCornersRounded, 50, 50);

// 如果需要创建“非原始”形状，例如 SingleCornerSnipped、TopCornersSnipped、DiagonalCornersSnipped，
// TopCornersOneRoundedOneSnipped、SingleCornerRounded、TopCornersRounded 或 DiagonalCornersRounded，
// 然后以“严格”或“过渡”合规性保存文档，这允许将形状保存为 DML。
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(SaveFormat.Docx);
saveOptions.Compliance = OoxmlCompliance.Iso29500_2008_Transitional;

doc.Save(ArtifactsDir + "Shape.ShapeInsertion.docx", saveOptions);
```

显示如何配置列表以在每个部分重新开始编号。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

doc.Lists.Add(ListTemplate.NumberDefault);

Aspose.Words.Lists.List list = doc.Lists[0];
list.IsRestartAtEachSection = restartListAtEachSection;

// “IsRestartAtEachSection”属性仅在以下情况下适用
// 该文档的 OOXML 合规级别符合比“OoxmlComplianceCore.Ecma376”更新的标准。
OoxmlSaveOptions options = new OoxmlSaveOptions
{
    Compliance = OoxmlCompliance.Iso29500_2008_Transitional
};

builder.ListFormat.List = list;

builder.Writeln("List item 1");
builder.Writeln("List item 2");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Writeln("List item 3");
builder.Writeln("List item 4");

doc.Save(ArtifactsDir + "OoxmlSaveOptions.RestartingDocumentList.docx", options);

doc = new Document(ArtifactsDir + "OoxmlSaveOptions.RestartingDocumentList.docx");

Assert.AreEqual(restartListAtEachSection, doc.Lists[0].IsRestartAtEachSection);
```

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

* enum [OoxmlCompliance](../../ooxmlcompliance/)
* class [OoxmlSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
