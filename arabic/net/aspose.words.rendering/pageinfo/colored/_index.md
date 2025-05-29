---
title: PageInfo.Colored
linktitle: Colored
articleTitle: Colored
second_title: Aspose.Words لـ .NET
description: اكتشف ما إذا كانت صفحتك تتميز بمحتوى ملون نابض بالحياة باستخدام خاصية PageInfo Colored. عزّز تفاعل المستخدمين وحسّن المظهر البصري!
type: docs
weight: 10
url: /ar/net/aspose.words.rendering/pageinfo/colored/
---
## PageInfo.Colored property

إرجاع`حقيقي` إذا كانت الصفحة تحتوي على محتوى ملون.

```csharp
public bool Colored { get; }
```

## أمثلة

يوضح كيفية التحقق مما إذا كانت الصفحة ملونة أم لا.

```csharp
Document doc = new Document(MyDir + "Document.docx");

// تأكد من أن الصفحة الأولى من المستند ليست ملونة.
Assert.IsFalse(doc.GetPageInfo(0).Colored);
```

### أنظر أيضا

* class [PageInfo](../)
* مساحة الاسم [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* المجسم [Aspose.Words](../../../)
