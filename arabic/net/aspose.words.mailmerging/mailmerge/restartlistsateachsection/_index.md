---
title: MailMerge.RestartListsAtEachSection
linktitle: RestartListsAtEachSection
articleTitle: RestartListsAtEachSection
second_title: Aspose.Words لـ .NET
description: MailMerge RestartListsAtEachSection ملكية. الحصول على أو تعيين قيمة تشير إلى ما إذا كان سيتم إعادة تشغيل القوائم في كل قسم بعد تنفيذ عملية دمج البريد في C#.
type: docs
weight: 110
url: /ar/net/aspose.words.mailmerging/mailmerge/restartlistsateachsection/
---
## MailMerge.RestartListsAtEachSection property

الحصول على أو تعيين قيمة تشير إلى ما إذا كان سيتم إعادة تشغيل القوائم في كل قسم بعد تنفيذ عملية دمج البريد.

```csharp
public bool RestartListsAtEachSection { get; set; }
```

## ملاحظات

القيمة الافتراضية هي`حقيقي` .

## أمثلة

يوضح كيفية التحكم في إعادة تشغيل ترقيم القائمة أم لا في كل قسم عند إجراء دمج البريد.

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
