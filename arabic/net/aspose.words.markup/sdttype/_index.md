---
title: SdtType Enum
linktitle: SdtType
articleTitle: SdtType
second_title: Aspose.Words لـ .NET
description: اكتشف Aspose.Words.Markup.SdtType enum، الذي يحدد أنواع علامات المستندات المنظمة لإدارة المستندات بشكل أفضل وسير العمل بشكل مبسط.
type: docs
weight: 4730
url: /ar/net/aspose.words.markup/sdttype/
---
## SdtType enumeration

يحدد نوع عقدة علامة المستند المنظم (SDT).

```csharp
public enum SdtType
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| None | `0` | لم يتم تعيين أي نوع إلى SDT. |
| Bibliography | `1` | يمثل SDT إدخالًا في المراجع. |
| Citation | `2` | يمثل SDT استشهادًا. |
| Equation | `3` | يمثل SDT معادلة. |
| DropDownList | `4` | يمثل SDT قائمة منسدلة عند عرضها في المستند. |
| ComboBox | `5` | يمثل SDT مربعًا مركبًا عند عرضه في المستند. |
| Date | `6` | يمثل SDT أداة اختيار التاريخ عند عرضه في المستند. |
| BuildingBlockGallery | `7` | يمثل SDT نوع معرض كتلة البناء. |
| DocPartObj | `8` | يمثل SDT نوع جزء المستند. |
| Group | `9` | يمثل SDT مجموعة مقيدة عند عرضها في المستند. |
| Picture | `10` | يمثل SDT صورة عند عرضها في المستند. |
| RichText | `11` | يمثل SDT مربع نص غني عند عرضه في المستند. |
| PlainText | `12` | يمثل SDT مربع نص عادي عند عرضه في المستند. |
| Checkbox | `13` | يمثل SDT مربع اختيار عند عرضه في المستند. |
| RepeatingSection | `14` | يمثل SDT نوع القسم المتكرر عند عرضه في المستند. |
| RepeatingSectionItem | `15` | يمثل SDT عنصر القسم المتكرر. |
| EntityPicker | `16` | يمثل SDT محدد الكيان الذي يسمح للمستخدم بتحديد مثيل لنوع المحتوى الخارجي. |

## أمثلة

يوضح كيفية إنشاء علامة مستند منظمة من نوع الاستشهاد.

```csharp
Document doc = new Document();

StructuredDocumentTag sdt = new StructuredDocumentTag(doc, SdtType.Citation, MarkupLevel.Inline);
Paragraph paragraph = doc.FirstSection.Body.FirstParagraph;
paragraph.AppendChild(sdt);

// إنشاء حقل الاستشهاد.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.MoveToParagraph(0, -1);
builder.InsertField(@"CITATION Ath22 \l 1033 ", "(John Lennon, 2022)");

// نقل الحقل إلى علامة المستند المنظم.
while (sdt.NextSibling != null)
    sdt.AppendChild(sdt.NextSibling);

doc.Save(ArtifactsDir + "StructuredDocumentTag.Citation.docx");
```

يوضح كيفية إنشاء علامة مستند منظمة للمجموعة على مستوى الصف.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();

// قم بإنشاء علامة مستند منظمة للمجموعة على مستوى الصف.
StructuredDocumentTag groupSdt = new StructuredDocumentTag(doc, SdtType.Group, MarkupLevel.Row);
table.AppendChild(groupSdt);
groupSdt.IsShowingPlaceholderText = false;
groupSdt.RemoveAllChildren();

// إنشاء صف فرعي لعلامة المستند المنظم.
Row row = new Row(doc);
groupSdt.AppendChild(row);

Cell cell = new Cell(doc);
row.AppendChild(cell);

builder.EndTable();

// إدراج محتويات الخلية.
cell.EnsureMinimum();
builder.MoveTo(cell.LastParagraph);
builder.Write("Lorem ipsum dolor.");

//إدراج النص بعد الجدول.
builder.MoveTo(table.NextSibling);
builder.Write("Nulla blandit nisi.");

doc.Save(ArtifactsDir + "StructuredDocumentTag.SdtAtRowLevel.docx");
```

