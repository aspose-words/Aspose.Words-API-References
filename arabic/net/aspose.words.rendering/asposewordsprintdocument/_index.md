---
title: Class AsposeWordsPrintDocument
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Rendering.AsposeWordsPrintDocument فصل. يوفر تطبيقًا افتراضيًا لطباعة ملف aDocument ضمن إطار الطباعة .NET.
type: docs
weight: 4530
url: /ar/net/aspose.words.rendering/asposewordsprintdocument/
---
## AsposeWordsPrintDocument class

يوفر تطبيقًا افتراضيًا لطباعة ملف a[`Document`](../../aspose.words/document/) ضمن إطار الطباعة .NET.

لمعرفة المزيد، قم بزيارة[طباعة مستند برمجياً أو باستخدام مربعات الحوار](https://docs.aspose.com/words/net/print-a-document-programmatically-or-using-dialogs/) مقالة توثيقية.

```csharp
public class AsposeWordsPrintDocument : PrintDocument
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [AsposeWordsPrintDocument](asposewordsprintdocument/)(Document) | تهيئة مثيل جديد لهذه الفئة. |

## الخصائص

| اسم | وصف |
| --- | --- |
| [ColorMode](../../aspose.words.rendering/asposewordsprintdocument/colormode/) { get; set; } | الحصول على أو تعيين كيفية طباعة الصفحات غير الملونة إذا كان الجهاز يدعم الطباعة الملونة. |
| [ColorPagesPrinted](../../aspose.words.rendering/asposewordsprintdocument/colorpagesprinted/) { get; } | يحصل على عدد الصفحات المطبوعة بالألوان (على سبيل المثالColor تم ضبطه على "صحيح". |

## طُرق

| اسم | وصف |
| --- | --- |
| [CachePrinterSettings](../../aspose.words.rendering/asposewordsprintdocument/cacheprintersettings/)() | يقرأ ويخزن بعض حقولPrinterSettings لتقليل وقت الطباعة. |

### ملاحظات

`AsposeWordsPrintDocument` يتجاوزPrintEventArgs) لطباعة نطاق الصفحات المحدد فيهPrinterSettings.

يمكن أن يتكون مستند Word واحد من أقسام متعددة تحدد الصفحات ذات الأحجام المختلفة، واتجاه ، وأدراج الورق.`AsposeWordsPrintDocument` overrides QueryPageSettingsEventArgs) لتحديد حجم الورق واتجاهه ومصدر الورق بشكل صحيح عند طباعة مستند Word.

يقوم Microsoft Word بتخزين قيم خاصة بالطابعة لأدراج الورق في مستند Word، وبالتالي، فإن الطباعة فقط على نفس طراز الطابعة الذي تم تحديده عندما حدد المستخدم أدراج الورق ستؤدي إلى الطباعة من الأدراج الصحيحة. إذا قمت بطباعة مستند على طابعة مختلفة، فمن المرجح أن يتم استخدام درج الورق الافتراضي، وليس الأدراج المحددة في المستند.

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Rendering](../../aspose.words.rendering/)
* المجسم [Aspose.Words](../../)


