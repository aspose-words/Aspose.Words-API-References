---
title: Document.Clone
second_title: Aspose.Words لمراجع .NET API
description: Document طريقة. إجراء نسخة عميقة من ملفDocument .
type: docs
weight: 570
url: /ar/net/aspose.words/document/clone/
---
## Document.Clone method

إجراء نسخة عميقة من ملف[`Document`](../) .

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

// سيؤدي الاستنساخ إلى إنتاج مستند جديد بنفس محتويات المستند الأصلي،
// ولكن مع نسخة فريدة من كل عقد من عقد المستند الأصلي.
Document clone = doc.Clone();

Assert.AreEqual(doc.FirstSection.Body.FirstParagraph.Runs[0].GetText(), 
    clone.FirstSection.Body.FirstParagraph.Runs[0].Text);
Assert.AreNotEqual(doc.FirstSection.Body.FirstParagraph.Runs[0].GetHashCode(),
    clone.FirstSection.Body.FirstParagraph.Runs[0].GetHashCode());
```

### أنظر أيضا

* class [Document](../)
* مساحة الاسم [Aspose.Words](../../document/)
* المجسم [Aspose.Words](../../../)


