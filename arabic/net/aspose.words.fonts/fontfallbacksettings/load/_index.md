---
title: FontFallbackSettings.Load
second_title: Aspose.Words لمراجع .NET API
description: FontFallbackSettings طريقة. تحميل الإعدادات الاحتياطية للخط من ملف XML.
type: docs
weight: 20
url: /ar/net/aspose.words.fonts/fontfallbacksettings/load/
---
## Load(string) {#load_1}

تحميل الإعدادات الاحتياطية للخط من ملف XML.

```csharp
public void Load(string fileName)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| fileName | String | اسم ملف الإدخال. |

### أمثلة

يوضح كيفية تحميل وحفظ إعدادات الخط الاحتياطية من/إلى مستند XML في نظام الملفات المحلي.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// قم بتحميل مستند XML يحدد مجموعة من الإعدادات الاحتياطية للخط.
FontSettings fontSettings = new FontSettings();
fontSettings.FallbackSettings.Load(MyDir + "Font fallback rules.xml");

doc.FontSettings = fontSettings;
doc.Save(ArtifactsDir + "FontSettings.LoadFontFallbackSettingsFromFile.pdf");

// احفظ الإعدادات الاحتياطية للخط الحالي للمستند كمستند XML.
doc.FontSettings.FallbackSettings.Save(ArtifactsDir + "FallbackSettings.xml");
```

### أنظر أيضا

* class [FontFallbackSettings](../)
* مساحة الاسم [Aspose.Words.Fonts](../../fontfallbacksettings/)
* المجسم [Aspose.Words](../../../)

---

## Load(Stream) {#load}

يقوم بتحميل الإعدادات الاحتياطية من تدفق XML.

```csharp
public void Load(Stream stream)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| stream | Stream | تيار الإدخال. |

### أمثلة

يوضح كيفية تحميل وحفظ إعدادات الخط الاحتياطية من/إلى التدفق.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// قم بتحميل مستند XML يحدد مجموعة من الإعدادات الاحتياطية للخط.
using (FileStream fontFallbackStream = new FileStream(MyDir + "Font fallback rules.xml", FileMode.Open))
{
    FontSettings fontSettings = new FontSettings();
    fontSettings.FallbackSettings.Load(fontFallbackStream);

    doc.FontSettings = fontSettings;
}

doc.Save(ArtifactsDir + "FontSettings.LoadFontFallbackSettingsFromStream.pdf");

// استخدم الدفق لحفظ الإعدادات الاحتياطية الحالية للخط في مستندنا كمستند XML.
using (FileStream fontFallbackStream =
    new FileStream(ArtifactsDir + "FallbackSettings.xml", FileMode.Create))
{
    doc.FontSettings.FallbackSettings.Save(fontFallbackStream);
}
```

### أنظر أيضا

* class [FontFallbackSettings](../)
* مساحة الاسم [Aspose.Words.Fonts](../../fontfallbacksettings/)
* المجسم [Aspose.Words](../../../)


