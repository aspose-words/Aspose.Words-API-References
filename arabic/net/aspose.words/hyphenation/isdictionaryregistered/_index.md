---
title: Hyphenation.IsDictionaryRegistered
linktitle: IsDictionaryRegistered
articleTitle: IsDictionaryRegistered
second_title: Aspose.Words لـ .NET
description: اكتشف طريقة Hyphenation IsDictionaryRegistered، والتي تتحقق مما إذا كان هناك قاموس مسجل للغة الخاصة بك، مما يضمن دقة استخدام الواصلة في تطبيقاتك.
type: docs
weight: 30
url: /ar/net/aspose.words/hyphenation/isdictionaryregistered/
---
## Hyphenation.IsDictionaryRegistered method

إرجاع`خطأ شنيع` إذا لم يكن هناك قاموس مسجل للغة المحددة أو إذا كان القاموس المسجل فارغًا،`حقيقي` وإلا.

```csharp
public static bool IsDictionaryRegistered(string language)
```

## أمثلة

يوضح كيفية تسجيل قاموس الوصلات.

```csharp
//يحتوي قاموس الوصل على قائمة من السلاسل التي تحدد قواعد الوصل للغة القاموس.
// عندما تحتوي الوثيقة على أسطر نصية يمكن تقسيم الكلمة فيها ومتابعتها في السطر التالي،
// سوف يبحث الواصلة في قائمة القاموس الخاصة بالسلاسل عن السلاسل الفرعية لتلك الكلمة.
// إذا كان القاموس يحتوي على سلسلة فرعية، فإن الوصلة ستقسم الكلمة عبر سطرين
// بواسطة السلسلة الفرعية وأضف شرطة إلى النصف الأول.
// قم بتسجيل ملف القاموس من نظام الملفات المحلي إلى الإعدادات المحلية "de-CH".
Hyphenation.RegisterDictionary("de-CH", MyDir + "hyph_de_CH.dic");

Assert.True(Hyphenation.IsDictionaryRegistered("de-CH"));

// افتح مستندًا يحتوي على نص بإعدادات محلية مطابقة لإعدادات القاموس لدينا،
// واحفظه بتنسيق صفحة ثابتة. سيتم وضع واصلة بين النص في هذا المستند.
Document doc = new Document(MyDir + "German text.docx");

Assert.True(doc.FirstSection.Body.FirstParagraph.Runs.OfType<Run>().All(
    r => r.Font.LocaleId == new CultureInfo("de-CH").LCID));

doc.Save(ArtifactsDir + "Hyphenation.Dictionary.Registered.pdf");

// أعد تحميل المستند بعد إلغاء تسجيل القاموس،
// واحفظه في ملف PDF آخر، والذي لن يحتوي على نص به واصلة.
Hyphenation.UnregisterDictionary("de-CH");

Assert.False(Hyphenation.IsDictionaryRegistered("de-CH"));

doc = new Document(MyDir + "German text.docx");
doc.Save(ArtifactsDir + "Hyphenation.Dictionary.Unregistered.pdf");
```

### أنظر أيضا

* class [Hyphenation](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
