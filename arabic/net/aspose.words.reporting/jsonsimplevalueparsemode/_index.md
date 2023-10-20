---
title: JsonSimpleValueParseMode Enum
linktitle: JsonSimpleValueParseMode
articleTitle: JsonSimpleValueParseMode
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Reporting.JsonSimpleValueParseMode تعداد. يحدد وضعًا لتحليل قيم JSON البسيطة فارغة ومنطقية ورقمية وعدد صحيح وسلسلة أثناء تحميل JSON. لا يؤثر هذا الوضع على تحليل قيم التاريخ والوقت في C#.
type: docs
weight: 4700
url: /ar/net/aspose.words.reporting/jsonsimplevalueparsemode/
---
## JsonSimpleValueParseMode enumeration

يحدد وضعًا لتحليل قيم JSON البسيطة (فارغة ومنطقية ورقمية وعدد صحيح وسلسلة) أثناء تحميل JSON. لا يؤثر هذا الوضع على تحليل قيم التاريخ والوقت.

```csharp
public enum JsonSimpleValueParseMode
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Loose | `0` | يحدد الوضع الذي يتم فيه تحديد أنواع قيم JSON البسيطة عند تحليل تمثيلات السلسلة الخاصة بها. على سبيل المثال، يتم تحديد نوع 'prop' من مقتطف JSON '{prop: "123" }' كعدد صحيح في هذا الوضع. |
| Strict | `1` | يحدد الوضع الذي يتم فيه تحديد أنواع قيم JSON البسيطة من تدوين JSON نفسه. على سبيل المثال، يتم تحديد نوع 'prop' من مقتطف JSON '{prop: "123" }' كسلسلة في هذا الوضع. |

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Reporting](../../aspose.words.reporting/)
* المجسم [Aspose.Words](../../)
