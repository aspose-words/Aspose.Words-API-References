---
title: OoxmlSaveOptions
second_title: Aspose.Words for .NET API 参考
description: 可用于在将文档保存到Docx  DocmDotxDotmor FlatOpc格式.
type: docs
weight: 5070
url: /zh/net/aspose.words.saving/ooxmlsaveoptions/
---
## OoxmlSaveOptions class

可用于在将文档保存到Docx , Docm,Dotx,Dotmor FlatOpc格式.

```csharp
public class OoxmlSaveOptions : SaveOptions
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [OoxmlSaveOptions](ooxmlsaveoptions#constructor)() | 初始化此类的新实例，该实例可用于将文档保存在Docx格式. |
| [OoxmlSaveOptions](ooxmlsaveoptions#constructor_1)(SaveFormat) | 初始化此类的新实例，该实例可用于将文档保存在Docx , Docm,Dotx,Dotmor FlatOpc格式. |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts) { get; set; } | 获取或设置一个布尔值，该值指示是否允许在保存文档中嵌入 TrueType 字体时使用 PostScript 轮廓嵌入字体 。 默认值为 **错误的**. |
| [Compliance](../../aspose.words.saving/ooxmlsaveoptions/compliance) { get; set; } | 指定输出文档的 OOXML 版本。 默认值为Ecma376_2006. |
| [CompressionLevel](../../aspose.words.saving/ooxmlsaveoptions/compressionlevel) { get; set; } | 指定用于保存文档的压缩级别。 默认值为Normal. |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo) { get; set; } | 获取或设置用于日期/时间字段的自定义本地时区。 |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate) { get; set; } | 获取或设置默认模板的路径（包括文件名）。 此属性的默认值为 **空字符串**(Empty ). |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode) { get; set; } | 获取或设置一个值，确定如何渲染 3D 效果。 |
| virtual [DmlEffectsRenderingMode](../../aspose.words.saving/saveoptions/dmleffectsrenderingmode) { get; set; } | 获取或设置一个值，确定如何呈现 DrawingML 效果。 |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode) { get; set; } | 获取或设置一个值，确定如何呈现 DrawingML 形状。 |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname) { get; set; } | 如果为真，则将 Aspose.Words 的名称和版本嵌入到生成的文件中。 默认值为 **真的**. |
| [FlatOpcXmlMappingOnly](../../aspose.words.saving/saveoptions/flatopcxmlmappingonly) { get; set; } | 获取或设置值，确定允许映射哪些文档格式[`XmlMapping`](../../aspose.words.markup/structureddocumenttag/xmlmapping). 仅默认FlatOpc允许映射文档格式。 |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode) { get; set; } | 获取或设置一个值，确定如何呈现墨水 (InkML) 对象。 |
| [KeepLegacyControlChars](../../aspose.words.saving/ooxmlsaveoptions/keeplegacycontrolchars) { get; set; } | 保留旧版控制字符的原始表示。 |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization) { get; set; } | 获取或设置值确定是否应在保存文档之前执行内存优化。 此属性的默认值为 **错误的**. |
| [Password](../../aspose.words.saving/ooxmlsaveoptions/password) { get; set; } | 获取/设置密码以使用 ECMA376 标准加密算法加密文档。 |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat) { get; set; } | 什么时候`真的` , 在适用的情况下输出漂亮的格式。 默认值为 **错误的**. |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback) { get; set; } | 在保存文档期间调用并接受有关保存进度的数据。 |
| override [SaveFormat](../../aspose.words.saving/ooxmlsaveoptions/saveformat) { get; set; } | 指定使用此保存选项对象时将保存文档的格式。 可以是Docx,Docm , Dotx,Dotm或者FlatOpc. |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder) { get; set; } | 指定保存到 DOC 或 DOCX 文件时使用的临时文件的文件夹。 默认情况下，此属性为`无效的`并且没有使用临时文件。 |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty) { get; set; } | 获取或设置一个值，确定是否[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime)属性在保存前更新。 默认值为 false； |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields) { get; set; } | 获取或设置一个值，该值确定在将文档保存为固定页面格式之前是否应更新某些类型的字段。 此属性的默认值为 **真的**. |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty) { get; set; } | 获取或设置一个值，确定是否[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted)属性在保存之前更新。 |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty) { get; set; } | 获取或设置一个值，确定是否[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime)属性在保存之前更新。 |
| [UpdateSdtContent](../../aspose.words.saving/saveoptions/updatesdtcontent) { get; set; } | 获取或设置值确定内容是否[`StructuredDocumentTag`](../../aspose.words.markup/structureddocumenttag)在保存之前更新。 |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing) { get; set; } | 获取或设置一个值，确定是否使用抗锯齿进行渲染。 |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering) { get; set; } | 获取或设置一个确定是否使用高质量（即慢速）渲染算法的值。 |

### 例子

演示如何设置要遵守的已保存文档的 OOXML 合规性规范。

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

// 我们保存的文档使用 DML 定义形状以符合“ISO/IEC 29500:2008”OOXML 标准。
doc = new Document(ArtifactsDir + "OoxmlSaveOptions.Iso29500Strict.docx");

Assert.AreEqual(ShapeMarkupLanguage.Dml, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).MarkupLanguage);
```

### 也可以看看

* class [SaveOptions](../saveoptions)
* 命名空间 [Aspose.Words.Saving](../../aspose.words.saving)
* 部件 [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
