---
title: "طريقة Aspose::Words::Fonts::FontFallbackSettings::LoadNotoFallbackSettings"
linktitle: "LoadNotoFallbackSettings"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Fonts::FontFallbackSettings::LoadNotoFallbackSettings. تقوم بتحميل إعدادات احتياطي مسبقة التعريف تستخدم خطوط Google Noto في C++."
type: docs
weight: 7000
url: /ar/cpp/aspose.words.fonts/fontfallbacksettings/loadnotofallbacksettings/
---
## FontFallbackSettings::LoadNotoFallbackSettings method


يقوم بتحميل إعدادات احتياطي مسبقة التعريف التي تستخدم خطوط Google Noto.

```cpp
void Aspose::Words::Fonts::FontFallbackSettings::LoadNotoFallbackSettings()
```


## أمثلة



يظهر كيفية إضافة إعدادات احتياطي مسبقة للخطوط لخطوط Google Noto.
```cpp
auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();

// هذه خطوط مجانية مرخصة بموجب رخصة SIL Open Font License.
// يمكننا تنزيل الخطوط هنا:
// https://www.google.com/get/noto/#sans-lgc
fontSettings->SetFontsFolder(get_FontsDir() + u"Noto", false);

// لاحظ أن الإعدادات المسبقة تستخدم فقط خطوط Noto بنمط Sans وبالوزن العادي.
// بعض خطوط Noto تستخدم ميزات طباعة متقدمة.
// قد لا يتم عرض الخطوط التي تحتوي على طباعة متقدمة بشكل صحيح لأن Aspose.Words لا يدعمها حاليًا.
fontSettings->get_FallbackSettings()->LoadNotoFallbackSettings();
fontSettings->get_SubstitutionSettings()->get_FontInfoSubstitution()->set_Enabled(false);
fontSettings->get_SubstitutionSettings()->get_DefaultFontSubstitution()->set_DefaultFontName(u"Noto Sans");

auto doc = System::MakeObject<Aspose::Words::Document>();
doc->set_FontSettings(fontSettings);
```


يظهر كيفية تحميل إعدادات احتياطي للخط مسبقة التعريف.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
doc->set_FontSettings(fontSettings);
System::SharedPtr<Aspose::Words::Fonts::FontFallbackSettings> fontFallbackSettings = fontSettings->get_FallbackSettings();

// احفظ مخطط الخط الاحتياطي الافتراضي إلى مستند XML.
// على سبيل المثال، أحد العناصر لديه قيمة "0C00-0C7F" للمدى وقيمة "Vani" المقابلة لـ FallbackFonts.
// هذا يعني أنه إذا كان الخط الذي يستخدمه النص لا يحتوي على رموز لكتلة Unicode 0x0C00-0x0C7F،
// سيستخدم مخطط الاحتياطي الرموز من الخط البديل "Vani".
fontFallbackSettings->Save(get_ArtifactsDir() + u"FontSettings.FallbackSettings.Default.xml");

// فيما يلي مخططان احتياطيان للخط محددان مسبقًا يمكننا الاختيار من بينهما.
// 1 -  استخدم مخطط Microsoft Office الافتراضي، وهو نفسه المخطط الافتراضي:
fontFallbackSettings->LoadMsOfficeFallbackSettings();
fontFallbackSettings->Save(get_ArtifactsDir() + u"FontSettings.FallbackSettings.LoadMsOfficeFallbackSettings.xml");

// 2 -  استخدم المخطط المبني من خطوط Google Noto:
fontFallbackSettings->LoadNotoFallbackSettings();
fontFallbackSettings->Save(get_ArtifactsDir() + u"FontSettings.FallbackSettings.LoadNotoFallbackSettings.xml");
```

## انظر أيضًا

* Class [FontFallbackSettings](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
