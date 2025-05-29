---
title: MailMerge.RestartListsAtEachSection
linktitle: RestartListsAtEachSection
articleTitle: RestartListsAtEachSection
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية MailMerge RestartListsAtEachSection — تُعاد ضبط قائمة التحكم في كل قسم لضمان دمج بريد سلس. حسّن دقة مستنداتك اليوم!
type: docs
weight: 110
url: /ar/net/aspose.words.mailmerging/mailmerge/restartlistsateachsection/
---
## MailMerge.RestartListsAtEachSection property

يحصل على قيمة أو يعينها للإشارة إلى ما إذا كان سيتم إعادة تشغيل القوائم في كل قسم بعد تنفيذ دمج البريد.

```csharp
public bool RestartListsAtEachSection { get; set; }
```

## ملاحظات

القيمة الافتراضية هي`حقيقي` .

## أمثلة

يوضح كيفية التحكم فيما إذا كان سيتم إعادة تشغيل ترقيم القائمة في كل قسم عند تنفيذ دمج البريد أم لا.

```csharp
Document doc = new Document(MyDir + "Section breaks with numbering.docx");

doc.MailMerge.RestartListsAtEachSection = false;
doc.MailMerge.Execute(new string[0], new object[0]);

doc.Save(ArtifactsDir + "MailMerge.RestartListsAtEachSection.pdf");
```

### أنظر أيضا

* class [MailMerge](../)
* مساحة الاسم [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* المجسم [Aspose.Words](../../../)
