---
title: MailMergeOptions.UseNonMergeFields
linktitle: UseNonMergeFields
articleTitle: UseNonMergeFields
second_title: Aspose.Words لـ .NET
description: استخدم إمكانيات دمج البريد المتقدمة مع خاصية UseNonMergeFields. تكامل بسلاسة بين MERGEFIELD وأنواع الحقول الأخرى لتحسين تخصيص المستندات.
type: docs
weight: 130
url: /ar/net/aspose.words.lowcode/mailmergeoptions/usenonmergefields/
---
## MailMergeOptions.UseNonMergeFields property

عندما`حقيقي` , يحدد أنه بالإضافة إلى حقول MERGEFIELD، يتم تنفيذ دمج البريد في بعض الأنواع الأخرى من الحقول و أيضًا في علامات "{{fieldName}}".

```csharp
public bool UseNonMergeFields { get; set; }
```

## ملاحظات

عادةً، يُنفَّذ دمج البريد في حقول MERGEFIELD فقط، ولكن العديد من العملاء بنوا ملف reporting الخاص بهم باستخدام حقول أخرى، وأنشأوا العديد من المستندات بهذه الطريقة. لتبسيط عملية الترحيل (ولأن العديد من العملاء استخدموا هذا النهج بشكل مستقل)، أُضيفت إمكانية دمج البريد في حقول أخرى.

متى`UseNonMergeFields` تم ضبطه على`حقيقي`سيقوم Aspose.Words بتنفيذ عملية دمج البريد في الحقول التالية:

اسم حقل MERGEFIELD

MACROBUTTON NOMACRO اسم الحقل

إذا 0 = 0 "{اسم الحقل}" ""

أيضا، عندما`UseNonMergeFields` تم ضبطه على`حقيقي`سيقوم Aspose.Words بدمج البريد في علامات النص tags "{{fieldName}}". هذه ليست حقولاً، بل مجرد علامات نصية.

### أنظر أيضا

* class [MailMergeOptions](../)
* مساحة الاسم [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* المجسم [Aspose.Words](../../../)
