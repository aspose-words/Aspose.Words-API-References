---
title: FontFallbackSettings Class
linktitle: FontFallbackSettings
articleTitle: FontFallbackSettings
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Fonts.FontFallbackSettings فصل. يحدد إعدادات آلية الرجوع للخط في C#.
type: docs
weight: 2900
url: /ar/net/aspose.words.fonts/fontfallbacksettings/
---
## FontFallbackSettings class

يحدد إعدادات آلية الرجوع للخط.

لمعرفة المزيد، قم بزيارة[العمل مع الخطوط](https://docs.aspose.com/words/net/working-with-fonts/) مقالة توثيقية.

```csharp
public class FontFallbackSettings
```

## طُرق

| اسم | وصف |
| --- | --- |
| [BuildAutomatic](../../aspose.words.fonts/fontfallbacksettings/buildautomatic/)() | إنشاء الإعدادات الاحتياطية تلقائيًا عن طريق فحص الخطوط المتاحة. |
| [Load](../../aspose.words.fonts/fontfallbacksettings/load/#load)(*Stream*) | يقوم بتحميل الإعدادات الاحتياطية من تدفق XML. |
| [Load](../../aspose.words.fonts/fontfallbacksettings/load/#load_1)(*string*) | تحميل الإعدادات الاحتياطية للخط من ملف XML. |
| [LoadMsOfficeFallbackSettings](../../aspose.words.fonts/fontfallbacksettings/loadmsofficefallbacksettings/)() | يقوم بتحميل الإعدادات الاحتياطية المحددة مسبقًا والتي تحاكي الإجراء الاحتياطي لـ Microsoft Word وتستخدم خطوط Microsoft Office. |
| [LoadNotoFallbackSettings](../../aspose.words.fonts/fontfallbacksettings/loadnotofallbacksettings/)() | يقوم بتحميل الإعدادات الاحتياطية المحددة مسبقًا والتي تستخدم خطوط Google Noto. |
| [Save](../../aspose.words.fonts/fontfallbacksettings/save/#save)(*Stream*) | يحفظ الإعدادات الاحتياطية الحالية للبث. |
| [Save](../../aspose.words.fonts/fontfallbacksettings/save/#save_1)(*string*) | يحفظ الإعدادات الاحتياطية الحالية في الملف. |

## ملاحظات

بشكل افتراضي تتم تهيئة الإعدادات الاحتياطية بإعدادات محددة مسبقًا والتي تحاكي الإجراء الاحتياطي لـ Microsoft Word.

## أمثلة

يوضح كيفية توزيع الخطوط الاحتياطية عبر نطاقات رموز أحرف Unicode.

```csharp
Document doc = new Document();

FontSettings fontSettings = new FontSettings();
doc.FontSettings = fontSettings;
FontFallbackSettings fontFallbackSettings = fontSettings.FallbackSettings;

// قم بتكوين إعدادات الخطوط الخاصة بنا لمصدر الخطوط فقط من المجلد "MyFonts".
FolderFontSource folderFontSource = new FolderFontSource(FontsDir, false);
fontSettings.SetFontsSources(new FontSourceBase[] {folderFontSource});

// سيؤدي استدعاء الأسلوب "BuildAutomatic" إلى إنشاء مخطط احتياطي
// يوزع الخطوط التي يمكن الوصول إليها عبر أكبر عدد ممكن من رموز أحرف Unicode.
// في حالتنا، يمكنه فقط الوصول إلى عدد قليل من الخطوط الموجودة داخل المجلد "MyFonts".
fontFallbackSettings.BuildAutomatic();
fontFallbackSettings.Save(ArtifactsDir + "FontSettings.FallbackSettingsCustom.BuildAutomatic.xml");

// يمكننا أيضًا تحميل نظام استبدال مخصص من ملف مثل هذا.
// يطبق هذا المخطط الخط "AllegroOpen" عبر كتل Unicode "0000-00ff"، والخط "AllegroOpen" عبر "0100-024f"،
// والخط "M+ 2m" في جميع النطاقات الأخرى التي لا تغطيها الخطوط الأخرى في المخطط.
fontFallbackSettings.Load(MyDir + "Custom font fallback settings.xml");

// قم بإنشاء منشئ المستندات وقم بتعيين الخط الخاص به على خط غير موجود في أي من مصادرنا.
// ستستدعي إعدادات الخط لدينا النظام الاحتياطي للأحرف التي نكتبها باستخدام الخط غير المتاح.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Font.Name = "Missing Font";

// استخدم المنشئ لطباعة كل حرف Unicode من 0x0021 إلى 0x052F،
// مع خطوط وصفية تقسم كتل Unicode التي حددناها في نظامنا الاحتياطي للخط المخصص.
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
