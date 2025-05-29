---
title: StructuredDocumentTag.WordOpenXML
linktitle: WordOpenXML
articleTitle: WordOpenXML
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية StructuredDocumentTag في WordOpenXML. تمتع بالوصول إلى بيانات XML بتنسيق FlatOpc لتكامل سلس للمستندات وتحسين الأداء.
type: docs
weight: 300
url: /ar/net/aspose.words.markup/structureddocumenttag/wordopenxml/
---
## StructuredDocumentTag.WordOpenXML property

يحصل على سلسلة تمثل XML الموجود داخل العقدة فيFlatOpc تنسيق.

```csharp
public string WordOpenXML { get; }
```

## أمثلة

يوضح كيفية الحصول على XML الموجود داخل العقدة بتنسيق FlatOpc.

```csharp
Document doc = new Document(MyDir + "Structured document tags.docx");

List<StructuredDocumentTag> tags = doc.GetChildNodes(NodeType.StructuredDocumentTag, true)
    .OfType<StructuredDocumentTag>().ToList();

Assert.True(tags[0].WordOpenXML
    .Contains(
        "<pkg:part pkg:name=\"/docProps/app.xml\" pkg:contentType=\"application/vnd.openxmlformats-officedocument.extended-properties+xml\">"));
```

### أنظر أيضا

* class [StructuredDocumentTag](../)
* مساحة الاسم [Aspose.Words.Markup](../../../aspose.words.markup/)
* المجسم [Aspose.Words](../../../)
