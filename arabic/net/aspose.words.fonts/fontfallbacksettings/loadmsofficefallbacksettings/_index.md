---
title: FontFallbackSettings.LoadMsOfficeFallbackSettings
linktitle: LoadMsOfficeFallbackSettings
articleTitle: LoadMsOfficeFallbackSettings
second_title: Aspose.Words لـ .NET
description: اكتشف طريقة FontFallbackSettings LoadMsOfficeFallbackSettings لتنفيذ إعدادات احتياطية مثل Microsoft Word بسهولة مع خطوط Office لتحقيق التكامل السلس.
type: docs
weight: 30
url: /ar/net/aspose.words.fonts/fontfallbacksettings/loadmsofficefallbacksettings/
---
## FontFallbackSettings.LoadMsOfficeFallbackSettings method

يقوم بتحميل إعدادات احتياطية محددة مسبقًا والتي تحاكي إعدادات Microsoft Word الاحتياطية وتستخدم خطوط Microsoft Office.

```csharp
public void LoadMsOfficeFallbackSettings()
```

## أمثلة

يوضح كيفية تحميل إعدادات الخط الاحتياطي المحددة مسبقًا.

```csharp
Document doc = new Document();

FontSettings fontSettings = new FontSettings();
doc.FontSettings = fontSettings;
FontFallbackSettings fontFallbackSettings = fontSettings.FallbackSettings;

// احفظ مخطط الخط الاحتياطي الافتراضي في مستند XML.
// على سبيل المثال، يحتوي أحد العناصر على قيمة "0C00-0C7F" لـ Range وقيمة "Vani" المقابلة لـ FallbackFonts.
// وهذا يعني أنه إذا كان الخط الذي يستخدمه بعض النصوص لا يحتوي على رموز لكتلة Unicode 0x0C00-0x0C7F،
// سوف يستخدم مخطط العودة رموزًا من الخط البديل "Vani".
fontFallbackSettings.Save(ArtifactsDir + "FontSettings.FallbackSettings.Default.xml");

// فيما يلي مخططان احتياطيان للخطوط محددان مسبقًا يمكننا الاختيار من بينهما.
// 1 - استخدم مخطط Microsoft Office الافتراضي، وهو نفس المخطط الافتراضي:
fontFallbackSettings.LoadMsOfficeFallbackSettings();
fontFallbackSettings.Save(ArtifactsDir + "FontSettings.FallbackSettings.LoadMsOfficeFallbackSettings.xml");

// 2 - استخدم المخطط المبني من خطوط Google Noto:
fontFallbackSettings.LoadNotoFallbackSettings();
fontFallbackSettings.Save(ArtifactsDir + "FontSettings.FallbackSettings.LoadNotoFallbackSettings.xml");
```

### أنظر أيضا

* class [FontFallbackSettings](../)
* مساحة الاسم [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* المجسم [Aspose.Words](../../../)
