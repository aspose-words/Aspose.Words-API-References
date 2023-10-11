---
title: FontFallbackSettings.LoadMsOfficeFallbackSettings
second_title: Aspose.Words لمراجع .NET API
description: FontFallbackSettings طريقة. يقوم بتحميل الإعدادات الاحتياطية المحددة مسبقًا والتي تحاكي الإجراء الاحتياطي لـ Microsoft Word وتستخدم خطوط Microsoft Office.
type: docs
weight: 30
url: /ar/net/aspose.words.fonts/fontfallbacksettings/loadmsofficefallbacksettings/
---
## FontFallbackSettings.LoadMsOfficeFallbackSettings method

يقوم بتحميل الإعدادات الاحتياطية المحددة مسبقًا والتي تحاكي الإجراء الاحتياطي لـ Microsoft Word وتستخدم خطوط Microsoft Office.

```csharp
public void LoadMsOfficeFallbackSettings()
```

### أمثلة

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


