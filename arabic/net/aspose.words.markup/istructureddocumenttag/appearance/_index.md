---
title: IStructuredDocumentTag.Appearance
linktitle: Appearance
articleTitle: Appearance
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية المظهر IStructuredDocumentTag لتخصيص علامات المستندات المنظمة وتحسينها لتحسين تجربة المستخدم.
type: docs
weight: 10
url: /ar/net/aspose.words.markup/istructureddocumenttag/appearance/
---
## IStructuredDocumentTag.Appearance property

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
* interface [IStructuredDocumentTag](../)
* مساحة الاسم [Aspose.Words.Markup](../../../aspose.words.markup/)
* المجسم [Aspose.Words](../../../)
