---
title: FontFallbackSettings.Save
second_title: Aspose.Words لمراجع .NET API
description: FontFallbackSettings طريقة. يحفظ الإعدادات الاحتياطية الحالية للبث.
type: docs
weight: 50
url: /ar/net/aspose.words.fonts/fontfallbacksettings/save/
---
## Save(Stream) {#save}

يحفظ الإعدادات الاحتياطية الحالية للبث.

```csharp
public void Save(Stream outputStream)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| outputStream | Stream | تيار الإخراج. |

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

---

## Save(string) {#save_1}

يحفظ الإعدادات الاحتياطية الحالية في الملف.

```csharp
public void Save(string fileName)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| fileName | String | ضع اسم الملف. |

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


