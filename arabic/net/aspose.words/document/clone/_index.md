---
title: Clone
second_title: Aspose.Words لمراجع .NET API
description: يقوم بإجراء نسخة عميقة من ملفDocumentaspose.words/document .
type: docs
weight: 530
url: /ar/net/aspose.words/document/clone/
---
## Document.Clone method

يقوم بإجراء نسخة عميقة من ملف[`Document`](../../document) .

```csharp
public Document Clone()
```

### قيمة الإرجاع

الوثيقة المستنسخة.

### أمثلة

يوضح كيفية استنساخ مستند بعمق.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");

// سينتج الاستنساخ مستندًا جديدًا بنفس محتويات المستند الأصلي ،
// ولكن بنسخة فريدة من كل عقد من عقد المستند الأصلي.
Document clone = doc.Clone();

Assert.AreEqual(doc.FirstSection.Body.FirstParagraph.Runs[0].GetText(), 
    clone.FirstSection.Body.FirstParagraph.Runs[0].Text);
Assert.AreNotEqual(doc.FirstSection.Body.FirstParagraph.Runs[0].GetHashCode(),
    clone.FirstSection.Body.FirstParagraph.Runs[0].GetHashCode());
```

### أنظر أيضا

* class [Document](../../document)
* مساحة الاسم [Aspose.Words](../../document)
* المجسم [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
