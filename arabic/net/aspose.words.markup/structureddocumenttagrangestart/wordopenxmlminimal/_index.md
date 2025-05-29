---
title: StructuredDocumentTagRangeStart.WordOpenXMLMinimal
linktitle: WordOpenXMLMinimal
articleTitle: WordOpenXMLMinimal
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية StructuredDocumentTagRangeStart في WordOpenXMLMinimal. تمكّن من الوصول إلى سلسلة XML مُبسّطة بتنسيق FlatOpc، مع التركيز على المحتوى فقط.
type: docs
weight: 180
url: /ar/net/aspose.words.markup/structureddocumenttagrangestart/wordopenxmlminimal/
---
## StructuredDocumentTagRangeStart.WordOpenXMLMinimal property

يحصل على سلسلة تمثل XML الموجود داخل العقدة فيFlatOpc format. على عكس[`WordOpenXML`](../wordopenxml/) الخاصية، هذه الطريقة تولد مستندًا مبسطًا يستبعد أي أجزاء غير مرتبطة بالمحتوى.

```csharp
public string WordOpenXMLMinimal { get; }
```

## أمثلة

يوضح كيفية الحصول على الحد الأدنى من XML الموجود داخل العقدة بتنسيق FlatOpc.

```csharp
Document doc = new Document(MyDir + "Multi-section structured document tags.docx");
StructuredDocumentTagRangeStart tag =
    doc.GetChild(NodeType.StructuredDocumentTagRangeStart, 0, true) as StructuredDocumentTagRangeStart;

Assert.True(tag.WordOpenXMLMinimal
    .Contains(
        "<pkg:part pkg:name=\"/docProps/app.xml\" pkg:contentType=\"application/vnd.openxmlformats-officedocument.extended-properties+xml\">"));
Assert.False(tag.WordOpenXMLMinimal.Contains("xmlns:w16cid=\"http://schemas.microsoft.com/office/word/2016/wordml/cid\""));
```

### أنظر أيضا

* class [StructuredDocumentTagRangeStart](../)
* مساحة الاسم [Aspose.Words.Markup](../../../aspose.words.markup/)
* المجسم [Aspose.Words](../../../)
