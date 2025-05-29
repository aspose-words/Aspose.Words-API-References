---
title: IStructuredDocumentTag.SdtType
linktitle: SdtType
articleTitle: SdtType
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية IStructuredDocumentTag SdtType للتعرف بسهولة على نوع علامات المستند المنظم لتحسين إدارة المستندات.
type: docs
weight: 120
url: /ar/net/aspose.words.markup/istructureddocumenttag/sdttype/
---
## IStructuredDocumentTag.SdtType property

يحصل على نوع من هذا**علامة المستند المنظم** .

```csharp
public SdtType SdtType { get; }
```

## أمثلة

يوضح كيفية الحصول على نوع علامة المستند المنظم.

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
* interface [IStructuredDocumentTag](../)
* مساحة الاسم [Aspose.Words.Markup](../../../aspose.words.markup/)
* المجسم [Aspose.Words](../../../)
