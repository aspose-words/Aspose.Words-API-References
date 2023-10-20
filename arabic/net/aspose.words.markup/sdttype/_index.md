---
title: SdtType Enum
linktitle: SdtType
articleTitle: SdtType
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Markup.SdtType تعداد. يحدد نوع عقدة علامة المستند المنظمة SDT في C#.
type: docs
weight: 4040
url: /ar/net/aspose.words.markup/sdttype/
---
## SdtType enumeration

يحدد نوع عقدة علامة المستند المنظمة (SDT).

```csharp
public enum SdtType
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| None | `0` | لم يتم تخصيص أي نوع لـ SDT. |
| Bibliography | `1` | تمثل المعاملة الخاصة والتفضيلية (SDT) إدخالاً ببليوغرافيًا. |
| Citation | `2` | تمثل المعاملة الخاصة والتفضيلية اقتباسًا. |
| Equation | `3` | تمثل المعاملة الخاصة والتفضيلية معادلة. |
| DropDownList | `4` | تمثل المعاملة SDT قائمة منسدلة عند عرضها في المستند. |
| ComboBox | `5` | يمثل SDT مربع التحرير والسرد عند عرضه في المستند. |
| Date | `6` | يمثل SDT منتقي التاريخ عند عرضه في المستند. |
| BuildingBlockGallery | `7` | يمثل SDT نوع معرض العناصر الأساسية. |
| DocPartObj | `8` | يمثل SDT نوع جزء المستند. |
| Group | `9` | تمثل المعاملة الخاصة والتفضيلية (SDT) تجميعًا مقيدًا عند عرضها في المستند. |
| Picture | `10` | تمثل المعاملة SDT صورة عند عرضها في المستند. |
| RichText | `11` | يمثل SDT مربع نص منسق عند عرضه في المستند. |
| PlainText | `12` | يمثل SDT مربع نص عادي عند عرضه في المستند. |
| Checkbox | `13` | يمثل SDT مربع اختيار عند عرضه في المستند. |
| RepeatingSection | `14` | يمثل SDT نوع القسم المتكرر عند عرضه في المستند. |
| RepeatingSectionItem | `15` | يمثل SDT عنصر القسم المتكرر. |
| EntityPicker | `16` | يمثل SDT منتقي الكيان الذي يسمح للمستخدم بتحديد مثيل لنوع محتوى خارجي. |

## أمثلة

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

// قم بإنشاء صف فرعي لعلامة المستند المنظم.
Row row = new Row(doc);
groupSdt.AppendChild(row);

Cell cell = new Cell(doc);
row.AppendChild(cell);

builder.EndTable();

// أدخل محتويات الخلية.
cell.EnsureMinimum();
builder.MoveTo(cell.LastParagraph);
builder.Write("Lorem ipsum dolor.");

// أدخل النص بعد الجدول.
builder.MoveTo(table.NextSibling);
builder.Write("Nulla blandit nisi.");

doc.Save(ArtifactsDir + "StructuredDocumentTag.SdtAtRowLevel.docx");
```

يوضح كيفية العمل مع أنماط عناصر التحكم في المحتوى.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// فيما يلي طريقتان لتطبيق نمط من المستند على علامة مستند منظمة.
// 1 - تطبيق كائن نمط من مجموعة أنماط المستند:
Style quoteStyle = doc.Styles[StyleIdentifier.Quote];
StructuredDocumentTag sdtPlainText =
    new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline) { Style = quoteStyle };

// 2 - قم بالإشارة إلى النمط الموجود في المستند بالاسم:
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

// أنشئ جدولًا به قسم متكرر بداخله.
StructuredDocumentTag repeatingSectionSdt =
    new StructuredDocumentTag(doc, SdtType.RepeatingSection, MarkupLevel.Row);
repeatingSectionSdt.XmlMapping.SetMapping(xmlPart, "/books[1]/book", string.Empty);
table.AppendChild(repeatingSectionSdt);

// أضف عنصر قسم متكرر داخل القسم المتكرر وقم بوضع علامة عليه كصف.
// سيحتوي هذا الجدول على صف لكل عنصر يمكننا العثور عليه في مستند XML
// باستخدام "/books[1]/book" XPath، والذي يوجد ثلاثة منه.
StructuredDocumentTag repeatingSectionItemSdt =
    new StructuredDocumentTag(doc, SdtType.RepeatingSectionItem, MarkupLevel.Row);
repeatingSectionSdt.AppendChild(repeatingSectionItemSdt);

Row row = new Row(doc);
repeatingSectionItemSdt.AppendChild(row);

// قم بتعيين بيانات XML مع خلايا الجدول التي تم إنشاؤها لعنوان ومؤلف كل كتاب.
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
