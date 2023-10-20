---
title: PageInfo.Colored
linktitle: Colored
articleTitle: Colored
second_title: Aspose.Words لـ .NET
description: PageInfo Colored ملكية. إرجاعحقيقي إذا كانت الصفحة تحتوي على محتوى ملون في C#.
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

// تأكد من أن الصفحة الأولى من المستند غير ملونة.
Assert.IsFalse(doc.GetPageInfo(0).Colored);
```

### أنظر أيضا

* class [PageInfo](../)
* مساحة الاسم [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* المجسم [Aspose.Words](../../../)
