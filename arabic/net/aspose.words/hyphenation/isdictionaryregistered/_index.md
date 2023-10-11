---
title: Hyphenation.IsDictionaryRegistered
second_title: Aspose.Words لمراجع .NET API
description: Hyphenation طريقة. إرجاعخطأ شنيع إذا لم يكن هناك قاموس مسجل للغة المحددة أو إذا كان المسجل هو قاموس فارغحقيقي وإلا.
type: docs
weight: 30
url: /ar/net/aspose.words/hyphenation/isdictionaryregistered/
---
## Hyphenation.IsDictionaryRegistered method

إرجاع`خطأ شنيع` إذا لم يكن هناك قاموس مسجل للغة المحددة أو إذا كان المسجل هو قاموس فارغ،`حقيقي` وإلا.

```csharp
public static bool IsDictionaryRegistered(string language)
```

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


