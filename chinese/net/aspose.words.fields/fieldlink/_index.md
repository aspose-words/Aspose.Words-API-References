---
title: FieldLink Class
linktitle: FieldLink
articleTitle: FieldLink
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Fields.FieldLink 类，实现无缝 LINK 字段。立即使用强大的功能增强您的文档处理能力！
type: docs
weight: 2520
url: /zh/net/aspose.words.fields/fieldlink/
---
## FieldLink class

实现 LINK 字段。

要了解更多信息，请访问[使用字段](https://docs.aspose.com/words/net/working-with-fields/)文档文章。

```csharp
public class FieldLink : Field
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [FieldLink](fieldlink/)() | 默认构造函数。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [AutoUpdate](../../aspose.words.fields/fieldlink/autoupdate/) { get; set; } | 获取或设置是否自动更新此字段。 |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | 获取表示显示字段结果的文本。 |
| [End](../../aspose.words.fields/field/end/) { get; } | 获取代表字段结束的节点。 |
| [Format](../../aspose.words.fields/field/format/) { get; } | 获得[`FieldFormat`](../fieldformat/)提供对字段格式进行类型化访问的对象。 |
| [FormatUpdateType](../../aspose.words.fields/fieldlink/formatupdatetype/) { get; set; } | 获取或设置链接对象更新其格式的方式。 |
| [InsertAsBitmap](../../aspose.words.fields/fieldlink/insertasbitmap/) { get; set; } | 获取或设置是否将链接对象作为位图插入。 |
| [InsertAsHtml](../../aspose.words.fields/fieldlink/insertashtml/) { get; set; } | 获取或设置是否将链接对象插入为 HTML 格式的文本。 |
| [InsertAsPicture](../../aspose.words.fields/fieldlink/insertaspicture/) { get; set; } | 获取或设置是否将链接对象作为图片插入。 |
| [InsertAsRtf](../../aspose.words.fields/fieldlink/insertasrtf/) { get; set; } | 获取或设置是否以富文本格式 (RTF) 插入链接对象。 |
| [InsertAsText](../../aspose.words.fields/fieldlink/insertastext/) { get; set; } | 获取或设置是否以纯文本格式插入链接对象。 |
| [InsertAsUnicode](../../aspose.words.fields/fieldlink/insertasunicode/) { get; set; } | 获取或设置是否将链接对象插入为 Unicode 文本。 |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | 获取或设置字段的当前结果是否由于对文档所做的其他修改而不再正确（陈旧）。 |
| [IsLinked](../../aspose.words.fields/fieldlink/islinked/) { get; set; } | 获取或设置是否通过不将图形数据与文档一起存储来减小文件大小。 |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | 获取或设置字段是否被锁定（不应重新计算其结果）。 |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | 获取或设置字段的 LCID。 |
| [ProgId](../../aspose.words.fields/fieldlink/progid/) { get; set; } | 获取或设置链接信息的应用类型。 |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | 获取或设置字段分隔符和字段结尾之间的文本。 |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | 获取表示字段分隔符的节点。可以是`无效的`. |
| [SourceFullName](../../aspose.words.fields/fieldlink/sourcefullname/) { get; set; } | 获取或设置源文件的名称和位置。 |
| [SourceItem](../../aspose.words.fields/fieldlink/sourceitem/) { get; set; } | 获取或设置正在链接的源文件部分。 |
| [Start](../../aspose.words.fields/field/start/) { get; } | 获取表示字段开始的节点。 |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | 获取 Microsoft Word 字段类型。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | 返回字段开始和字段分隔符之间的文本（如果没有分隔符，则返回字段结束）。 包括子字段的字段代码和字段结果。 |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | 返回字段开始和字段分隔符之间的文本（如果没有分隔符，则返回字段结束）。 |
| [Remove](../../aspose.words.fields/field/remove/)() | 从文档中移除该字段。返回紧接该字段之后的节点。如果该字段的末尾是其父节点的最后一个 child ，则返回其父段落。如果该字段已被移除，则返回`无效的`. |
| [Unlink](../../aspose.words.fields/field/unlink/)() | 执行字段取消链接。 |
| [Update](../../aspose.words.fields/field/update/)() | 执行字段更新。如果字段已在更新，则抛出异常。 |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | 执行字段更新。如果字段已在更新，则抛出异常。 |

## 评论

对于从其他应用程序复制的信息，此字段将该信息链接到其原始 源文件。

## 例子

展示如何使用各种字段类型链接到本地文件系统中的其他文档并显示其内容。

```csharp
public void FieldLinkedObjectsAsText(InsertLinkedObjectAs insertLinkedObjectAs)
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // 以下是我们可以用来以文本形式显示链接文档内容的三种类型的字段。
    // 1 - LINK 字段：
    builder.Writeln("FieldLink:\n");
    InsertFieldLink(builder, insertLinkedObjectAs, "Word.Document.8", MyDir + "Document.docx", null, true);

    // 2 - DDE 字段：
    builder.Writeln("FieldDde:\n");
    InsertFieldDde(builder, insertLinkedObjectAs, "Excel.Sheet", MyDir + "Spreadsheet.xlsx",
        "Sheet1!R1C1", true, true);

    // 3 - DDEAUTO 字段：
    builder.Writeln("FieldDdeAuto:\n");
    InsertFieldDdeAuto(builder, insertLinkedObjectAs, "Excel.Sheet", MyDir + "Spreadsheet.xlsx",
        "Sheet1!R1C1", true);

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.LINK.DDE.DDEAUTO.docx");
}

