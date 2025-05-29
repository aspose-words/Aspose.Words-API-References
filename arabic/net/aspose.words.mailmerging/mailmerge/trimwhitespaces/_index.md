---
title: MailMerge.TrimWhitespaces
linktitle: TrimWhitespaces
articleTitle: TrimWhitespaces
second_title: Aspose.Words لـ .NET
description: قم بتحسين عملية دمج البريد لديك باستخدام خاصية TrimWhitespaces، مما يضمن بيانات نظيفة من خلال إزالة المسافات البادئة واللاحقة للحصول على نتائج دقيقة.
type: docs
weight: 130
url: /ar/net/aspose.words.mailmerging/mailmerge/trimwhitespaces/
---
## MailMerge.TrimWhitespaces property

يحصل على قيمة أو يعينها للإشارة إلى ما إذا كانت المسافات البيضاء النهائية والبادئة يتم اقتصاصها من قيم دمج البريد.

```csharp
public bool TrimWhitespaces { get; set; }
```

## ملاحظات

القيمة الافتراضية هي`حقيقي` .

## أمثلة

يوضح كيفية إزالة المسافات البيضاء من قيم مصدر البيانات أثناء تنفيذ دمج البريد.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertField("MERGEFIELD myMergeField", null);

doc.MailMerge.TrimWhitespaces = trimWhitespaces;
doc.MailMerge.Execute(new[] { "myMergeField" }, new object[] { "\t hello world! " });

Assert.AreEqual(trimWhitespaces ? "hello world!\f" : "\t hello world! \f", doc.GetText());
```

### أنظر أيضا

* class [MailMerge](../)
* مساحة الاسم [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* المجسم [Aspose.Words](../../../)
