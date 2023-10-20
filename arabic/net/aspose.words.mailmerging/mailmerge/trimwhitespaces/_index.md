---
title: MailMerge.TrimWhitespaces
linktitle: TrimWhitespaces
articleTitle: TrimWhitespaces
second_title: Aspose.Words لـ .NET
description: MailMerge TrimWhitespaces ملكية. الحصول على قيمة أو تعيينها تشير إلى ما إذا كان سيتم اقتطاع المسافات البيضاء الزائدة والبادئة من قيم دمج المراسلات في C#.
type: docs
weight: 130
url: /ar/net/aspose.words.mailmerging/mailmerge/trimwhitespaces/
---
## MailMerge.TrimWhitespaces property

الحصول على قيمة أو تعيينها تشير إلى ما إذا كان سيتم اقتطاع المسافات البيضاء الزائدة والبادئة من قيم دمج المراسلات.

```csharp
public bool TrimWhitespaces { get; set; }
```

## ملاحظات

القيمة الافتراضية هي`حقيقي` .

## أمثلة

يوضح كيفية اقتطاع المسافات البيضاء من قيم مصدر البيانات أثناء تنفيذ عملية دمج البريد.

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
