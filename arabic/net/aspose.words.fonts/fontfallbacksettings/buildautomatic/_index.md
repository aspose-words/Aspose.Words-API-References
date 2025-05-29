---
title: FontFallbackSettings.BuildAutomatic
linktitle: BuildAutomatic
articleTitle: BuildAutomatic
second_title: Aspose.Words لـ .NET
description: اكتشف طريقة FontFallbackSettings BuildAutomatic التي تقوم بمسح الخطوط بسهولة لإنشاء إعدادات احتياطية مثالية لتحسين الطباعة.
type: docs
weight: 10
url: /ar/net/aspose.words.fonts/fontfallbacksettings/buildautomatic/
---
## FontFallbackSettings.BuildAutomatic method

يقوم تلقائيًا ببناء إعدادات احتياطية عن طريق مسح الخطوط المتوفرة.

```csharp
public void BuildAutomatic()
```

## ملاحظات

قد تُنتج هذه الطريقة إعدادات احتياطية غير مثالية. يتم فحص الخطوط بواسطة[ نطاق أحرف Unicode ](https://docs.microsoft.com/en-us/typography/opentype/spec/os2#ur) الحقول، وليس بناءً على وجود الحروف الرسومية الفعلية. كما يتم فحص نطاقات يونيكود بشكل فردي ، وقد تستخدم عدة نطاقات مرتبطة بلغة/نص واحد خطوطًا احتياطية مختلفة.

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

* class [FontFallbackSettings](../)
* مساحة الاسم [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* المجسم [Aspose.Words](../../../)
