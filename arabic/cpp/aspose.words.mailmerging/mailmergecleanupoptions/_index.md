---
title: "تعداد Aspose::Words::MailMerging::MailMergeCleanupOptions"
linktitle: "MailMergeCleanupOptions"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "تعداد Aspose::Words::MailMerging::MailMergeCleanupOptions. يحدد الخيارات التي تحدد ما العناصر التي تُزال أثناء دمج البريد في C++."
type: docs
weight: 11000
url: /ar/cpp/aspose.words.mailmerging/mailmergecleanupoptions/
---
## MailMergeCleanupOptions enum


يحدد الخيارات التي تحدد العناصر التي يتم إزالتها أثناء دمج البريد.

```cpp
enum class MailMergeCleanupOptions
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| None | 0 | يحدد قيمة افتراضية. |
| RemoveEmptyParagraphs | 1 | يحدد ما إذا كان يجب إزالة الفقرات التي تحتوي على حقول دمج بريدية بدون بيانات من المستند. عندما يتم تعيين هذا الخيار، تُزال أيضًا الفقرات التي تحتوي على حقول دمج بداية ونهاية المنطقة والتي تكون فارغة بخلاف ذلك. |
| RemoveUnusedRegions | 2 | يحدد ما إذا كان يجب إزالة مناطق دمج البريد غير المستخدمة من المستند. |
| RemoveUnusedFields | 4 | يحدد ما إذا كان يجب إزالة حقول الدمج غير المستخدمة من المستند. |
| RemoveContainingFields | 8 | يحدد ما إذا كان يجب إزالة الحقول التي تحتوي على حقول دمج (مثل IFs) من المستند إذا تمت إزالة حقول الدمج المتداخلة. |
| RemoveStaticFields | 16 | يحدد ما إذا كان يجب إزالة الحقول الثابتة من المستند. الحقول الثابتة هي الحقول التي تظل نتائجها كما هي عند أي تغيير في المستند. [Fields](../../aspose.words.fields/)، التي لا تخزن نتائجها في المستند وتُحسب في الوقت الفعلي (مثل [FieldListNum](../../aspose.words.fields/fieldtype/)، [FieldSymbol](../../aspose.words.fields/fieldtype/)، إلخ) لا تُعتبر ثابتة. |
| RemoveEmptyTableRows | 32 | يحدد ما إذا كان يجب إزالة الصفوف الفارغة التي تحتوي على مناطق دمج البريد من المستند. |
| RemoveEmptyTables | 64 | يحدد ما إذا كان يجب إزالة الجداول التي تحتوي على مناطق دمج البريد والتي تم إزالتها باستخدام إما خيار [RemoveUnusedRegions](./) أو خيار [RemoveEmptyTableRows](./) من المستند. |

## انظر أيضًا

* Namespace [Aspose::Words::MailMerging](../)
* Library [Aspose.Words for C++](../../)
