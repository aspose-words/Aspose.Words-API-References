---
title: FontFeature Enum
linktitle: FontFeature
articleTitle: FontFeature
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Shaping.FontFeature تعداد. توفر الميزات معلومات حول كيفية استخدام الحروف الرسومية في الخط لعرض البرنامج النصي. https//docs.microsoft.com/enus/typography/opentype/spec/featuretags في C#.
type: docs
weight: 6030
url: /ar/net/aspose.words.shaping/fontfeature/
---
## FontFeature enumeration

توفر الميزات معلومات حول كيفية استخدام الحروف الرسومية في الخط لعرض البرنامج النصي. https://docs.microsoft.com/en-us/typography/opentype/spec/featuretags

```csharp
public enum FontFeature
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| GlyphCompositionDecomposition | `1667460464` | لتقليل عدد بدائل الحروف الرسومية، من المستحسن في بعض الأحيان تحليل الحرف الرسومي الافتراضي للحرف إلى حرفين رسوميين أو أكثر. بالإضافة إلى ذلك، قد يكون من الأفضل إنشاء صور رمزية افتراضية لحرفين أو أكثر في حرف رسومي واحد للحصول على حرف رسومي أفضل المعالجة. تسمح هذه الميزة بالتركيب/التحليل. https://docs.microsoft.com/en-us/typography/opentype/spec/features_ae#ccmp علامة OpenType المكافئة: 'ccmp' |
| StandardLigatures | `1818847073` | يستبدل تسلسل الحروف الرسومية بحرف رسومي واحد مفضل للأغراض المطبعية. تغطي هذه الميزة الحروف المركبة التي يرى المصمم/الشركة المصنعة أنه يجب استخدامها في الظروف العادية. علامة OpenType المكافئة: 'liga' https://docs .microsoft.com/en-us/typography/opentype/spec/features_ko#liga |
| RequiredLigatures | `1919707495` | يستبدل تسلسل الحروف الرسومية بحرف رسومي واحد مفضل لأغراض الطباعة. تغطي هذه الميزة تلك الأحرف المركبة، والتي يحددها البرنامج النصي على أنها مطلوبة للاستخدام في الظروف العادية. هذه الميزة مهمة لبعض البرامج النصية لضمان تكوين الحروف الرسومية الصحيحة . https://docs.microsoft.com/en-us/typography/opentype/spec/features_pt#rlig علامة OpenType المكافئة: 'rlig' |
| ContextualLigatures | `1668049255` | يستبدل تسلسل الحروف الرسومية بحرف رسومي واحد مفضل لأغراض الطباعة. على عكس ميزات الحروف المركبة الأخرى، يحدد 'clig' السياق الذي يوصى فيه بالأحرف المركبة. هذه الإمكانية مهمة في بعض تصميمات البرامج النصية والأحرف المركبة المائلة. https://docs.microsoft.com/en-us/typography/opentype/spec/features_ae#clig علامة OpenType المكافئة: 'clig' |
| DiscretionaryLigatures | `1684826471` | يستبدل تسلسل الحروف الرسومية بحرف رسومي واحد مفضل لأغراض الطباعة. تغطي هذه الميزة تلك الأحرف المركبة التي يمكن استخدامها لتأثير خاص، حسب تفضيلات المستخدم. https://docs.microsoft.com/en-us /typography/opentype/spec/features_ae#dlig علامة OpenType المكافئة: 'dlig' |
| HistoricalLigatures | `1751935335` | كانت بعض الحروف المركبة شائعة الاستخدام في الماضي، ولكنها تبدو وكأنها عفا عليها الزمن اليوم. تتضمن بعض الخطوط النماذج التاريخية كبدائل، بحيث يمكن استخدامها لتأثير "الفترة". تستبدل هذه الميزة النماذج الافتراضية (الحالية) بالملحق البدائل التاريخية. https://docs.microsoft.com/en-us/typography/opentype/spec/features_fj#hlig علامة OpenType المكافئة: 'hlig' |
| ProportionalFigures | `1886287213` | يستبدل الحروف الرسومية الشكلية التي تم تعيينها على عروض موحدة (جدولية) بالحروف الرسومية المقابلة التي تم تعيينها على عروض الحروف الرسومية (المتناسبة). https://docs.microsoft.com/en-us/typography/opentype/spec/features_pt#tag-pnum علامة OpenType المكافئة: 'pnum' |
| TabularFigures | `1953396077` | يستبدل الحروف الرسومية الشكلية التي تم تعيينها على عروض متناسبة مع الحروف الرسومية المقابلة التي تم تعيينها على عروض موحدة (جدولية). ستكون العروض الجدولية هي الافتراضية بشكل عام، ولكن لا يمكن افتراض ذلك بأمان. بالطبع لن تكون هذه الميزة موجودة في التصميمات أحادية المسافة. https //docs.microsoft.com/en-us/typography/opentype/spec/features_pt#tag-tnum علامة OpenType المكافئة: 'tnum' |
| LiningFigures | `1819178349` | تعمل هذه الميزة على تغيير الأشكال غير المبطنة المحددة إلى أشكال مبطنة. https://docs.microsoft.com/en-us/typography/opentype/spec/features_ko#lnum علامة OpenType المكافئة: 'lnum' |
| OldstyleFigures | `1869509997` | تعمل هذه الميزة على تغيير الأشكال المحددة من النمط الافتراضي أو نمط البطانة إلى نموذج النمط القديم. https://docs.microsoft.com/en-us/typography/opentype/spec/features_ko#onum علامة OpenType المكافئة: 'onum' |
| VerticalAlternates | `1986359924` | تحويل الحروف الرسومية الافتراضية إلى صور رمزية مناسبة للعرض التقديمي المستقيم في وضع الكتابة العمودي. https://docs.microsoft.com/en-us/typography/opentype/spec/features_uz#tag-vert علامة OpenType المكافئة: 'vert' |
| VerticalAlternatesAndRotation | `1987212338` | يستبدل بعض الحروف الرسومية ذات العرض الثابت (نصف أو ثالث أو ربع) أو ذات العرض المتناسب (معظمها لاتينية أو كاتاكانا) بأشكال مناسبة للكتابة العمودية (أي تدويرها 90 درجة في اتجاه عقارب الساعة). https:// docs.microsoft.com/en-us/typography/opentype/spec/features_uz#tag-vrt2 علامة OpenType المكافئة: 'vrt2' |
| StylisticSet01 | `1936928817` | المجموعة الأسلوبية 1 بالإضافة إلى، أو بدلاً من، البدائل الأسلوبية للحروف الرسومية الفردية (راجع ميزة "الملح")، قد تحتوي بعض الخطوط على مجموعات من الصور الرمزية المتغيرة الأسلوبية المقابلة لأجزاء من مجموعة الأحرف، على سبيل المثال، المتغيرات المتعددة للأحرف الصغيرة في خط لاتيني. https://docs.microsoft.com/en-us/typography/opentype/spec/features_pt#tag-ss01---ss20 علامة OpenType المكافئة: 'ss01' |
| StylisticSet02 | `1936928818` | المجموعة الأسلوبية 2 علامة OpenType المكافئة: 'ss02' |
| StylisticSet03 | `1936928819` | المجموعة الأسلوبية 3 علامة OpenType المكافئة: 'ss03' |
| StylisticSet04 | `1936928820` | المجموعة الأسلوبية 4 علامة OpenType المكافئة: 'ss04' |
| StylisticSet05 | `1936928821` | المجموعة الأسلوبية 5 علامة OpenType المكافئة: 'ss05' |
| StylisticSet06 | `1936928822` | المجموعة الأسلوبية 6 علامة OpenType المكافئة: 'ss06' |
| StylisticSet07 | `1936928823` | المجموعة الأسلوبية 7 علامة OpenType المكافئة: 'ss07' |
| StylisticSet08 | `1936928824` | المجموعة الأسلوبية 8 علامة OpenType المكافئة: 'ss08' |
| StylisticSet09 | `1936928825` | المجموعة الأسلوبية 9 علامة OpenType المكافئة: 'ss09' |
| StylisticSet10 | `1936929072` | المجموعة الأسلوبية 10 علامة OpenType المكافئة: 'ss10' |
| StylisticSet11 | `1936929073` | المجموعة الأسلوبية 11 علامة OpenType المكافئة: 'ss11' |
| StylisticSet12 | `1936929074` | المجموعة الأسلوبية 12 علامة OpenType المكافئة: 'ss12' |
| StylisticSet13 | `1936929075` | المجموعة الأسلوبية 13 علامة OpenType المكافئة: 'ss13' |
| StylisticSet14 | `1936929076` | المجموعة الأسلوبية 14 علامة OpenType المكافئة: 'ss14' |
| StylisticSet15 | `1936929077` | المجموعة الأسلوبية 15 علامة OpenType المكافئة: 'ss15' |
| StylisticSet16 | `1936929078` | المجموعة الأسلوبية 16 علامة OpenType المكافئة: 'ss16' |
| StylisticSet17 | `1936929079` | المجموعة الأسلوبية 17 علامة OpenType المكافئة: 'ss17' |
| StylisticSet18 | `1936929080` | المجموعة الأسلوبية 18 علامة OpenType المكافئة: 'ss18' |
| StylisticSet19 | `1936929081` | المجموعة الأسلوبية 19 علامة OpenType المكافئة: 'ss19' |
| StylisticSet20 | `1936929328` | المجموعة الأسلوبية 20 علامة OpenType المكافئة: 'ss20' |
| Kerning | `1801810542` | يضبط مقدار المسافة بين الحروف الرسومية، بشكل عام لتوفير تباعد متسق بصريًا بين الحروف الرسومية. على الرغم من أن المحرف المصمم جيدًا يحتوي على تباعد متسق بين الحروف الرسومية بشكل عام، إلا أن بعض مجموعات الحروف الرسومية تتطلب تعديلًا لتحسين الوضوح. إلى جانب الضبط القياسي في الاتجاه الأفقي، يمكن لهذه الميزة توفير بيانات تقنين تعتمد على الحجم عبر جداول الأجهزة، تقنين الأحرف "المتقاطع" في اتجاه النص Y، وضبط موضع الحرف الرسومي بشكل مستقل عن التعديل المتقدم. لاحظ أن هذه الميزة قد تنطبق على تشغيل أكثر من اثنين الحروف الرسومية، ولن يتم استخدامها في الخطوط أحادية المسافة. لاحظ أيضًا أن هذه الميزة لا تنطبق على مجموعة النص عموديًا. https://docs.microsoft.com/en-us/typography/opentype/spec/features_ko#kern Equivalent علامة OpenType: 'kern' |

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Shaping](../../aspose.words.shaping/)
* المجسم [Aspose.Words](../../)
