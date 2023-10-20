---
title: FieldRef Class
linktitle: FieldRef
articleTitle: FieldRef
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.Fields.FieldRef 班级. 实现 REF 字段 在 C#.
type: docs
weight: 2330
url: /zh/net/aspose.words.fields/fieldref/
---
## FieldRef class

实现 REF 字段。

要了解更多信息，请访问[使用字段](https://docs.aspose.com/words/net/working-with-fields/)文档文章。

```csharp
public class FieldRef : Field
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [FieldRef](fieldref/)() | 默认构造函数。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [BookmarkName](../../aspose.words.fields/fieldref/bookmarkname/) { get; set; } | 获取或设置引用的书签的名称。 |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | 获取表示显示的字段结果的文本。 |
| [End](../../aspose.words.fields/field/end/) { get; } | 获取表示字段结束的节点。 |
| [Format](../../aspose.words.fields/field/format/) { get; } | 获得[`FieldFormat`](../fieldformat/)提供对字段格式的类型化访问的对象。 |
| [IncludeNoteOrComment](../../aspose.words.fields/fieldref/includenoteorcomment/) { get; set; } | 获取或设置是否增加书签标记的脚注、尾注和注释编号，并插入相应的脚注、尾注和注释文本。 |
| [InsertHyperlink](../../aspose.words.fields/fieldref/inserthyperlink/) { get; set; } | 获取或设置是否创建指向已添加书签的段落的超链接。 |
| [InsertParagraphNumber](../../aspose.words.fields/fieldref/insertparagraphnumber/) { get; set; } | 获取或设置是否按照文档中显示的方式插入引用段落的段落编号。 |
| [InsertParagraphNumberInFullContext](../../aspose.words.fields/fieldref/insertparagraphnumberinfullcontext/) { get; set; } | 获取或设置是否在完整上下文中插入引用段落的段落编号。 |
| [InsertParagraphNumberInRelativeContext](../../aspose.words.fields/fieldref/insertparagraphnumberinrelativecontext/) { get; set; } | 获取或设置是否在相对上下文中插入引用段落的段落编号。 |
| [InsertRelativePosition](../../aspose.words.fields/fieldref/insertrelativeposition/) { get; set; } | 获取或设置是否插入引用段落的相对位置。 |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | 获取或设置字段的当前结果是否由于对文档进行的其他修改而不再正确（陈旧）。 |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | 获取或设置字段是否被锁定（不应重新计算其结果）。 |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | 获取或设置字段的 LCID。 |
| [NumberSeparator](../../aspose.words.fields/fieldref/numberseparator/) { get; set; } | 获取或设置用于分隔序列号和页码的字符序列。 |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | 获取或设置字段分隔符和字段结束之间的文本。 |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | 获取表示字段分隔符的节点。可`无效的`. |
| [Start](../../aspose.words.fields/field/start/) { get; } | 获取表示字段开始的节点。 |
| [SuppressNonDelimiters](../../aspose.words.fields/fieldref/suppressnondelimiters/) { get; set; } | 获取或设置是否隐藏非分隔符。 |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | 获取 Microsoft Word 字段类型。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | 返回字段开始和字段分隔符之间的文本（如果没有分隔符，则返回字段结束）。 包括子字段的字段代码和字段结果。 |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | 返回字段开始和字段分隔符之间的文本（如果没有分隔符，则返回字段结束）。 |
| [Remove](../../aspose.words.fields/field/remove/)() | 从文档中删除该字段。返回字段后面的节点。如果字段的结尾是其父节点的最后一个 child ，则返回其父段落。如果该字段已被删除，则返回`无效的`. |
| [Unlink](../../aspose.words.fields/field/unlink/)() | 执行字段取消链接。 |
| [Update](../../aspose.words.fields/field/update/)() | 执行字段更新。如果该字段已被更新，则抛出异常。 |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | 执行字段更新。如果该字段已被更新，则抛出异常。 |

## 评论

插入由指定书签表示的文本或图形。

## 例子

演示如何使用 SET 字段创建带书签的文本，然后使用 REF 字段将其显示在文档中。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

 // 使用 SET 字段命名已添加书签的文本。
// 该字段指的是“书签”，不是出现在文本中的书签结构，而是一个命名变量。
FieldSet fieldSet = (FieldSet)builder.InsertField(FieldType.FieldSet, false);
fieldSet.BookmarkName = "MyBookmark";
fieldSet.BookmarkText = "Hello world!";
fieldSet.Update();

Assert.AreEqual(" SET  MyBookmark \"Hello world!\"", fieldSet.GetFieldCode());

// 在 REF 字段中按名称引用书签并显示其内容。
FieldRef fieldRef = (FieldRef)builder.InsertField(FieldType.FieldRef, true);
fieldRef.BookmarkName = "MyBookmark";
fieldRef.Update();

Assert.AreEqual(" REF  MyBookmark", fieldRef.GetFieldCode());
Assert.AreEqual("Hello world!", fieldRef.Result);

doc.Save(ArtifactsDir + "Field.SET.REF.docx");
```

演示如何将 REF 字段插入到参考书签。

```csharp
public void FieldRef()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.StartBookmark("MyBookmark");
    builder.InsertFootnote(FootnoteType.Footnote, "MyBookmark footnote #1");
    builder.Write("Text that will appear in REF field");
    builder.InsertFootnote(FootnoteType.Footnote, "MyBookmark footnote #2");
    builder.EndBookmark("MyBookmark");
    builder.MoveToDocumentStart();

    // 我们将应用自定义列表格式，其中尖括号的数量表示我们当前所处的列表级别。
    builder.ListFormat.ApplyNumberDefault();
    builder.ListFormat.ListLevel.NumberFormat = "> \x0000";

    // 插入一个 REF 字段，该字段将包含书签中的文本，充当超链接，并克隆书签的脚注。
    FieldRef field = InsertFieldRef(builder, "MyBookmark", "", "\n");
    field.IncludeNoteOrComment = true;
    field.InsertHyperlink = true;

    Assert.AreEqual(" REF  MyBookmark \\f \\h", field.GetFieldCode());

    // 插入一个 REF 字段，并显示引用的书签是在其上方还是下方。
    field = InsertFieldRef(builder, "MyBookmark", "The referenced paragraph is ", " this field.\n");
    field.InsertRelativePosition = true;

    Assert.AreEqual(" REF  MyBookmark \\p", field.GetFieldCode());

    // 显示文档中出现的书签的列表编号。
    field = InsertFieldRef(builder, "MyBookmark", "The bookmark's paragraph number is ", "\n");
    field.InsertParagraphNumber = true;

    Assert.AreEqual(" REF  MyBookmark \\n", field.GetFieldCode());

    // 显示书签的列表编号，但省略非分隔符（例如尖括号）。
    field = InsertFieldRef(builder, "MyBookmark", "The bookmark's paragraph number, non-delimiters suppressed, is ", "\n");
    field.InsertParagraphNumber = true;
    field.SuppressNonDelimiters = true;

    Assert.AreEqual(" REF  MyBookmark \\n \\t", field.GetFieldCode());

    // 向下移动一级列表。
    builder.ListFormat.ListLevelNumber++;
    builder.ListFormat.ListLevel.NumberFormat = ">> \x0001";

    // 显示书签的列表编号及其上方所有列表级别的编号。
    field = InsertFieldRef(builder, "MyBookmark", "The bookmark's full context paragraph number is ", "\n");
    field.InsertParagraphNumberInFullContext = true;

    Assert.AreEqual(" REF  MyBookmark \\w", field.GetFieldCode());

    builder.InsertBreak(BreakType.PageBreak);

    // 显示此 REF 字段与其引用的书签之间的列表级别编号。
    field = InsertFieldRef(builder, "MyBookmark", "The bookmark's relative paragraph number is ", "\n");
    field.InsertParagraphNumberInRelativeContext = true;

    Assert.AreEqual(" REF  MyBookmark \\r", field.GetFieldCode());

    // 在文档的末尾，书签将在此处显示为列表项。
    builder.Writeln("List level above bookmark");
    builder.ListFormat.ListLevelNumber++;
    builder.ListFormat.ListLevel.NumberFormat = ">>> \x0002";

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.REF.docx");
}

/// <summary>
/// 让文档构建器插入 REF 字段，用它引用书签，并在其前后添加文本。
/// </summary>
private static FieldRef InsertFieldRef(DocumentBuilder builder, string bookmarkName, string textBefore, string textAfter)
{
    builder.Write(textBefore);
    FieldRef field = (FieldRef)builder.InsertField(FieldType.FieldRef, true);
    field.BookmarkName = bookmarkName;
    builder.Write(textAfter);
    return field;
}
```

### 也可以看看

* class [Field](../field/)
* 命名空间 [Aspose.Words.Fields](../../aspose.words.fields/)
* 部件 [Aspose.Words](../../)
