---
title: Document.Clone
linktitle: Clone
articleTitle: Clone
second_title: Aspose.Words لـ .NET
description: انسخ مستنداتك بسهولة باستخدام طريقة نسخ المستندات لدينا. احصل على نسخ دقيقة وعميقة لتحرير سلس وسير عمل فعال.
type: docs
weight: 590
url: /ar/net/aspose.words/document/clone/
---
## Document.Clone method

يقوم بإجراء نسخة عميقة من[`Document`](../) .

```csharp
public Document Clone()
```

### قيمة الإرجاع

الوثيقة المستنسخة.

## أمثلة

يوضح كيفية استنساخ مستند بشكل عميق.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");

// سيؤدي الاستنساخ إلى إنشاء مستند جديد بنفس محتويات المستند الأصلي،
// ولكن مع نسخة فريدة من كل عقدة من عقد المستند الأصلي.
Document clone = doc.Clone();

Assert.AreEqual(doc.FirstSection.Body.FirstParagraph.Runs[0].GetText(),
    clone.FirstSection.Body.FirstParagraph.Runs[0].Text);
Assert.AreNotEqual(doc.FirstSection.Body.FirstParagraph.Runs[0].GetHashCode(),
    clone.FirstSection.Body.FirstParagraph.Runs[0].GetHashCode());
```

### أنظر أيضا

* class [Document](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
