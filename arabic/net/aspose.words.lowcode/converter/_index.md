---
title: Converter Class
linktitle: Converter
articleTitle: Converter
second_title: Aspose.Words لـ .NET
description: حوّل أنواعًا مختلفة من المستندات بسهولة مع Aspose.Words.LowCode.Converter. بسّط سير عملك بسطر واحد فقط من التعليمات البرمجية لضمان تكامل سلس.
type: docs
weight: 4230
url: /ar/net/aspose.words.lowcode/converter/
---
## Converter class

يمثل مجموعة من الأساليب المخصصة لتحويل مجموعة متنوعة من أنواع المستندات المختلفة باستخدام سطر واحد من التعليمات البرمجية.

```csharp
public class Converter : Processor
```

## طُرق

| اسم | وصف |
| --- | --- |
| static [Create](../../aspose.words.lowcode/converter/create/#create)() | ينشئ مثيلًا جديدًا لمعالج المحول. |
| static [Create](../../aspose.words.lowcode/converter/create/#create_1)(*[ConverterContext](../convertercontext/)*) | ينشئ مثيلًا جديدًا لمعالج المحول. |
| [Execute](../../aspose.words.lowcode/processor/execute/)() | تنفيذ إجراء المعالج. |
| [From](../../aspose.words.lowcode/processor/from/)(*Stream, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | يحدد مستند الإدخال للمعالجة. |
| [From](../../aspose.words.lowcode/processor/from/)(*string, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | يحدد مستند الإدخال للمعالجة. |
| [To](../../aspose.words.lowcode/processor/to/)(*List&lt;Stream&gt;, [SaveFormat](../../aspose.words/saveformat/)*) | يحدد قائمة تدفقات المستندات الناتجة. |
| [To](../../aspose.words.lowcode/processor/to/)(*List&lt;Stream&gt;, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | يحدد قائمة تدفقات المستندات الناتجة. |
| [To](../../aspose.words.lowcode/processor/to/)(*Stream, [SaveFormat](../../aspose.words/saveformat/)*) | يحدد تدفق الإخراج للمعالج. |
| [To](../../aspose.words.lowcode/processor/to/)(*Stream, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | يحدد تدفق الإخراج للمعالج. |
| [To](../../aspose.words.lowcode/processor/to/)(*string, [SaveFormat](../../aspose.words/saveformat/)*) | يحدد ملف الإخراج للمعالج. |
| [To](../../aspose.words.lowcode/processor/to/)(*string, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | يحدد ملف الإخراج للمعالج. |
| static [Convert](../../aspose.words.lowcode/converter/convert/#convert_4)(*string, string*) | يحول مستند الإدخال المعطى إلى مستند الإخراج باستخدام أسماء ملفات الإدخال والإخراج المحددة وملحقاتها. |
| static [Convert](../../aspose.words.lowcode/converter/convert/#convert_1)(*Stream, Stream, [SaveFormat](../../aspose.words/saveformat/)*) | يحول مستند الإدخال المعطى إلى مستند إخراج واحد باستخدام تدفقات الإدخال والإخراج المحددة. |
| static [Convert](../../aspose.words.lowcode/converter/convert/#convert_2)(*Stream, Stream, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | يحول مستند الإدخال المعطى إلى مستند إخراج واحد باستخدام تدفقات الإدخال والإخراج المحددة. |
| static [Convert](../../aspose.words.lowcode/converter/convert/#convert_5)(*string, string, [SaveFormat](../../aspose.words/saveformat/)*) | يحول مستند الإدخال المعطى إلى مستند الإخراج باستخدام أسماء ملفات الإدخال والإخراج المحددة وتنسيق المستند النهائي. |
| static [Convert](../../aspose.words.lowcode/converter/convert/#convert_6)(*string, string, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | يحول مستند الإدخال المعطى إلى مستند الإخراج باستخدام أسماء ملفات الإدخال والإخراج المحددة وخيارات الحفظ. |
| static [Convert](../../aspose.words.lowcode/converter/convert/#convert)(*Stream, [LoadOptions](../../aspose.words.loading/loadoptions/), Stream, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | يحول مستند الإدخال المعطى إلى مستند إخراج واحد باستخدام تدفقات الإدخال والإخراج المحددة. |
| static [Convert](../../aspose.words.lowcode/converter/convert/#convert_3)(*string, [LoadOptions](../../aspose.words.loading/loadoptions/), string, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | يحول مستند الإدخال المعطى إلى مستند الإخراج باستخدام أسماء ملفات الإدخال والإخراج المحددة وخيارات التحميل/الحفظ الخاصة به. |
| static [ConvertToImages](../../aspose.words.lowcode/converter/converttoimages/#converttoimages_1)(*[Document](../../aspose.words/document/), [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/)*) | يحول صفحات المستند المحدد إلى صور باستخدام خيارات الحفظ المحددة ويعيد مجموعة من التدفقات التي تحتوي على الصور. |
| static [ConvertToImages](../../aspose.words.lowcode/converter/converttoimages/#converttoimages)(*[Document](../../aspose.words/document/), [SaveFormat](../../aspose.words/saveformat/)*) | يحول صفحات المستند المحدد إلى صور بالتنسيق المحدد ويعيد مجموعة من التدفقات التي تحتوي على الصور. |
| static [ConvertToImages](../../aspose.words.lowcode/converter/converttoimages/#converttoimages_4)(*Stream, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/)*) | يحول صفحات مجرى الإدخال المحدد إلى صور باستخدام خيارات الحفظ المحددة ويعيد مجموعة من المجاري التي تحتوي على الصور. |
| static [ConvertToImages](../../aspose.words.lowcode/converter/converttoimages/#converttoimages_3)(*Stream, [SaveFormat](../../aspose.words/saveformat/)*) | يحول صفحات مجرى الإدخال المحدد إلى صور بالتنسيق المحدد ويعيد مجموعة من المجاري التي تحتوي على الصور. |
| static [ConvertToImages](../../aspose.words.lowcode/converter/converttoimages/#converttoimages_6)(*string, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/)*) | يحول صفحات ملف الإدخال المحدد إلى صور باستخدام خيارات الحفظ المحددة ويعيد مجموعة من التدفقات التي تحتوي على الصور. |
| static [ConvertToImages](../../aspose.words.lowcode/converter/converttoimages/#converttoimages_5)(*string, [SaveFormat](../../aspose.words/saveformat/)*) | يحول صفحات ملف الإدخال المحدد إلى صور بالتنسيق المحدد ويعيد مجموعة من التدفقات التي تحتوي على الصور. |
| static [ConvertToImages](../../aspose.words.lowcode/converter/converttoimages/#converttoimages_2)(*Stream, [LoadOptions](../../aspose.words.loading/loadoptions/), [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/)*) | يحول صفحات مجرى الإدخال المحدد إلى صور باستخدام خيارات التحميل والحفظ المقدمة، ويعيد مجموعة من المجاري التي تحتوي على الصور. |

## ملاحظات

يتم استخدام ملفات الإدخال والإخراج أو التدفقات المحددة، إلى جانب تنسيق الحفظ المطلوب، لتحويل مستند الإدخال المحدد بتنسيق واحد إلى مستند الإخراج للتنسيق المحدد الآخر.

تدعم وظيفة التحويل أكثر من 35 تنسيق ملف مختلفًا.

ال[`ConvertToImages`](./converttoimages/)مجموعة من الطرق مصممة لتحويل المستندات إلى صور، مع تحويل كل صفحة إلى ملف صورة منفصل. كما تحوّل هذه الطرق مستندات PDF مباشرةً إلى تنسيقات صفحات ثابتة، دون تحميلها في نموذج المستند، مما يُحسّن الأداء والدقة.

مع[`PageSet`](../../aspose.words.saving/imagesaveoptions/pageset/)يمكنك تحديد مجموعة معينة من الصفحات لتحويلها إلى صور.

### أنظر أيضا

* class [Processor](../processor/)
* مساحة الاسم [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* المجسم [Aspose.Words](../../)
