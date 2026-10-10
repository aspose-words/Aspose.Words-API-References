---
title: "Aspose::Words::Saving::PdfPermissions enum"
linktitle: "PdfPermissions"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Saving::PdfPermissions enum. يحدد العمليات المسموح بها للمستخدم على مستند PDF مشفر في C++."
type: docs
weight: 80000
url: /ar/cpp/aspose.words.saving/pdfpermissions/
---
## PdfPermissions enum


يحدد العمليات المسموح بها للمستخدم على مستند PDF مشفر.

```cpp
enum class PdfPermissions
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| DisallowAll | 0 | يمنع جميع العمليات على مستند PDF. هذا هو القيمة الافتراضية. |
| AllowAll | 65535 | يسمح بجميع العمليات على مستند PDF. |
| ContentCopy | n/a | نسخ أو استخراج النص والرسومات من المستند بطرق أخرى غير تلك التي يتحكم فيها [ContentCopyForAccessibility](./). |
| ContentCopyForAccessibility | n/a | استخراج النص والرسومات (دعمًا لإمكانية الوصول للمستخدمين ذوي الإعاقات أو لأغراض أخرى). |
| ModifyContents | n/a | تعديل محتويات المستند بعمليات أخرى غير تلك التي يتحكم فيها [ModifyAnnotations](./)، [FillIn](./)، و[DocumentAssembly](./). |
| ModifyAnnotations | n/a | إضافة أو تعديل تعليقات نصية، ملء حقول النماذج التفاعلية، وإذا تم تعيين [ModifyContents](./) أيضًا، إنشاء أو تعديل حقول النماذج التفاعلية (بما في ذلك حقول التوقيع). |
| FillIn | n/a | ملء حقول النماذج التفاعلية الموجودة (بما في ذلك حقول التوقيع)، حتى إذا كان [ModifyContents](./) غير مفعّل. |
| DocumentAssembly | n/a | تجميع المستند (إدراج، تدوير أو حذف صفحات وإنشاء عناصر مخطط المستند أو صور مصغرة)، حتى إذا كان [ModifyContents](./) غير مفعّل. |
| Printing | n/a | طباعة المستند (ربما ليس بأعلى جودة، اعتمادًا على ما إذا كان [HighResolutionPrinting](./) مفعّلًا أيضًا). |
| HighResolutionPrinting | n/a | طباعة المستند إلى تمثيل يمكن من خلاله إنشاء نسخة رقمية دقيقة لمحتوى PDF، بناءً على خوارزمية تعتمد على التنفيذ. عندما تكون هذه العلامة غير مفعّلة (و[Printing](./) مفعّل)، يجب حصر الطباعة على تمثيل منخفض المستوى للمظهر، وربما بجودة منخفضة. |

## انظر أيضًا

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
