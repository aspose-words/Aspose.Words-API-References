---
title: BuiltInDocumentProperties.SharedDocument
linktitle: SharedDocument
articleTitle: SharedDocument
second_title: Aspose.Words لـ .NET
description: اكتشف ميزة SharedDocument في BuiltInDocumentProperties التي تكشف ما إذا كان مستندك مشتركًا، مما يعزز التعاون وإمكانية الوصول.
type: docs
weight: 280
url: /ar/net/aspose.words.properties/builtindocumentproperties/shareddocument/
---
## BuiltInDocumentProperties.SharedDocument property

يشير إلى ما إذا كانت الوثيقة وثيقة مشتركة.

```csharp
public bool SharedDocument { get; }
```

## ملاحظات

لا يقوم Aspose.Words بتحديث هذه الخاصية.

## أمثلة

يوضح كيفية الحصول على خصائص ممتدة.

```csharp
Document doc = new Document(MyDir + "Extended properties.docx");
Assert.IsTrue(doc.BuiltInDocumentProperties.ScaleCrop);
Assert.IsTrue(doc.BuiltInDocumentProperties.SharedDocument);
Assert.IsTrue(doc.BuiltInDocumentProperties.HyperlinksChanged);
```

### أنظر أيضا

* class [BuiltInDocumentProperties](../)
* مساحة الاسم [Aspose.Words.Properties](../../../aspose.words.properties/)
* المجسم [Aspose.Words](../../../)
