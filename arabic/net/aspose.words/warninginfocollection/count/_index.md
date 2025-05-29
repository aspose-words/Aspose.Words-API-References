---
title: WarningInfoCollection.Count
linktitle: Count
articleTitle: Count
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية Count الخاصة بـ WarningInfoCollection للوصول بسهولة إلى العدد الإجمالي للعناصر في مجموعتك لإدارة البيانات بكفاءة.
type: docs
weight: 20
url: /ar/net/aspose.words/warninginfocollection/count/
---
## WarningInfoCollection.Count property

يحصل على عدد العناصر الموجودة في المجموعة.

```csharp
public int Count { get; }
```

## أمثلة

يوضح كيفية الحصول على تحذيرات حول التنسيقات غير المدعومة.

```csharp
WarningInfoCollection warnings = new WarningInfoCollection();
Document doc = new Document(MyDir + "FB2 document.fb2", new LoadOptions { WarningCallback = warnings });

Assert.AreEqual("The original file load format is FB2, which is not supported by Aspose.Words. The file is loaded as an XML document.", warnings[0].Description);
Assert.AreEqual(1, warnings.Count);
```

### أنظر أيضا

* class [WarningInfoCollection](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
