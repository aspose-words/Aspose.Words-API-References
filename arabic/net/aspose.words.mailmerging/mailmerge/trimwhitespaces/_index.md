---
title: MailMerge.TrimWhitespaces
second_title: Aspose.Words لمراجع .NET API
description: MailMerge ملكية. الحصول على أو تعيين قيمة تشير إلى ما إذا كانت المسافات البيضاء الزائدة والبادئة قد تم اقتطاعها من قيم دمج البريد.
type: docs
weight: 130
url: /ar/net/aspose.words.mailmerging/mailmerge/trimwhitespaces/
---
## MailMerge.TrimWhitespaces property

الحصول على أو تعيين قيمة تشير إلى ما إذا كانت المسافات البيضاء الزائدة والبادئة قد تم اقتطاعها من قيم دمج البريد.

```csharp
public bool TrimWhitespaces { get; set; }
```

### ملاحظات

القيمة الافتراضية هي **حقيقي** .

### أمثلة

يوضح كيفية اقتطاع المسافات البيضاء من قيم مصدر البيانات أثناء تنفيذ دمج البريد.

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
* مساحة الاسم [Aspose.Words.MailMerging](../../mailmerge/)
* المجسم [Aspose.Words](../../../)


