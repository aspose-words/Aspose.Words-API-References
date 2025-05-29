---
title: FontFallbackSettings.Save
linktitle: Save
articleTitle: Save
second_title: Aspose.Words لـ .NET
description: احفظ إعدادات الخط الاحتياطية بسهولة باستخدام طريقة الحفظ السهلة. احتفظ بإعداداتك الاحتياطية المخصصة لإدارة خطوطك بسلاسة.
type: docs
weight: 50
url: /ar/net/aspose.words.fonts/fontfallbacksettings/save/
---
## Save(*Stream*) {#save}

يحفظ إعدادات الرجوع الحالية إلى البث.

```csharp
public void Save(Stream outputStream)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| outputStream | Stream | تيار الإخراج. |

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

---

## Save(*string*) {#save_1}

يحفظ إعدادات الرجوع الحالية إلى الملف.

```csharp
public void Save(string fileName)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| fileName | String | اسم ملف الإخراج. |

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
