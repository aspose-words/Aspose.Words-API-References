---
title: FontFallbackSettings.Load
linktitle: Load
articleTitle: Load
second_title: Aspose.Words لـ .NET
description: قم بتحميل وإدارة إعدادات الرجوع للخطوط بسهولة من ملفات XML باستخدام طريقة تحميل FontFallbackSettings للتكامل السلس مع الطباعة.
type: docs
weight: 20
url: /ar/net/aspose.words.fonts/fontfallbacksettings/load/
---
## Load(*string*) {#load_1}

يقوم بتحميل إعدادات الخط الاحتياطية من ملف XML.

```csharp
public void Load(string fileName)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| fileName | String | اسم ملف الإدخال. |

## أمثلة

يوضح كيفية تحميل إعدادات الخط الاحتياطي وحفظها من/إلى مستند XML في نظام الملفات المحلي.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// قم بتحميل مستند XML الذي يحدد مجموعة من إعدادات الخط الاحتياطية.
FontSettings fontSettings = new FontSettings();
fontSettings.FallbackSettings.Load(MyDir + "Font fallback rules.xml");

doc.FontSettings = fontSettings;
doc.Save(ArtifactsDir + "FontSettings.LoadFontFallbackSettingsFromFile.pdf");

// احفظ إعدادات الخط الاحتياطي الحالية لمستندنا كمستند XML.
doc.FontSettings.FallbackSettings.Save(ArtifactsDir + "FallbackSettings.xml");
```

### أنظر أيضا

* class [FontFallbackSettings](../)
* مساحة الاسم [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* المجسم [Aspose.Words](../../../)

---

## Load(*Stream*) {#load}

يقوم بتحميل الإعدادات الاحتياطية من دفق XML.

```csharp
public void Load(Stream stream)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| stream | Stream | تدفق الإدخال. |

## أمثلة

يوضح كيفية تحميل إعدادات الخط الاحتياطي وحفظها من/إلى مجرى ما.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// قم بتحميل مستند XML الذي يحدد مجموعة من إعدادات الخط الاحتياطية.
using (FileStream fontFallbackStream = new FileStream(MyDir + "Font fallback rules.xml", FileMode.Open))
{
    FontSettings fontSettings = new FontSettings();
    fontSettings.FallbackSettings.Load(fontFallbackStream);

    doc.FontSettings = fontSettings;
}

doc.Save(ArtifactsDir + "FontSettings.LoadFontFallbackSettingsFromStream.pdf");

// استخدم تيارًا لحفظ إعدادات الخط الاحتياطية الحالية لمستندنا كمستند XML.
using (FileStream fontFallbackStream =
    new FileStream(ArtifactsDir + "FallbackSettings.xml", FileMode.Create))
{
    doc.FontSettings.FallbackSettings.Save(fontFallbackStream);
}
```

### أنظر أيضا

* class [FontFallbackSettings](../)
* مساحة الاسم [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* المجسم [Aspose.Words](../../../)
