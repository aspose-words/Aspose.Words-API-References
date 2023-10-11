---
title: StructuredDocumentTag.SdtType
second_title: Aspose.Words لمراجع .NET API
description: StructuredDocumentTag ملكية. يحصل على نوع من هذا علامة الوثيقة المنظمة .
type: docs
weight: 250
url: /ar/net/aspose.words.markup/structureddocumenttag/sdttype/
---
## StructuredDocumentTag.SdtType property

يحصل على نوع من هذا **علامة الوثيقة المنظمة** .

```csharp
public SdtType SdtType { get; }
```

### أمثلة

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
* مساحة الاسم [Aspose.Words.Markup](../../structureddocumenttag/)
* المجسم [Aspose.Words](../../../)


