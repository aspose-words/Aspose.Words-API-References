---
title: StructuredDocumentTag.WordOpenXML
linktitle: WordOpenXML
articleTitle: WordOpenXML
second_title: Aspose.Words لـ .NET
description: StructuredDocumentTag WordOpenXML ملكية. يحصل على سلسلة تمثل XML الموجود داخل العقدة في ملفFlatOpc التنسيق في C#.
type: docs
weight: 300
url: /ar/net/aspose.words.markup/structureddocumenttag/wordopenxml/
---
## StructuredDocumentTag.WordOpenXML property

يحصل على سلسلة تمثل XML الموجود داخل العقدة في ملفFlatOpc التنسيق.

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
