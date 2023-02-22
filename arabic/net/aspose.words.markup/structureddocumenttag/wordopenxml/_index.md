---
title: StructuredDocumentTag.WordOpenXML
second_title: Aspose.Words لمراجع .NET API
description: StructuredDocumentTag ملكية. يحصل على سلسلة تمثل XML الموجود داخل العقدة في ملفFlatOpc التنسيق .
type: docs
weight: 300
url: /ar/net/aspose.words.markup/structureddocumenttag/wordopenxml/
---
## StructuredDocumentTag.WordOpenXML property

يحصل على سلسلة تمثل XML الموجود داخل العقدة في ملفFlatOpc التنسيق .

```csharp
public string WordOpenXML { get; }
```

### أمثلة

يوضح كيفية الحصول على XML داخل العقدة بتنسيق FlatOpc.

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
* مساحة الاسم [Aspose.Words.Markup](../../structureddocumenttag/)
* المجسم [Aspose.Words](../../../)


