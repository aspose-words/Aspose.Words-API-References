---
title: StructuredDocumentTag.SdtType
linktitle: SdtType
articleTitle: SdtType
second_title: Aspose.Words لـ .NET
description: StructuredDocumentTag SdtType ملكية. يحصل على نوع من هذاعلامة الوثيقة المنظمة  في C#.
type: docs
weight: 250
url: /ar/net/aspose.words.markup/structureddocumenttag/sdttype/
---
## StructuredDocumentTag.SdtType property

يحصل على نوع من هذا**علامة الوثيقة المنظمة** .

```csharp
public SdtType SdtType { get; }
```

## أمثلة

يوضح كيفية الحصول على نوع علامة المستند المنظمة.

```csharp
Document doc = new Document(MyDir + "Structured document tags.docx");

List<StructuredDocumentTag> tags = doc.GetChildNodes(NodeType.StructuredDocumentTag, true)
    .OfType<StructuredDocumentTag>().ToList();

Assert.AreEqual(SdtType.RepeatingSection, tags[0].SdtType);
Assert.AreEqual(SdtType.RepeatingSectionItem, tags[1].SdtType);
Assert.AreEqual(SdtType.RichText, tags[2].SdtType);
```

### أنظر أيضا

* enum [SdtType](../../sdttype/)
* class [StructuredDocumentTag](../)
* مساحة الاسم [Aspose.Words.Markup](../../../aspose.words.markup/)
* المجسم [Aspose.Words](../../../)
