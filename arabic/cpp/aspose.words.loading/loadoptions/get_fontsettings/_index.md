---
title: "طريقة Aspose::Words::Loading::LoadOptions::get_FontSettings"
linktitle: "get_FontSettings"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Loading::LoadOptions::get_FontSettings. يسمح بتحديد إعدادات خطوط المستند في C++."
type: docs
weight: 7000
url: /ar/cpp/aspose.words.loading/loadoptions/get_fontsettings/
---
## LoadOptions::get_FontSettings method


يسمح بتحديد إعدادات خط المستند.

```cpp
System::SharedPtr<Aspose::Words::Fonts::FontSettings> Aspose::Words::Loading::LoadOptions::get_FontSettings() const
```

## ملاحظات


عند تحميل بعض الصيغ، قد تحتاج Aspose.Words إلى حل الخطوط. على سبيل المثال، عند تحميل مستندات HTML قد تقوم [Aspose.Words](../../../aspose.words/) بحل الخطوط لتنفيذ fallback للخط.

إذا تم تعيينه إلى **null**، سيتم استخدام إعدادات الخط الثابتة الافتراضية [DefaultInstance](../../../aspose.words.fonts/fontsettings/get_defaultinstance/).

القيمة الافتراضية هي **null**.

## أمثلة



يوضح كيفية تعيين بدائل الخطوط أثناء التحميل.
```cpp
auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
loadOptions->set_FontSettings(System::MakeObject<Aspose::Words::Fonts::FontSettings>());

// قم بتعيين قاعدة استبدال الخط لكائن LoadOptions.
// إذا كان المستند الذي نقوم بتحميله يستخدم خطًا غير متوفر لدينا،
// ستستبدل هذه القاعدة الخط غير المتوفر بآخر موجود.
// في هذه الحالة، سيتحول كل استخدام للخط "MissingFont" إلى "Comic Sans MS".
System::SharedPtr<Aspose::Words::Fonts::TableSubstitutionRule> substitutionRule = loadOptions->get_FontSettings()->get_SubstitutionSettings()->get_TableSubstitution();
substitutionRule->AddSubstitutes(u"MissingFont", System::MakeArray<System::String>({u"Comic Sans MS"}));

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Missing font.html", loadOptions);

// في هذه المرحلة سيظل هذا النص في "MissingFont".
// ستتم استبدال الخط عندما نقوم بعرض المستند.
ASSERT_EQ(u"MissingFont", doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)->get_Font()->get_Name());

doc->Save(get_ArtifactsDir() + u"FontSettings.ResolveFontsBeforeLoadingDocument.pdf");
```


يظهر كيفية تطبيق إعدادات استبدال الخط أثناء تحميل المستند.
```cpp
// إنشاء كائن FontSettings سيستبدل الخط "Times New Roman"
// بالخط "Arvo" من مجلد "MyFonts" الخاص بنا.
auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
fontSettings->SetFontsFolder(get_FontsDir(), false);
fontSettings->get_SubstitutionSettings()->get_TableSubstitution()->AddSubstitutes(u"Times New Roman", System::MakeArray<System::String>({u"Arvo"}));

// قم بتعيين كائن FontSettings هذا كخاصية لكائن LoadOptions الذي تم إنشاؤه حديثًا.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
loadOptions->set_FontSettings(fontSettings);

// حمّل المستند، ثم اعرضه كملف PDF مع استبدال الخط.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx", loadOptions);

doc->Save(get_ArtifactsDir() + u"LoadOptions.FontSettings.pdf");
```

## انظر أيضًا

* Class [FontSettings](../../../aspose.words.fonts/fontsettings/)
* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
