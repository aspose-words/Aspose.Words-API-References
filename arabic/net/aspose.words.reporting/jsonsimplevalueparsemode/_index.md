---
title: JsonSimpleValueParseMode
second_title: Aspose.Words لمراجع .NET API
description: يحدد وضعًا لتحليل قيم JSON البسيطة فارغ  منطقي  رقم  عدد صحيح  وسلسلة أثناء تحميل JSON. مثل هذا الوضع لا يؤثر على تحليل قيم التاريخ والوقت.
type: docs
weight: 4440
url: /ar/net/aspose.words.reporting/jsonsimplevalueparsemode/
---
## JsonSimpleValueParseMode enumeration

يحدد وضعًا لتحليل قيم JSON البسيطة (فارغ ، منطقي ، رقم ، عدد صحيح ، وسلسلة) أثناء تحميل JSON. مثل هذا الوضع لا يؤثر على تحليل قيم التاريخ والوقت.

```csharp
public enum JsonSimpleValueParseMode
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Loose | `0` | يحدد الوضع الذي يتم فيه تحديد أنواع قيم JSON البسيطة عند تحليل تمثيلات السلاسل الخاصة بها . على سبيل المثال ، يتم تحديد نوع "الخاصية" من مقتطف JSON "{prop:" 123 "}" كعدد صحيح في هذا الوضع. |
| Strict | `1` | يحدد الوضع الذي يتم فيه تحديد أنواع قيم JSON البسيطة من تدوين JSON نفسه . على سبيل المثال ، يتم تحديد نوع "prop" من مقتطف JSON "{prop:" 123 "}" كسلسلة في هذا الوضع . |

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Reporting](../../aspose.words.reporting)
* المجسم [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