يوضح كيفية العمل مع الأنماط لعناصر التحكم في المحتوى.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// فيما يلي طريقتان لتطبيق نمط من المستند على علامة مستند منظمة.
// 1 - تطبيق كائن نمط من مجموعة أنماط المستند:
Style quoteStyle = doc.Styles[StyleIdentifier.Quote];
StructuredDocumentTag sdtPlainText =
    new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline) { Style = quoteStyle };

// 2 - الإشارة إلى النمط في المستند بالاسم:
StructuredDocumentTag sdtRichText =
    new StructuredDocumentTag(doc, SdtType.RichText, MarkupLevel.Inline) { StyleName = "Quote" };

builder.InsertNode(sdtPlainText);
builder.InsertNode(sdtRichText);

Assert.AreEqual(NodeType.StructuredDocumentTag, sdtPlainText.NodeType);

NodeCollection tags = doc.GetChildNodes(NodeType.StructuredDocumentTag, true);

foreach (Node node in tags)
{
    StructuredDocumentTag sdt = (StructuredDocumentTag)node;

    Console.WriteLine(sdt.WordOpenXMLMinimal);

    Assert.AreEqual(StyleIdentifier.Quote, sdt.Style.StyleIdentifier);
    Assert.AreEqual("Quote", sdt.StyleName);
}
```

يوضح كيفية ملء جدول بالبيانات من جزء XML.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

CustomXmlPart xmlPart = doc.CustomXmlParts.Add("Books",
    "<books>" +
        "<book>" +
            "<title>Everyday Italian</title>" +
            "<author>Giada De Laurentiis</author>" +
        "</book>" +
        "<book>" +
            "<title>The C Programming Language</title>" +
            "<author>Brian W. Kernighan, Dennis M. Ritchie</author>" +
        "</book>" +
        "<book>" +
            "<title>Learning XML</title>" +
            "<author>Erik T. Ray</author>" +
        "</book>" +
    "</books>");

// إنشاء رؤوس للبيانات من محتوى XML.
Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Title");
builder.InsertCell();
builder.Write("Author");
builder.EndRow();
builder.EndTable();

// إنشاء جدول يحتوي على قسم متكرر بداخله.
StructuredDocumentTag repeatingSectionSdt =
    new StructuredDocumentTag(doc, SdtType.RepeatingSection, MarkupLevel.Row);
repeatingSectionSdt.XmlMapping.SetMapping(xmlPart, "/books[1]/book", string.Empty);
table.AppendChild(repeatingSectionSdt);

// أضف عنصر قسم متكرر داخل القسم المتكرر وقم بتمييزه كصف.
// سيحتوي هذا الجدول على صف لكل عنصر يمكننا العثور عليه في مستند XML
// باستخدام "/books[1]/book" XPath، والذي يوجد منه ثلاثة.
StructuredDocumentTag repeatingSectionItemSdt =
    new StructuredDocumentTag(doc, SdtType.RepeatingSectionItem, MarkupLevel.Row);
repeatingSectionSdt.AppendChild(repeatingSectionItemSdt);

Row row = new Row(doc);
repeatingSectionItemSdt.AppendChild(row);

// قم بإنشاء خريطة لبيانات XML باستخدام خلايا الجدول التي تم إنشاؤها لعنوان ومؤلف كل كتاب.
StructuredDocumentTag titleSdt =
    new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Cell);
titleSdt.XmlMapping.SetMapping(xmlPart, "/books[1]/book[1]/title[1]", string.Empty);
row.AppendChild(titleSdt);

StructuredDocumentTag authorSdt =
    new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Cell);
authorSdt.XmlMapping.SetMapping(xmlPart, "/books[1]/book[1]/author[1]", string.Empty);
row.AppendChild(authorSdt);

doc.Save(ArtifactsDir + "StructuredDocumentTag.RepeatingSectionItem.docx");
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Markup](../../aspose.words.markup/)
* المجسم [Aspose.Words](../../)
