---
title: FontFallbackSettings.LoadNotoFallbackSettings
second_title: Aspose.Words لمراجع .NET API
description: FontFallbackSettings طريقة. يقوم بتحميل الإعدادات الاحتياطية المحددة مسبقًا والتي تستخدم خطوط Google Noto.
type: docs
weight: 40
url: /ar/net/aspose.words.fonts/fontfallbacksettings/loadnotofallbacksettings/
---
## FontFallbackSettings.LoadNotoFallbackSettings method

يقوم بتحميل الإعدادات الاحتياطية المحددة مسبقًا والتي تستخدم خطوط Google Noto.

```csharp
public void LoadNotoFallbackSettings()
```

### أمثلة

يوضح كيفية إضافة إعدادات احتياطية محددة مسبقًا لخطوط Google Noto.

```csharp
FontSettings fontSettings = new FontSettings();

// هذه خطوط مجانية مرخصة بموجب ترخيص SIL Open Font.
// يمكننا تنزيل الخطوط هنا:
// https://www.google.com/get/noto/#sans-lgc
fontSettings.SetFontsFolder(FontsDir + "Noto", false);

 // لاحظ أن الإعدادات المحددة مسبقًا تستخدم فقط خطوط Sans-style Noto ذات الوزن العادي.
// تستخدم بعض خطوط Noto ميزات الطباعة المتقدمة.
// الخطوط التي تتميز بطباعة متقدمة قد لا يتم عرضها بشكل صحيح لأن Aspose.Words لا تدعمها حاليًا.
fontSettings.FallbackSettings.LoadNotoFallbackSettings();
fontSettings.SubstitutionSettings.FontInfoSubstitution.Enabled = false;
fontSettings.SubstitutionSettings.DefaultFontSubstitution.DefaultFontName = "Noto Sans";

Document doc = new Document();
doc.FontSettings = fontSettings;
```

يوضح كيفية تحميل إعدادات الخط الاحتياطي المحددة مسبقًا.

```csharp
Document doc = new Document();

FontSettings fontSettings = new FontSettings();
doc.FontSettings = fontSettings;
FontFallbackSettings fontFallbackSettings = fontSettings.FallbackSettings;

// احفظ نظام الخطوط الاحتياطية الافتراضي في مستند XML.
// على سبيل المثال، أحد العناصر له قيمة "0C00-0C7F" للنطاق وقيمة "Vani" المقابلة لـ FallbackFonts.
// هذا يعني أنه إذا كان الخط الذي يستخدمه بعض النص لا يحتوي على رموز لكتلة Unicode 0x0C00-0x0C7F،
// سيستخدم المخطط الاحتياطي رموزًا من بديل الخط "Vani".
fontFallbackSettings.Save(ArtifactsDir + "FontSettings.FallbackSettings.Default.xml");

// يوجد أدناه نظامان احتياطيان محددان مسبقًا للخطوط يمكننا الاختيار من بينهما.
// 1 - استخدم نظام Microsoft Office الافتراضي، وهو نفس النظام الافتراضي:
fontFallbackSettings.LoadMsOfficeFallbackSettings();
fontFallbackSettings.Save(ArtifactsDir + "FontSettings.FallbackSettings.LoadMsOfficeFallbackSettings.xml");

// 2 - استخدم المخطط المبني من خطوط Google Noto:
fontFallbackSettings.LoadNotoFallbackSettings();
fontFallbackSettings.Save(ArtifactsDir + "FontSettings.FallbackSettings.LoadNotoFallbackSettings.xml");
```

### أنظر أيضا

* class [FontFallbackSettings](../)
* مساحة الاسم [Aspose.Words.Fonts](../../fontfallbacksettings/)
* المجسم [Aspose.Words](../../../)


