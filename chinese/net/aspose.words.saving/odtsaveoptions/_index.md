---
title: OdtSaveOptions Class
linktitle: OdtSaveOptions
articleTitle: OdtSaveOptions
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.Saving.OdtSaveOptions 班级. 可用于在将文档保存到Odt或 Ott格式 在 C#.
type: docs
weight: 5330
url: /zh/net/aspose.words.saving/odtsaveoptions/
---
## OdtSaveOptions class

可用于在将文档保存到Odt或 Ott格式.

要了解更多信息，请访问[指定保存选项](https://docs.aspose.com/words/net/specify-save-options/)文档文章。

```csharp
public class OdtSaveOptions : SaveOptions
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [OdtSaveOptions](odtsaveoptions/#constructor)() | 初始化此类的一个新实例，该实例可用于将文档保存在Odt格式. |
| [OdtSaveOptions](odtsaveoptions/#constructor_1)(*[SaveFormat](../../aspose.words/saveformat/)*) | 初始化此类的一个新实例，该实例可用于将文档保存在Odt或 Ott格式. |
| [OdtSaveOptions](odtsaveoptions/#constructor_2)(*string*) | 初始化此类的一个新实例，该实例可用于将文档保存在Odt format 使用密码加密。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/) { get; set; } | 获取或设置一个布尔值，指示在保存的文档中嵌入 TrueType 字体时是否允许使用 PostScript 轮廓嵌入字体。 默认值为`错误的`. |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo/) { get; set; } | 获取或设置用于日期/时间字段的自定义本地时区。 |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate/) { get; set; } | 获取或设置默认模板的路径（包括文件名）。 此属性的默认值为**空字符串**（Empty). |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode/) { get; set; } | 获取或设置一个确定如何渲染 3D 效果的值。 |
| virtual [DmlEffectsRenderingMode](../../aspose.words.saving/saveoptions/dmleffectsrenderingmode/) { get; set; } | 获取或设置一个值，确定如何呈现 DrawingML 效果。 |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode/) { get; set; } | 获取或设置一个值，确定如何呈现 DrawingML 形状。 |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname/) { get; set; } | 当`真的` ，导致 Aspose.Words 的名称和版本嵌入到生成的文件中。 默认值为`真的`. |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode/) { get; set; } | 获取或设置一个值，确定如何呈现墨迹 (InkML) 对象。 |
| [IsStrictSchema11](../../aspose.words.saving/odtsaveoptions/isstrictschema11/) { get; set; } | 指定导出是否应严格符合 ODT 规范 1.1。 OOo 3.0 在文件包含 ODT 1.2 的元素和属性时正确显示文件。 为此目的使用“false”，或严格符合规范 1.1. 使用“true”默认值为`错误的`. |
| [MeasureUnit](../../aspose.words.saving/odtsaveoptions/measureunit/) { get; set; } | 允许指定应用于文档内容的测量单位。 默认值为Centimeters |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization/) { get; set; } | 获取或设置确定在保存文档之前是否应执行内存优化的值。 此属性的默认值为`错误的`. |
| [Password](../../aspose.words.saving/odtsaveoptions/password/) { get; set; } | 获取或设置加密文档的密码。 |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat/) { get; set; } | 当`真的`，在适用的情况下漂亮的格式输出。 默认值为`错误的`. |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback/) { get; set; } | 在保存文档期间调用并接受有关保存进度的数据。 |
| override [SaveFormat](../../aspose.words.saving/odtsaveoptions/saveformat/) { get; set; } | 指定使用此保存选项对象时保存文档的格式。 可以Odt或者Ott. |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder/) { get; set; } | 指定保存到 DOC 或 DOCX 文件时使用的临时文件的文件夹。 默认情况下，此属性为`无效的`并且没有使用临时文件。 |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty/) { get; set; } | 获取或设置一个值，确定是否[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime/)属性在保存前更新。 默认值为`错误的`; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields/) { get; set; } | 获取或设置一个值，确定在将文档保存为固定页面格式之前是否应更新某些类型的字段。 此属性的默认值为`真的`. |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty/) { get; set; } | 获取或设置一个值，确定是否[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted/)属性在保存前更新。 |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty/) { get; set; } | 获取或设置一个值，确定是否[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime/)属性在保存前更新。 |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing/) { get; set; } | 获取或设置一个值，确定是否使用抗锯齿进行渲染。 |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering/) { get; set; } | 获取或设置一个值，确定是否使用高质量（即慢速）渲染算法。 |

## 评论

目前仅提供[`SaveFormat`](./saveformat/)属性，但将来会添加 其他选项，例如加密密码或数字签名设置。

## 例子

演示如何使保存的文档符合旧版 ODT 架构。

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

OdtSaveOptions saveOptions = new OdtSaveOptions
{
    MeasureUnit = OdtSaveMeasureUnit.Centimeters,
    IsStrictSchema11 = exportToOdt11Specs
};

doc.Save(ArtifactsDir + "OdtSaveOptions.Odt11Schema.odt", saveOptions);
```

演示如何使用不同的测量单位来定义已保存 ODT 文档的样式参数。

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// 当我们将文档导出为.odt时，我们可以使用OdtSaveOptions对象来修改保存文档的方式。
// 我们可以将“MeasureUnit”属性设置为“OdtSaveMeasureUnit.Centimeters”
 // 使用 Open Office 使用的公制来定义样式参数等内容。
// 我们可以将“MeasureUnit”属性设置为“OdtSaveMeasureUnit.Inches”
// 使用 Microsoft Word 使用的英制系统来定义样式参数等内容。
OdtSaveOptions saveOptions = new OdtSaveOptions
{
    MeasureUnit = odtSaveMeasureUnit
};

doc.Save(ArtifactsDir + "OdtSaveOptions.Odt11Schema.odt", saveOptions);
```

### 也可以看看

* class [SaveOptions](../saveoptions/)
* 命名空间 [Aspose.Words.Saving](../../aspose.words.saving/)
* 部件 [Aspose.Words](../../)
