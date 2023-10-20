---
title: StructuredDocumentTag.WordOpenXMLMinimal
linktitle: WordOpenXMLMinimal
articleTitle: WordOpenXMLMinimal
second_title: Aspose.Words لـ .NET
description: StructuredDocumentTag WordOpenXMLMinimal ملكية. يحصل على سلسلة تمثل XML الموجود داخل العقدة في ملفFlatOpc تنسيق. خلافا لWordOpenXMLالخاصية تقوم هذه الطريقة بإنشاء مستند مبسط يستبعد أي أجزاء غير متعلقة بالمحتوى في C#.
type: docs
weight: 310
url: /ar/net/aspose.words.markup/structureddocumenttag/wordopenxmlminimal/
---
## StructuredDocumentTag.WordOpenXMLMinimal property

يحصل على سلسلة تمثل XML الموجود داخل العقدة في ملفFlatOpc تنسيق. خلافا ل[`WordOpenXML`](../wordopenxml/)الخاصية، تقوم هذه الطريقة بإنشاء مستند مبسط يستبعد أي أجزاء غير متعلقة بالمحتوى.

```csharp
public string WordOpenXMLMinimal { get; }
```

## أمثلة

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

* class [StructuredDocumentTag](../)
* مساحة الاسم [Aspose.Words.Markup](../../../aspose.words.markup/)
* المجسم [Aspose.Words](../../../)
