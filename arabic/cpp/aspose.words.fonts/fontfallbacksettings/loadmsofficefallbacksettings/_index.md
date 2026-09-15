---
title: "Aspose::Words::Fonts::FontFallbackSettings::LoadMsOfficeFallbackSettings method"
linktitle: "LoadMsOfficeFallbackSettings"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Fonts::FontFallbackSettings::LoadMsOfficeFallbackSettings method. يحمل إعدادات الاحتياطي المعرفة مسبقًا التي تحاكي احتياطي Microsoft Word وتستخدم خطوط Microsoft office في C++."
type: docs
weight: 6000
url: /ar/cpp/aspose.words.fonts/fontfallbacksettings/loadmsofficefallbacksettings/
---
## FontFallbackSettings::LoadMsOfficeFallbackSettings method


يقوم بتحميل إعدادات احتياطي مسبقة التعريف تحاكي احتياطي Microsoft Word وتستخدم خطوط Microsoft Office.

```cpp
void Aspose::Words::Fonts::FontFallbackSettings::LoadMsOfficeFallbackSettings()
```


## أمثلة



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
