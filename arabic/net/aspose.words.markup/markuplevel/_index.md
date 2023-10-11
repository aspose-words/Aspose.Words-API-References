---
title: Enum MarkupLevel
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Markup.MarkupLevel تعداد. يحدد المستوى في شجرة الوثيقة حيث يوجد مستوى معينStructuredDocumentTag يمكن أن يحدث.
type: docs
weight: 3980
url: /ar/net/aspose.words.markup/markuplevel/
---
## MarkupLevel enumeration

يحدد المستوى في شجرة الوثيقة حيث يوجد مستوى معين[`StructuredDocumentTag`](../structureddocumenttag/) يمكن أن يحدث.

```csharp
public enum MarkupLevel
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Unknown | `0` | يحدد القيمة غير المعروفة أو غير الصالحة. |
| Inline | `1` | يحدث العنصر على المستوى المضمن (على سبيل المثال، بين مجموعات النص). |
| Block | `2` | يحدث العنصر على مستوى الكتلة (على سبيل المثال بين الجداول والفقرات). |
| Row | `3` | يظهر العنصر بين صفوف الجدول. |
| Cell | `4` | يحدث العنصر بين الخلايا في صف واحد. |

### أمثلة

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

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Markup](../../aspose.words.markup/)
* المجسم [Aspose.Words](../../)


