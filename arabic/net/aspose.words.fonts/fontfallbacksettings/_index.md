---
title: FontFallbackSettings Class
linktitle: FontFallbackSettings
articleTitle: FontFallbackSettings
second_title: Aspose.Words لـ .NET
description: اكتشف Aspose.Words.Fonts.FontFallbackSettings للحصول على خيارات خط بديلة قابلة للتخصيص، مما يضمن عرض المستندات بشكل سلس وعرض النص بشكل محسّن.
type: docs
weight: 3330
url: /ar/net/aspose.words.fonts/fontfallbacksettings/
---
## FontFallbackSettings class

يحدد إعدادات آلية الرجوع إلى الخط.

لمعرفة المزيد، قم بزيارة[العمل مع الخطوط](https://docs.aspose.com/words/net/working-with-fonts/) مقالة توثيقية.

```csharp
public class FontFallbackSettings
```

## طُرق

| اسم | وصف |
| --- | --- |
| [BuildAutomatic](../../aspose.words.fonts/fontfallbacksettings/buildautomatic/)() | يقوم تلقائيًا ببناء إعدادات احتياطية عن طريق مسح الخطوط المتوفرة. |
| [Load](../../aspose.words.fonts/fontfallbacksettings/load/#load)(*Stream*) | يقوم بتحميل الإعدادات الاحتياطية من دفق XML. |
| [Load](../../aspose.words.fonts/fontfallbacksettings/load/#load_1)(*string*) | يقوم بتحميل إعدادات الخط الاحتياطية من ملف XML. |
| [LoadMsOfficeFallbackSettings](../../aspose.words.fonts/fontfallbacksettings/loadmsofficefallbacksettings/)() | يقوم بتحميل إعدادات احتياطية محددة مسبقًا والتي تحاكي إعدادات Microsoft Word الاحتياطية وتستخدم خطوط Microsoft Office. |
| [LoadNotoFallbackSettings](../../aspose.words.fonts/fontfallbacksettings/loadnotofallbacksettings/)() | يقوم بتحميل إعدادات احتياطية محددة مسبقًا والتي تستخدم خطوط Google Noto. |
| [Save](../../aspose.words.fonts/fontfallbacksettings/save/#save)(*Stream*) | يحفظ إعدادات الرجوع الحالية إلى البث. |
| [Save](../../aspose.words.fonts/fontfallbacksettings/save/#save_1)(*string*) | يحفظ إعدادات الرجوع الحالية إلى الملف. |

## ملاحظات

بشكل افتراضي، يتم تهيئة إعدادات الرجوع إلى الوضع الاحتياطي بإعدادات محددة مسبقًا تحاكي إعدادات الرجوع إلى الوضع الاحتياطي لبرنامج Microsoft Word.

## أمثلة

يوضح كيفية توزيع الخطوط البديلة عبر نطاقات رموز أحرف Unicode.

```csharp
Document doc = new Document();

FontSettings fontSettings = new FontSettings();
doc.FontSettings = fontSettings;
FontFallbackSettings fontFallbackSettings = fontSettings.FallbackSettings;

// قم بتكوين إعدادات الخط لدينا للحصول على الخطوط المصدرية فقط من مجلد "MyFonts".
FolderFontSource folderFontSource = new FolderFontSource(FontsDir, false);
fontSettings.SetFontsSources(new FontSourceBase[] {folderFontSource});

// سيؤدي استدعاء طريقة "BuildAutomatic" إلى إنشاء مخطط احتياطي
// يقوم بتوزيع الخطوط التي يمكن الوصول إليها عبر أكبر عدد ممكن من أكواد أحرف Unicode.
// في حالتنا، لا يتوفر لدينا سوى إمكانية الوصول إلى عدد قليل من الخطوط داخل مجلد "MyFonts".
fontFallbackSettings.BuildAutomatic();
fontFallbackSettings.Save(ArtifactsDir + "FontSettings.FallbackSettingsCustom.BuildAutomatic.xml");

//يمكننا أيضًا تحميل مخطط استبدال مخصص من ملف مثل هذا.
// يطبق هذا المخطط الخط "AllegroOpen" عبر كتل Unicode "0000-00ff"، والخط "AllegroOpen" عبر "0100-024f"،
// والخط "M+ 2m" في جميع النطاقات الأخرى التي لا تغطيها الخطوط الأخرى في المخطط.
fontFallbackSettings.Load(MyDir + "Custom font fallback settings.xml");

// قم بإنشاء منشئ مستندات وضبط الخط الخاص به على خط غير موجود في أي من مصادرنا.
// ستستدعي إعدادات الخط لدينا مخططًا احتياطيًا للأحرف التي نكتبها باستخدام الخط غير المتوفر.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Font.Name = "Missing Font";

// استخدم المنشئ لطباعة كل حرف Unicode من 0x0021 إلى 0x052F،
// مع خطوط وصفية تقسم كتل Unicode التي حددناها في مخطط الخط المخصص لدينا.
for (int i = 0x0021; i < 0x0530; i++)
{
    switch (i)
    {
        case 0x0021:
            builder.Writeln(
                "\n\n0x0021 - 0x00FF: \nBasic Latin/Latin-1 Supplement Unicode blocks in \"AllegroOpen\" font:");
            break;
        case 0x0100:
            builder.Writeln(
                "\n\n0x0100 - 0x024F: \nLatin Extended A/B blocks, mostly in \"AllegroOpen\" font:");
            break;
        case 0x0250:
            builder.Writeln("\n\n0x0250 - 0x052F: \nIPA/Greek/Cyrillic blocks in \"M+ 2m\" font:");
            break;
    }

    builder.Write($"{Convert.ToChar(i)}");
}

doc.Save(ArtifactsDir + "FontSettings.FallbackSettingsCustom.pdf");
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Fonts](../../aspose.words.fonts/)
* المجسم [Aspose.Words](../../)
