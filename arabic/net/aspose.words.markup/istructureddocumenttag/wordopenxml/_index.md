---
title: IStructuredDocumentTag.WordOpenXML
linktitle: WordOpenXML
articleTitle: WordOpenXML
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية IStructuredDocumentTag WordOpenXML، وقم بالوصول إلى سلاسل XML بتنسيق FlatOpc لتحسين إدارة المستندات والتكامل.
type: docs
weight: 150
url: /ar/net/aspose.words.markup/istructureddocumenttag/wordopenxml/
---
## IStructuredDocumentTag.WordOpenXML property

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

* interface [IStructuredDocumentTag](../)
* مساحة الاسم [Aspose.Words.Markup](../../../aspose.words.markup/)
* المجسم [Aspose.Words](../../../)
