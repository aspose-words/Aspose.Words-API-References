---
title: MailMergeOptions.TrimWhitespaces
linktitle: TrimWhitespaces
articleTitle: TrimWhitespaces
second_title: Aspose.Words لـ .NET
description: حسّن دمج البريد باستخدام خاصية TrimWhitespaces. أدر المسافات البادئة واللاحقة بسهولة لمستندات أكثر تنظيمًا واحترافية.
type: docs
weight: 110
url: /ar/net/aspose.words.lowcode/mailmergeoptions/trimwhitespaces/
---
## MailMergeOptions.TrimWhitespaces property

يحصل على قيمة أو يعينها للإشارة إلى ما إذا كانت المسافات البيضاء النهائية والبادئة يتم اقتصاصها من قيم دمج البريد.

```csharp
public bool TrimWhitespaces { get; set; }
```

## ملاحظات

القيمة الافتراضية هي`حقيقي` .

## أمثلة

يوضح كيفية إجراء عملية دمج البريد لسجل واحد.

```csharp
// هناك عدة طرق لإجراء عملية دمج البريد:
string doc = MyDir + "Mail merge.doc";

string[] fieldNames = new string[] { "FirstName", "Location", "SpecialCharsInName()" };
string[] fieldValues = new string[] { "James Bond", "London", "Classified" };

MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMerge.1.docx", fieldNames, fieldValues);
MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMerge.2.docx", SaveFormat.Docx, fieldNames, fieldValues);
MailMergeOptions mailMergeOptions = new MailMergeOptions();
mailMergeOptions.TrimWhitespaces = true;
MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMerge.3.docx", SaveFormat.Docx, fieldNames, fieldValues, mailMergeOptions);
```

### أنظر أيضا

* class [MailMergeOptions](../)
* مساحة الاسم [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* المجسم [Aspose.Words](../../../)
