---
title: PdfCompliance
second_title: Aspose.Words لمراجع .NET API
description: يحدد مستوى التوافق مع معايير PDF .
type: docs
weight: 5130
url: /ar/net/aspose.words.saving/pdfcompliance/
---
## PdfCompliance enumeration

يحدد مستوى التوافق مع معايير PDF .

```csharp
public enum PdfCompliance
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Pdf17 | `0` | سيتوافق ملف الإخراج مع معيار PDF 1.7 (ISO 32000-1) . |
| Pdf20 | `1` | سيتوافق ملف الإخراج مع معيار PDF 2.0 (ISO 32000-2) . |
| PdfA1a | `2` | سيتوافق ملف الإخراج مع معيار PDF / A-1a (ISO 19005-1) . يتضمن هذا المستوى جميع متطلبات PDF / A-1b ويتطلب بالإضافة إلى ذلك تضمين بنية المستند (المعروف أيضًا باسم "الموسومة" ) ، _ x000d_ بهدف ضمان إمكانية البحث في محتوى المستند وإعادة استخدامه. |
| PdfA1b | `3` | سيتوافق ملف الإخراج مع معيار PDF / A-1b (ISO 19005-1) . يهدف PDF / A-1b إلى ضمان إعادة إنتاج موثوق للمظهر المرئي للوثيقة. |
| PdfA2a | `4` | سيتوافق ملف الإخراج مع معيار PDF / A-2a (ISO 19005-2) . يتضمن هذا المستوى جميع متطلبات PDF / A-2u ويتطلب بالإضافة إلى ذلك تضمين بنية المستند (المعروفة أيضًا باسم "الموسومة" ) ، _ x000d_ بهدف ضمان إمكانية البحث في محتوى المستند وإعادة استخدامه. |
| PdfA2u | `5` | سيتوافق ملف الإخراج مع معيار PDF / A-2u (ISO 19005-2). _ x000d_ يهدف PDF / A-2u إلى الحفاظ على المظهر المرئي الثابت للوثيقة بمرور الوقت ، بغض النظر عن الأدوات_ x000d_ والأنظمة المستخدمة للإنشاء والتخزين أو تقديم الملفات. بالإضافة إلى ذلك ، يمكن استخراج أي نص موجود في document بشكل موثوق به كسلسلة من نقاط تشفير Unicode. |
| PdfA4 | `6` | سيلتزم ملف الإخراج بمعيار PDF / A-4 (ISO 19005-4: 2020) . يهدف PDF / A-4 إلى الحفاظ على المظهر المرئي الثابت للوثيقة بمرور الوقت ، بغض النظر عن الأدوات_ x000d_ والأنظمة المستخدمة للإنشاء أو تخزين أو عرض الملفات. بالإضافة إلى ذلك ، يمكن استخراج أي نص موجود في document بشكل موثوق به كسلسلة من نقاط تشفير Unicode. |
| PdfUa1 | `7` | سيتوافق ملف الإخراج مع معيار PDF / UA-1 (ISO 14289-1) . الغرض الأساسي من PDF / UA هو تحديد كيفية تمثيل المستندات الإلكترونية بتنسيق PDF بطريقة a التي تسمح للملف بأن يكون يمكن الوصول إليه. |

### أمثلة

يوضح كيفية تعيين مستوى التوافق مع معايير PDF لمستندات PDF المحفوظة.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// قم بإنشاء كائن "PdfSaveOptions" يمكننا تمريره إلى طريقة "Save" الخاصة بالمستند
// لتعديل كيفية تحويل هذه الطريقة المستند إلى PDF.
// لاحظ أن بعض خيارات PdfSaveOptions محظورة عند الحفظ في أحد المعايير ويتم إصلاحها تلقائيًا.
// استخدم IWarningCallback لمعرفة الخيارات التي يتم إصلاحها تلقائيًا.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// اضبط خاصية "Compliance" على "PdfCompliance.PdfA1b" للامتثال لمعيار "PDF / A-1b" ،
// الذي يهدف إلى الحفاظ على المظهر المرئي للوثيقة مثل Aspose ، وتحول الكلمات إلى PDF.
// عيِّن خاصية "الامتثال" على "PdfCompliance.Pdf17" لتتوافق مع المعيار "1.7".
// قم بتعيين خاصية "الامتثال" على "PdfCompliance.PdfA1a" للامتثال لمعيار "PDF / A-1a" ،
// الذي يتوافق مع "PDF / A-1b" بالإضافة إلى الحفاظ على بنية المستند الأصلي.
// قم بتعيين خاصية "الامتثال" على "PdfCompliance.PdfUa1" للامتثال لمعيار "PDF / UA-1" (ISO 14289-1) ،
// الذي يهدف إلى تحديد تمثيل المستندات الإلكترونية في PDF والتي تسمح بالوصول إلى الملف.
// يساعد هذا في جعل المستندات قابلة للبحث ولكن قد يزيد بشكل كبير من حجم المستندات الكبيرة بالفعل.
saveOptions.Compliance = pdfCompliance;

doc.Save(ArtifactsDir + "PdfSaveOptions.Compliance.pdf", saveOptions);
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Saving](../../aspose.words.saving)
* المجسم [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->