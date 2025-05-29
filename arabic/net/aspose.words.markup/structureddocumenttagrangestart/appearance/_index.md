---
title: StructuredDocumentTagRangeStart.Appearance
linktitle: Appearance
articleTitle: Appearance
second_title: Aspose.Words لـ .NET
description: اكتشف كيفية تخصيص مظهر StructuredDocumentTagRangeStart لتحسين تنسيق المستندات وتحسين إمكانية القراءة.
type: docs
weight: 20
url: /ar/net/aspose.words.markup/structureddocumenttagrangestart/appearance/
---
## StructuredDocumentTagRangeStart.Appearance property

يحصل على مظهر علامة المستند المنظم أو يعينه.

```csharp
public SdtAppearance Appearance { get; set; }
```

## أمثلة

يوضح كيفية إظهار العلامة حول المحتوى.

```csharp
Document doc = new Document(MyDir + "Multi-section structured document tags.docx");
StructuredDocumentTagRangeStart tag =
    doc.GetChild(NodeType.StructuredDocumentTagRangeStart, 0, true) as StructuredDocumentTagRangeStart;

if (tag.Appearance == SdtAppearance.Hidden)
    tag.Appearance = SdtAppearance.Tags;
```

### أنظر أيضا

* enum [SdtAppearance](../../sdtappearance/)
* class [StructuredDocumentTagRangeStart](../)
* مساحة الاسم [Aspose.Words.Markup](../../../aspose.words.markup/)
* المجسم [Aspose.Words](../../../)
