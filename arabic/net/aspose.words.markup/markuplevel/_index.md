---
title: MarkupLevel Enum
linktitle: MarkupLevel
articleTitle: MarkupLevel
second_title: Aspose.Words لـ .NET
description: اكتشف Aspose.Words.Markup.MarkupLevel enum، الذي يحدد مكان ملاءمة StructuredDocumentTags في شجرة المستندات لديك لتحسين التنظيم والتحكم.
type: docs
weight: 4670
url: /ar/net/aspose.words.markup/markuplevel/
---
## MarkupLevel enumeration

يحدد المستوى في شجرة المستند حيث يوجد ملف معين[`StructuredDocumentTag`](../structureddocumenttag/) يمكن أن يحدث.

```csharp
public enum MarkupLevel
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Unknown | `0` | يحدد القيمة غير المعروفة أو غير الصالحة. |
| Inline | `1` | يظهر العنصر على مستوى السطر (على سبيل المثال بين عمليات تشغيل النص). |
| Block | `2` | يظهر العنصر على مستوى الكتلة (على سبيل المثال بين الجداول والفقرات). |
| Row | `3` | يظهر العنصر بين الصفوف في الجدول. |
| Cell | `4` | يظهر العنصر بين الخلايا في صف واحد. |

## أمثلة

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

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Markup](../../aspose.words.markup/)
* المجسم [Aspose.Words](../../)
