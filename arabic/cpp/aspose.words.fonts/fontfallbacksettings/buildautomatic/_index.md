---
title: "Aspose::Words::Fonts::FontFallbackSettings::BuildAutomatic method"
linktitle: "BuildAutomatic"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Fonts::FontFallbackSettings::BuildAutomatic method. يبني إعدادات الاحتياطي تلقائيًا عن طريق فحص الخطوط المتاحة في C++."
type: docs
weight: 2000
url: /ar/cpp/aspose.words.fonts/fontfallbacksettings/buildautomatic/
---
## FontFallbackSettings::BuildAutomatic method


يبني إعدادات الاحتياطي تلقائيًا عن طريق مسح الخطوط المتاحة.

```cpp
void Aspose::Words::Fonts::FontFallbackSettings::BuildAutomatic()
```


## أمثلة



يوضح كيفية توزيع خطوط الاحتياطي عبر نطاقات رموز الأحرف Unicode.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
doc->set_FontSettings(fontSettings);
System::SharedPtr<Aspose::Words::Fonts::FontFallbackSettings> fontFallbackSettings = fontSettings->get_FallbackSettings();

// قم بتكوين إعدادات الخط لدينا لتستورد الخطوط فقط من المجلد "MyFonts".
auto folderFontSource = System::MakeObject<Aspose::Words::Fonts::FolderFontSource>(get_FontsDir(), false);
fontSettings->SetFontsSources(System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({folderFontSource}));

// ستؤدي استدعاء الطريقة "BuildAutomatic" إلى إنشاء مخطط احتياطي
// يقوم بتوزيع الخطوط المتاحة عبر أكبر عدد ممكن من رموز الأحرف Unicode.
// في حالتنا، لا يمكنه الوصول إلا إلى القليل من الخطوط داخل المجلد "MyFonts".
fontFallbackSettings->BuildAutomatic();
fontFallbackSettings->Save(get_ArtifactsDir() + u"FontSettings.FallbackSettingsCustom.BuildAutomatic.xml");

// يمكننا أيضًا تحميل مخطط استبدال مخصص من ملف مثل هذا.
// يطبق هذا المخطط الخط "AllegroOpen" عبر كتل Unicode "0000-00ff"، والخط "AllegroOpen" عبر "0100-024f"،
// وخط "M+ 2m" في جميع النطاقات الأخرى التي لا تغطيها الخطوط الأخرى في المخطط.
fontFallbackSettings->Load(get_MyDir() + u"Custom font fallback settings.xml");

// أنشئ منشئ مستندات واضبط خطه على خط غير موجود في أي من مصادرنا.
// ستستدعي إعدادات الخط لدينا مخطط الاحتياطي للأحرف التي نكتبها باستخدام الخط غير المتاح.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->get_Font()->set_Name(u"Missing Font");

// استخدم المنشئ لطباعة كل حرف Unicode من 0x0021 إلى 0x052F،
// مع أسطر وصفية تقسم كتل Unicode التي حددناها في مخطط احتياطي الخط المخصص لدينا.
for (int32_t i = 0x0021; i < 0x0530; i++)
{
    switch (i)
    {
        case 0x0021:
            builder->Writeln(u"\n\n0x0021 - 0x00FF: \nBasic Latin/Latin-1 Supplement Unicode blocks in \"AllegroOpen\" font:");
            break;

        case 0x0100:
            builder->Writeln(u"\n\n0x0100 - 0x024F: \nLatin Extended A/B blocks, mostly in \"AllegroOpen\" font:");
            break;

        case 0x0250:
            builder->Writeln(u"\n\n0x0250 - 0x052F: \nIPA/Greek/Cyrillic blocks in \"M+ 2m\" font:");
            break;

    }

    builder->Write(System::String::Format(u"{0}", System::Convert::ToChar(i)));
}

doc->Save(get_ArtifactsDir() + u"FontSettings.FallbackSettingsCustom.pdf");
```

## انظر أيضًا

* Class [FontFallbackSettings](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