public void FieldLinkedObjectsAsImage(InsertLinkedObjectAs insertLinkedObjectAs)
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // 以下是我们可以用来以图像形式显示链接文档内容的三种类型的字段。
    // 1 - LINK 字段：
    builder.Writeln("FieldLink:\n");
    InsertFieldLink(builder, insertLinkedObjectAs, "Excel.Sheet", MyDir + "MySpreadsheet.xlsx",
        "Sheet1!R2C2", true);

    // 2 - DDE 字段：
    builder.Writeln("FieldDde:\n");
    InsertFieldDde(builder, insertLinkedObjectAs, "Excel.Sheet", MyDir + "Spreadsheet.xlsx",
        "Sheet1!R1C1", true, true);

    // 3 - DDEAUTO 字段：
    builder.Writeln("FieldDdeAuto:\n");
    InsertFieldDdeAuto(builder, insertLinkedObjectAs, "Excel.Sheet", MyDir + "Spreadsheet.xlsx",
        "Sheet1!R1C1", true);

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.LINK.DDE.DDEAUTO.AsImage.docx");
}

/// <summary>
/// 使用文档生成器插入 LINK 字段并根据参数设置其属性。
/// </summary>
private static void InsertFieldLink(DocumentBuilder builder, InsertLinkedObjectAs insertLinkedObjectAs,
    string progId, string sourceFullName, string sourceItem, bool shouldAutoUpdate)
{
    FieldLink field = (FieldLink)builder.InsertField(FieldType.FieldLink, true);

    switch (insertLinkedObjectAs)
    {
        case InsertLinkedObjectAs.Text:
            field.InsertAsText = true;
            break;
        case InsertLinkedObjectAs.Unicode:
            field.InsertAsUnicode = true;
            break;
        case InsertLinkedObjectAs.Html:
            field.InsertAsHtml = true;
            break;
        case InsertLinkedObjectAs.Rtf:
            field.InsertAsRtf = true;
            break;
        case InsertLinkedObjectAs.Picture:
            field.InsertAsPicture = true;
            break;
        case InsertLinkedObjectAs.Bitmap:
            field.InsertAsBitmap = true;
            break;
    }

    field.AutoUpdate = shouldAutoUpdate;
    field.ProgId = progId;
    field.SourceFullName = sourceFullName;
    field.SourceItem = sourceItem;

    builder.Writeln("\n");
}

/// <summary>
/// 使用文档生成器插入 DDE 字段，并根据参数设置其属性。
/// </summary>
private static void InsertFieldDde(DocumentBuilder builder, InsertLinkedObjectAs insertLinkedObjectAs, string progId,
    string sourceFullName, string sourceItem, bool isLinked, bool shouldAutoUpdate)
{
    FieldDde field = (FieldDde)builder.InsertField(FieldType.FieldDDE, true);

    switch (insertLinkedObjectAs)
    {
        case InsertLinkedObjectAs.Text:
            field.InsertAsText = true;
            break;
        case InsertLinkedObjectAs.Unicode:
            field.InsertAsUnicode = true;
            break;
        case InsertLinkedObjectAs.Html:
            field.InsertAsHtml = true;
            break;
        case InsertLinkedObjectAs.Rtf:
            field.InsertAsRtf = true;
            break;
        case InsertLinkedObjectAs.Picture:
            field.InsertAsPicture = true;
            break;
        case InsertLinkedObjectAs.Bitmap:
            field.InsertAsBitmap = true;
            break;
    }

    field.AutoUpdate = shouldAutoUpdate;
    field.ProgId = progId;
    field.SourceFullName = sourceFullName;
    field.SourceItem = sourceItem;
    field.IsLinked = isLinked;

    builder.Writeln("\n");
}

/// <summary>
/// 使用文档生成器插入 DDEAUTO 字段并根据参数设置其属性。
/// </summary>
private static void InsertFieldDdeAuto(DocumentBuilder builder, InsertLinkedObjectAs insertLinkedObjectAs,
    string progId, string sourceFullName, string sourceItem, bool isLinked)
{
    FieldDdeAuto field = (FieldDdeAuto)builder.InsertField(FieldType.FieldDDEAuto, true);

    switch (insertLinkedObjectAs)
    {
        case InsertLinkedObjectAs.Text:
            field.InsertAsText = true;
            break;
        case InsertLinkedObjectAs.Unicode:
            field.InsertAsUnicode = true;
            break;
        case InsertLinkedObjectAs.Html:
            field.InsertAsHtml = true;
            break;
        case InsertLinkedObjectAs.Rtf:
            field.InsertAsRtf = true;
            break;
        case InsertLinkedObjectAs.Picture:
            field.InsertAsPicture = true;
            break;
        case InsertLinkedObjectAs.Bitmap:
            field.InsertAsBitmap = true;
            break;
    }

    field.ProgId = progId;
    field.SourceFullName = sourceFullName;
    field.SourceItem = sourceItem;
    field.IsLinked = isLinked;
}

public enum InsertLinkedObjectAs
{
    // 链接对象作为文本
    Text,
    Unicode,
    Html,
    Rtf,
    // 链接对象作为图像
    Picture,
    Bitmap
}
```

### 也可以看看

* class [Field](../field/)
* 命名空间 [Aspose.Words.Fields](../../aspose.words.fields/)
* 部件 [Aspose.Words](../../)
