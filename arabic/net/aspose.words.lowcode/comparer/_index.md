---
title: Comparer Class
linktitle: Comparer
articleTitle: Comparer
second_title: Aspose.Words لـ .NET
description: قارن المستندات بسهولة باستخدام فئة Aspose.Words LowCode Comparer. تعرّف على أساليب فعّالة لتحليل المستندات والتعاون بسلاسة.
type: docs
weight: 4210
url: /ar/net/aspose.words.lowcode/comparer/
---
## Comparer class

يوفر طرقًا مخصصة لمقارنة المستندات.

```csharp
public class Comparer : Processor
```

## طُرق

| اسم | وصف |
| --- | --- |
| static [Create](../../aspose.words.lowcode/comparer/create/#create)() | ينشئ مثيلًا جديدًا لمعالج المحول. |
| static [Create](../../aspose.words.lowcode/comparer/create/#create_1)(*[ComparerContext](../comparercontext/)*) | ينشئ مثيلًا جديدًا لمعالج المقارنة. |
| [Execute](../../aspose.words.lowcode/processor/execute/)() | تنفيذ إجراء المعالج. |
| [From](../../aspose.words.lowcode/processor/from/)(*Stream, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | يحدد مستند الإدخال للمعالجة. |
| [From](../../aspose.words.lowcode/processor/from/)(*string, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | يحدد مستند الإدخال للمعالجة. |
| [To](../../aspose.words.lowcode/processor/to/)(*List&lt;Stream&gt;, [SaveFormat](../../aspose.words/saveformat/)*) | يحدد قائمة تدفقات المستندات الناتجة. |
| [To](../../aspose.words.lowcode/processor/to/)(*List&lt;Stream&gt;, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | يحدد قائمة تدفقات المستندات الناتجة. |
| [To](../../aspose.words.lowcode/processor/to/)(*Stream, [SaveFormat](../../aspose.words/saveformat/)*) | يحدد تدفق الإخراج للمعالج. |
| [To](../../aspose.words.lowcode/processor/to/)(*Stream, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | يحدد تدفق الإخراج للمعالج. |
| [To](../../aspose.words.lowcode/processor/to/)(*string, [SaveFormat](../../aspose.words/saveformat/)*) | يحدد ملف الإخراج للمعالج. |
| [To](../../aspose.words.lowcode/processor/to/)(*string, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | يحدد ملف الإخراج للمعالج. |
| static [Compare](../../aspose.words.lowcode/comparer/compare/#compare_4)(*string, string, string, string, DateTime, [CompareOptions](../../aspose.words.comparing/compareoptions/)*) | يقارن بين مستندين باستخدام خيارات إضافية ويحفظ الاختلافات في ملف الإخراج المحدد، ينتج تغييرات كعدد من مراجعات التحرير والتنسيق. |
| static [Compare](../../aspose.words.lowcode/comparer/compare/#compare)(*Stream, Stream, Stream, [SaveFormat](../../aspose.words/saveformat/), string, DateTime, [CompareOptions](../../aspose.words.comparing/compareoptions/)*) | يقارن بين مستندين تم تحميلهما من تدفقات تحتوي على خيارات إضافية ويحفظ الاختلافات في تدفق الإخراج المقدم بتنسيق الحفظ المحدد، ينتج تغييرات كعدد من مراجعات التحرير والتنسيق. |
| static [Compare](../../aspose.words.lowcode/comparer/compare/#compare_1)(*Stream, Stream, Stream, [SaveOptions](../../aspose.words.saving/saveoptions/), string, DateTime, [CompareOptions](../../aspose.words.comparing/compareoptions/)*) | يقارن بين مستندين تم تحميلهما من تدفقات تحتوي على خيارات إضافية ويحفظ الاختلافات في تدفق الإخراج المقدم بتنسيق الحفظ المحدد، ينتج تغييرات كعدد من مراجعات التحرير والتنسيق. |
| static [Compare](../../aspose.words.lowcode/comparer/compare/#compare_2)(*string, string, string, [SaveFormat](../../aspose.words/saveformat/), string, DateTime, [CompareOptions](../../aspose.words.comparing/compareoptions/)*) | يقارن بين مستندين باستخدام خيارات إضافية ويحفظ الاختلافات في ملف الإخراج المحدد بتنسيق الحفظ المقدم، ينتج تغييرات كعدد من مراجعات التحرير والتنسيق. |
| static [Compare](../../aspose.words.lowcode/comparer/compare/#compare_3)(*string, string, string, [SaveOptions](../../aspose.words.saving/saveoptions/), string, DateTime, [CompareOptions](../../aspose.words.comparing/compareoptions/)*) | يقارن بين مستندين باستخدام خيارات إضافية ويحفظ الاختلافات في ملف الإخراج المحدد بتنسيق الحفظ المقدم، ينتج تغييرات كعدد من مراجعات التحرير والتنسيق. |
| static [CompareToImages](../../aspose.words.lowcode/comparer/comparetoimages/#comparetoimages)(*Stream, Stream, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/), string, DateTime, [CompareOptions](../../aspose.words.comparing/compareoptions/)*) | يقارن بين مستندين ويحفظ الاختلافات كصور. يمثل كل عنصر في المصفوفة المرتجعة صفحة واحدة من الناتج المعروض كصورة. |
| static [CompareToImages](../../aspose.words.lowcode/comparer/comparetoimages/#comparetoimages_1)(*string, string, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/), string, DateTime, [CompareOptions](../../aspose.words.comparing/compareoptions/)*) | يقارن بين مستندين ويحفظ الاختلافات كصور. يمثل كل عنصر في المصفوفة المرتجعة صفحة واحدة من الناتج المعروض كصورة. |

### أنظر أيضا

* class [Processor](../processor/)
* مساحة الاسم [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* المجسم [Aspose.Words](../../)
