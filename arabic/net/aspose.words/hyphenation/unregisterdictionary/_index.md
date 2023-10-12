---
title: Hyphenation.UnregisterDictionary
second_title: Aspose.Words لمراجع .NET API
description: Hyphenation طريقة. إلغاء تسجيل قاموس الواصلة للغة المحددة.
type: docs
weight: 50
url: /ar/net/aspose.words/hyphenation/unregisterdictionary/
---
## Hyphenation.UnregisterDictionary method

إلغاء تسجيل قاموس الواصلة للغة المحددة.

وهذا يختلف عن تسجيل قاموس فارغ. يؤدي إلغاء تسجيل القاموس إلى تمكين رد الاتصال باللغة المحددة.

```csharp
public static void UnregisterDictionary(string language)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| language | String | اسم لغة، على سبيل المثال "en-US". راجع وثائق .NET لـ "اسم الثقافة" وRFC 4646 للحصول على التفاصيل. |

### أمثلة

يوضح كيفية تسجيل قاموس الواصلة.

```csharp
// يحتوي قاموس الواصلة على قائمة من السلاسل التي تحدد قواعد الواصلة للغة القاموس.
// عندما يحتوي المستند على أسطر نصية يمكن فيها تقسيم الكلمة واستمرارها في السطر التالي،
// ستبحث الواصلة في قائمة سلاسل القاموس عن السلاسل الفرعية لتلك الكلمة.
// إذا كان القاموس يحتوي على سلسلة فرعية، فستؤدي الواصلة إلى تقسيم الكلمة عبر سطرين
// بواسطة السلسلة الفرعية وأضف واصلة إلى النصف الأول.
// سجل ملف قاموس من نظام الملفات المحلي إلى لغة "de-CH".
Hyphenation.RegisterDictionary("de-CH", MyDir + "hyph_de_CH.dic");

Assert.True(Hyphenation.IsDictionaryRegistered("de-CH"));

// افتح مستندًا يحتوي على نص ذو لغة تطابق لغة القاموس الخاص بنا،
// وحفظه بتنسيق حفظ صفحة ثابتة. سيتم تطبيق الواصلة على النص الموجود في هذا المستند.
Document doc = new Document(MyDir + "German text.docx");

Assert.True(doc.FirstSection.Body.FirstParagraph.Runs.OfType<Run>().All(
    r => r.Font.LocaleId == new CultureInfo("de-CH").LCID));

doc.Save(ArtifactsDir + "Hyphenation.Dictionary.Registered.pdf");

// أعد تحميل المستند بعد إلغاء تسجيل القاموس،
// واحفظه في ملف PDF آخر، والذي لن يحتوي على نص موصول.
Hyphenation.UnregisterDictionary("de-CH");

Assert.False(Hyphenation.IsDictionaryRegistered("de-CH"));

doc = new Document(MyDir + "German text.docx");
doc.Save(ArtifactsDir + "Hyphenation.Dictionary.Unregistered.pdf");
```

### أنظر أيضا

* class [Hyphenation](../)
* مساحة الاسم [Aspose.Words](../../hyphenation/)
* المجسم [Aspose.Words](../../../)


