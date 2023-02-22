---
title: Hyphenation.IsDictionaryRegistered
second_title: Aspose.Words لمراجع .NET API
description: Hyphenation طريقة. إرجاع خطأ إذا لم يكن هناك قاموس مسجل للغة المحددة أو إذا كان مسجلاً هو قاموس Null  أو إذا كان صحيحًا بخلاف ذلك.
type: docs
weight: 30
url: /ar/net/aspose.words/hyphenation/isdictionaryregistered/
---
## Hyphenation.IsDictionaryRegistered method

إرجاع خطأ إذا لم يكن هناك قاموس مسجل للغة المحددة أو إذا كان مسجلاً هو قاموس Null ، أو إذا كان صحيحًا بخلاف ذلك.

```csharp
public static bool IsDictionaryRegistered(string language)
```

### أمثلة

يوضح كيفية تسجيل قاموس الواصلة.

```csharp
// يحتوي قاموس الواصلة على قائمة بالسلاسل التي تحدد قواعد الواصلة للغة القاموس.
// عندما يحتوي المستند على سطور من النص يمكن فيها تقسيم الكلمة والاستمرار في السطر التالي ،
// ستبحث الواصلة في قائمة السلاسل في القاموس للسلاسل الفرعية لهذه الكلمة.
// إذا كان القاموس يحتوي على سلسلة فرعية ، فإن الواصلة ستقسم الكلمة على سطرين
// بواسطة السلسلة الفرعية وإضافة واصلة إلى النصف الأول.
// تسجيل ملف قاموس من نظام الملفات المحلي إلى لغة "de-CH".
Hyphenation.RegisterDictionary("de-CH", MyDir + "hyph_de_CH.dic");

Assert.True(Hyphenation.IsDictionaryRegistered("de-CH"));

// افتح مستندًا يحتوي على نص بلغة تطابق لغة قاموسنا ،
// واحفظه في تنسيق حفظ بصفحة ثابتة. سيتم وصل النص الموجود في هذا المستند.
Document doc = new Document(MyDir + "German text.docx");

Assert.True(doc.FirstSection.Body.FirstParagraph.Runs.OfType<Run>().All(
    r => r.Font.LocaleId == new CultureInfo("de-CH").LCID));

doc.Save(ArtifactsDir + "Hyphenation.Dictionary.Registered.pdf");

// أعد تحميل المستند بعد إلغاء تسجيل القاموس ،
// واحفظه في ملف PDF آخر ، والذي لن يحتوي على نصوص بواصلة.
Hyphenation.UnregisterDictionary("de-CH");

Assert.False(Hyphenation.IsDictionaryRegistered("de-CH"));

doc = new Document(MyDir + "German text.docx");
doc.Save(ArtifactsDir + "Hyphenation.Dictionary.Unregistered.pdf");
```

### أنظر أيضا

* class [Hyphenation](../)
* مساحة الاسم [Aspose.Words](../../hyphenation/)
* المجسم [Aspose.Words](../../../)


