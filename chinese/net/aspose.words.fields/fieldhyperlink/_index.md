---
title: FieldHyperlink
second_title: Aspose.Words for .NET API 参考
description: 实现 HYPERLINK 字段
type: docs
weight: 1840
url: /zh/net/aspose.words.fields/fieldhyperlink/
---
## FieldHyperlink class

实现 HYPERLINK 字段

```csharp
public class FieldHyperlink : Field
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [FieldHyperlink](fieldhyperlink)() | 默认构造函数。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Address](../../aspose.words.fields/fieldhyperlink/address) { get; set; } | 获取或设置此超链接跳转的位置。 |
| [DisplayResult](../../aspose.words.fields/field/displayresult) { get; } | 获取表示显示字段结果的文本。 |
| [End](../../aspose.words.fields/field/end) { get; } | 获取代表字段end的节点。 |
| [Format](../../aspose.words.fields/field/format) { get; } | 得到一个[`FieldFormat`](../fieldformat)提供对字段格式的类型化访问的对象。 |
| [IsDirty](../../aspose.words.fields/field/isdirty) { get; set; } | 获取或设置字段的当前结果是否由于对文档的其他修改而不再正确（陈旧）。 |
| [IsImageMap](../../aspose.words.fields/fieldhyperlink/isimagemap) { get; set; } | 获取或设置是否将坐标附加到服务器端图像映射的超链接。 |
| [IsLocked](../../aspose.words.fields/field/islocked) { get; set; } | 获取或设置字段是否被锁定（不应重新计算其结果）。 |
| [LocaleId](../../aspose.words.fields/field/localeid) { get; set; } | 获取或设置字段的LCID。 |
| [OpenInNewWindow](../../aspose.words.fields/fieldhyperlink/openinnewwindow) { get; set; } | 获取或设置是否在新的 Web 浏览器窗口中打开目标站点。 |
| [Result](../../aspose.words.fields/field/result) { get; set; } | 获取或设置字段分隔符和字段结尾之间的文本。 |
| [ScreenTip](../../aspose.words.fields/fieldhyperlink/screentip) { get; set; } | 获取或设置超链接的屏幕提示文本。 |
| [Separator](../../aspose.words.fields/field/separator) { get; } | 获取表示字段分隔符的节点。可以为空。 |
| [Start](../../aspose.words.fields/field/start) { get; } | 获取表示字段开始的节点。 |
| [SubAddress](../../aspose.words.fields/fieldhyperlink/subaddress) { get; set; } | 获取或设置文件中的位置，例如书签，此超链接跳转的位置。 |
| [Target](../../aspose.words.fields/fieldhyperlink/target) { get; set; } | 获取或设置链接应重定向到的目标。 |
| virtual [Type](../../aspose.words.fields/field/type) { get; } | 获取 Microsoft Word 字段类型。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)() | 返回字段开始和字段分隔符之间的文本（或字段结束，如果没有分隔符）。 包括子字段的字段代码和字段结果。 |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)(bool) | 返回字段开始和字段分隔符之间的文本（如果没有分隔符，则返回字段结束）。 |
| [Remove](../../aspose.words.fields/field/remove)() | 从文档中删除字段。在字段之后返回一个节点。如果字段的结尾是其父节点的最后一个 child ，则返回其父段落。如果该字段已被删除，则返回 **无效的**. |
| [Unlink](../../aspose.words.fields/field/unlink)() | 执行字段取消链接。 |
| [Update](../../aspose.words.fields/field/update)() | 执行字段更新。如果该字段已被更新，则抛出。 |
| [Update](../../aspose.words.fields/field/update)(bool) | 执行字段更新。如果该字段已被更新，则抛出。 |

### 评论

选中后，使控件跳转到书签或 URL 等位置。

### 例子

展示如何使用 HYPERLINK 字段链接到本地文件系统中的文档。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldHyperlink field = (FieldHyperlink)builder.InsertField(FieldType.FieldHyperlink, true);

// 当我们在 Microsoft Word 中单击此 HYPERLINK 字段时，
// 它将打开链接的文档，然后将光标放在指定的书签上。
field.Address = MyDir + "Bookmarks.docx";
field.SubAddress = "MyBookmark3";
field.ScreenTip = "Open " + field.Address + " on bookmark " + field.SubAddress + " in a new window";

builder.Writeln();

// 当我们在 Microsoft Word 中单击此 HYPERLINK 字段时，
// 它将打开链接的文档，并自动向下滚动到指定的 iframe。
field = (FieldHyperlink)builder.InsertField(FieldType.FieldHyperlink, true);
field.Address = MyDir + "Iframes.html";
field.ScreenTip = "Open " + field.Address;
field.Target = "iframe_3";
field.OpenInNewWindow = true;
field.IsImageMap = false;

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.HYPERLINK.docx");
```

### 也可以看看

* class [Field](../field)
* 命名空间 [Aspose.Words.Fields](../../aspose.words.fields)
* 部件 [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->