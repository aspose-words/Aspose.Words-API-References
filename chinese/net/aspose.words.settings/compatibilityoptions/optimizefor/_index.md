---
title: CompatibilityOptions.OptimizeFor
second_title: Aspose.Words for .NET API 参考
description: CompatibilityOptions 方法. 允许优化文档内容以及针对特定版本的 MS Word 的默认 Aspose.Words 行为
type: docs
weight: 720
url: /zh/net/aspose.words.settings/compatibilityoptions/optimizefor/
---
## CompatibilityOptions.OptimizeFor method

允许优化文档内容以及针对特定版本的 MS Word 的默认 Aspose.Words 行为。

使用此方法可以防止 MS Word 在加载文档时显示“兼容模式”功能区。 （请注意，您可能还需要设置[`Compliance`](../../../aspose.words.saving/ooxmlsaveoptions/compliance/)属性为 Iso29500_2008_Transitional或更高。）

```csharp
public void OptimizeFor(MsWordVersion version)
```

### 例子

演示如何垂直对齐文本框的文本内容。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.TextBox, 200, 200);

// 将“VerticalAnchor”属性设置为“TextBoxAnchor.Top”
// 将此文本框中的文本与形状的顶部对齐。
// 将“VerticalAnchor”属性设置为“TextBoxAnchor.Middle”
// 将此文本框中的文本与形状的中心对齐。
// 将“VerticalAnchor”属性设置为“TextBoxAnchor.Bottom”
// 将此文本框中的文本与形状的底部对齐。
shape.TextBox.VerticalAnchor = verticalAnchor;

builder.MoveTo(shape.FirstParagraph);
builder.Write("Hello world!");

// 从 Microsoft Word 2007 开始，文本框中文本的垂直对齐功能可用。
doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2007);
doc.Save(ArtifactsDir + "Shape.VerticalAnchor.docx");
```

演示如何为保存的文档设置要遵守的 OOXML 合规性规范。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 如果我们配置兼容性选项以符合 Microsoft Word 2003，
// 插入图像将使用 VML 定义其形状。
doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2003);
builder.InsertImage(ImageDir + "Transparent background logo.png");

Assert.AreEqual(ShapeMarkupLanguage.Vml, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).MarkupLanguage);

// “ISO/IEC 29500:2008”OOXML 标准不支持 VML 形状。
// 如果我们将 SaveOptions 对象的“Compliance”属性设置为“OoxmlCompliance.Iso29500_2008_Strict”，
 // 我们在传递此对象时保存的任何文档都必须遵循该标准。
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions
{
    Compliance = OoxmlCompliance.Iso29500_2008_Strict,
    SaveFormat = SaveFormat.Docx
};

doc.Save(ArtifactsDir + "OoxmlSaveOptions.Iso29500Strict.docx", saveOptions);

// 我们保存的文档使用 DML 定义形状，以遵守“ISO/IEC 29500:2008”OOXML 标准。
doc = new Document(ArtifactsDir + "OoxmlSaveOptions.Iso29500Strict.docx");

Assert.AreEqual(ShapeMarkupLanguage.Dml, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).MarkupLanguage);
```

演示如何针对不同版本的 Microsoft Word 优化文档。

```csharp
public void OptimizeFor()
{
    Document doc = new Document();

    // 该对象包含每个文档特有的广泛标志列表
    // 这使我们能够促进与旧版本 Microsoft Word 的向后兼容性。
    CompatibilityOptions options = doc.CompatibilityOptions;

    // 打印空白文档的默认设置。
    Console.WriteLine("\nDefault optimization settings:");
    PrintCompatibilityOptions(options);

    // 我们可以通过“文件”-> 在 Microsoft Word 中访问这些设置“选项”-> “高级”-> “兼容选项...”。
    doc.Save(ArtifactsDir + "CompatibilityOptions.OptimizeFor.DefaultSettings.docx");

    // 我们可以使用 OptimizeFor 方法来确保与特定 Microsoft Word 版本的最佳兼容性。
    doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2010);
    Console.WriteLine("\nOptimized for Word 2010:");
    PrintCompatibilityOptions(options);

    doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2000);
    Console.WriteLine("\nOptimized for Word 2000:");
    PrintCompatibilityOptions(options);
}

/// <summary>
/// 按状态对文档兼容性选项对象中的所有标志进行分组，然后打印每个组。
/// </summary>
private static void PrintCompatibilityOptions(CompatibilityOptions options)
{
    for (int i = 1; i >= 0; i--)
    {
        Console.WriteLine(Convert.ToBoolean(i) ? "\tEnabled options:" : "\tDisabled options:");
        SortedSet<string> optionNames = new SortedSet<string>();

        foreach (System.ComponentModel.PropertyDescriptor descriptor in System.ComponentModel.TypeDescriptor.GetProperties(options))
        {
            if (descriptor.PropertyType == Type.GetType("System.Boolean") && i == Convert.ToInt32(descriptor.GetValue(options)))
            {
                optionNames.Add(descriptor.Name);
            }
        }

        foreach (string s in optionNames)
        {
            Console.WriteLine($"\t\t{s}");
        }
    }
}
```

### 也可以看看

* enum [MsWordVersion](../../mswordversion/)
* class [CompatibilityOptions](../)
* 命名空间 [Aspose.Words.Settings](../../compatibilityoptions/)
* 部件 [Aspose.Words](../../../)


