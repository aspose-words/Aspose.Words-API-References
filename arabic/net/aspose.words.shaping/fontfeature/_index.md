---
title: FontFeature Enum
linktitle: FontFeature
articleTitle: FontFeature
second_title: Aspose.Words لـ .NET
description: اكتشف مجموعة Aspose.Words.Shaping.FontFeature، التي تُفصّل استخدام الحروف في الخطوط لعرض النصوص. حسّن معرفتك بالطباعة اليوم!
type: docs
weight: 6860
url: /ar/net/aspose.words.shaping/fontfeature/
---
## FontFeature enumeration

توفر ميزات معلومات حول كيفية استخدام الحروف الرسومية في الخط لعرض البرنامج النصي. https://docs.microsoft.com/en-us/typography/opentype/spec/featuretags

```csharp
public enum FontFeature
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| GlyphCompositionDecomposition | `1667460464` | لتقليل عدد البدائل بين الحروف، من المستحسن أحيانًا تحليل الحرف الافتراضي لحرف ما إلى حرفين أو أكثر. بالإضافة إلى ذلك، قد يكون من الأفضل تكوين حروف افتراضية لحرفين أو أكثر في حرف واحد لمعالجة الحروف بشكل أفضل. تسمح هذه الميزة بمثل هذا التكوين/التحليل. https://docs.microsoft.com/en-us/typography/opentype/spec/features_ae#ccmp علامة OpenType المكافئة: 'ccmp' |
| StandardLigatures | `1818847073` | يستبدل سلسلة من الحروف بحرف واحد مفضل لأغراض الطباعة. تغطي هذه الميزة الأربطة التي يقرر المصمم/الشركة المصنعة أنه يجب استخدامها في الظروف العادية. علامة OpenType المكافئة: 'liga' https://docs.microsoft.com/en-us/typography/opentype/spec/features_ko#liga |
| RequiredLigatures | `1919707495` | يستبدل سلسلة من الحروف بحرف واحد مفضل لأغراض الطباعة. تغطي هذه الميزة تلك الأربطة، التي يحددها البرنامج النصي على أنها مطلوبة للاستخدام في الظروف العادية. هذه الميزة مهمة لبعض البرامج النصية لضمان تكوين الحروف بشكل صحيح. https://docs.microsoft.com/en-us/typography/opentype/spec/features_pt#rlig علامة OpenType المكافئة: 'rlig' |
| ContextualLigatures | `1668049255` | يستبدل سلسلة من الحروف بحرف واحد مفضل لأغراض الطباعة. على عكس ميزات الربط الأخرى، يحدد 'clig' السياق الذي يوصى فيه بالربط. تُعد هذه الإمكانية مهمة في بعض تصميمات النصوص ولربطات swash. https://docs.microsoft.com/en-us/typography/opentype/spec/features_ae#clig علامة OpenType المكافئة: 'clig' |
| DiscretionaryLigatures | `1684826471` | يستبدل سلسلة من الحروف بحرف واحد مفضل لأغراض الطباعة. تغطي هذه الميزة تلك الروابط التي يمكن استخدامها للتأثيرات الخاصة، حسب تفضيل المستخدم. https://docs.microsoft.com/en-us/typography/opentype/spec/features_ae#dlig علامة OpenType المكافئة: 'dlig' |
| HistoricalLigatures | `1751935335` | كانت بعض الروابط مستخدمة بشكل شائع في الماضي، ولكنها تبدو قديمة اليوم. تتضمن بعض الخطوط الأشكال التاريخية كبدائل، لذا يمكن استخدامها لتأثير "الفترة". تستبدل هذه الميزة الأشكال الافتراضية (الحالية) بالبدائل التاريخية. https://docs.microsoft.com/en-us/typography/opentype/spec/features_fj#hlig علامة OpenType المكافئة: 'hlig' |
| ProportionalFigures | `1886287213` | يستبدل رموز الأشكال الموجودة على عرض موحد (جدولي) برموز مقابلة موجودة على عرض خاص بالرموز (متناسب). https://docs.microsoft.com/en-us/typography/opentype/spec/features_pt#tag-pnum علامة OpenType المكافئة: 'pnum' |
| TabularFigures | `1953396077` | يستبدل رموز الأشكال المحددة بعرض متناسب بالرموز المقابلة المحددة بعرض موحد (جدولي). ستكون العروض الجدولية هي الافتراضية بشكل عام، ولكن لا يمكن افتراض ذلك بأمان. بالطبع لن تكون هذه الميزة موجودة في التصميمات أحادية المسافة. https://docs.microsoft.com/en-us/typography/opentype/spec/features_pt#tag-tnum علامة OpenType المكافئة: 'tnum' |
| LiningFigures | `1819178349` | تعمل هذه الميزة على تغيير الأشكال غير المبطنة المحددة إلى أشكال مبطنة. https://docs.microsoft.com/en-us/typography/opentype/spec/features_ko#lnum علامة OpenType المكافئة: 'lnum' |
| OldstyleFigures | `1869509997` | تعمل هذه الميزة على تغيير الأشكال المحددة من النمط الافتراضي أو نمط التبطين إلى النموذج القديم. https://docs.microsoft.com/en-us/typography/opentype/spec/features_ko#onum علامة OpenType المكافئة: 'onum' |
| VerticalAlternates | `1986359924` | يحول الحروف الرسومية الافتراضية إلى حروف رسومية مناسبة للعرض المستقيم في وضع الكتابة الرأسي. https://docs.microsoft.com/en-us/typography/opentype/spec/features_uz#tag-vert علامة OpenType المكافئة: 'vert' |
| VerticalAlternatesAndRotation | `1987212338` | يستبدل بعض الحروف ذات العرض الثابت (نصف أو ثلث أو ربع العرض) أو ذات العرض المتناسب (معظمها لاتينية أو كاتاكانا) بأشكال مناسبة للكتابة الرأسية (أي، تدور 90 درجة في اتجاه عقارب الساعة). https://docs.microsoft.com/en-us/typography/opentype/spec/features_uz#tag-vrt2 علامة OpenType المكافئة: 'vrt2' |
| StylisticSet01 | `1936928817` | المجموعة الأسلوبية 1 بالإضافة إلى، أو بدلاً من، البدائل الأسلوبية للرموز الفردية (انظر ميزة "salt")، قد تحتوي بعض الخطوط على مجموعات من الرموز الأسلوبية المتنوعة التي تتوافق مع أجزاء من مجموعة الأحرف، على سبيل المثال، متغيرات متعددة للأحرف الصغيرة في الخط اللاتيني. https://docs.microsoft.com/en-us/typography/opentype/spec/features_pt#tag-ss01---ss20 علامة OpenType المكافئة: 'ss01' |
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
| Kerning | `1801810542` | يضبط مقدار المسافة بين الحروف، لتوفير تباعد بصري متسق بين الحروف. على الرغم من أن الخطوط المصممة جيدًا تتميز بمسافات متسقة بين الحروف بشكل عام، إلا أن بعض مجموعات الحروف تتطلب تعديلًا لتحسين الوضوح. بالإضافة إلى التعديل القياسي في الاتجاه الأفقي، يمكن لهذه الميزة توفير بيانات التباعد بين الحروف المعتمدة على الحجم عبر جداول الأجهزة، التباعد بين الحروف "عبر التيار" في اتجاه النص Y، وتعديل موضع الحرف بشكل مستقل عن التعديل المسبق. لاحظ أن هذه الميزة قد تنطبق على عمليات تشغيل لأكثر من حرفين، ولن تُستخدم في الخطوط أحادية المسافة. لاحظ أيضًا أن هذه الميزة لا تنطبق على النصوص الموضوعة عموديًا. https://docs.microsoft.com/en-us/typography/opentype/spec/features_ko#kern علامة OpenType المكافئة: 'kern' |

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Shaping](../../aspose.words.shaping/)
* المجسم [Aspose.Words](../../)
