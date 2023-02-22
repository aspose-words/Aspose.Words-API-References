---
title: Enum MarkupLevel
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Markup.MarkupLevel تعداد. يحدد المستوى في شجرة الوثيقة حيث يوجدStructuredDocumentTag يمكن أن يحدث.
type: docs
weight: 3740
url: /ar/net/aspose.words.markup/markuplevel/
---
## MarkupLevel enumeration

يحدد المستوى في شجرة الوثيقة حيث يوجد[`StructuredDocumentTag`](../structureddocumenttag/) يمكن أن يحدث.

```csharp
public enum MarkupLevel
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Unknown | `0` | يحدد القيمة غير المعروفة أو غير الصالحة . |
| Inline | `1` | يظهر العنصر على المستوى المضمن (على سبيل المثال بين عمليات تشغيل النص) . |
| Block | `2` | يظهر العنصر على مستوى الكتلة (على سبيل المثال بين الجداول والفقرات) . |
| Row | `3` | يظهر العنصر بين صفوف في جدول . |
| Cell | `4` | يظهر العنصر بين الخلايا المتتالية . |

### أمثلة

يوضح كيفية العمل باستخدام أنماط عناصر التحكم في المحتوى.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// فيما يلي طريقتان لتطبيق نمط من المستند إلى علامة مستند منظم.
// 1 - تطبيق كائن نمط من مجموعة أنماط المستند:
Style quoteStyle = doc.Styles[StyleIdentifier.Quote];
StructuredDocumentTag sdtPlainText =
    new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline) { Style = quoteStyle };

// 2 - الإشارة إلى نمط في المستند بالاسم:
StructuredDocumentTag sdtRichText =
    new StructuredDocumentTag(doc, SdtType.RichText, MarkupLevel.Inline) { StyleName = "Quote" };

builder.InsertNode(sdtPlainText);
builder.InsertNode(sdtRichText);

Assert.AreEqual(NodeType.StructuredDocumentTag, sdtPlainText.NodeType);

NodeCollection tags = doc.GetChildNodes(NodeType.StructuredDocumentTag, true);

foreach (Node node in tags)
{
    StructuredDocumentTag sdt = (StructuredDocumentTag)node;

    Assert.AreEqual(StyleIdentifier.Quote, sdt.Style.StyleIdentifier);
    Assert.AreEqual("Quote", sdt.StyleName);
}
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Markup](../../aspose.words.markup/)
* المجسم [Aspose.Words](../../)


