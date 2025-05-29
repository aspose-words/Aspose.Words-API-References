---
title: FontFallbackSettings.LoadNotoFallbackSettings
linktitle: LoadNotoFallbackSettings
articleTitle: LoadNotoFallbackSettings
second_title: Aspose.Words لـ .NET
description: اكتشف كيفية تحسين أسلوب الطباعة لديك باستخدام طريقة FontFallbackSettings LoadNotoFallbackSettings، باستخدام خطوط Google Noto لعرض نص سلس.
type: docs
weight: 40
url: /ar/net/aspose.words.fonts/fontfallbacksettings/loadnotofallbacksettings/
---
## FontFallbackSettings.LoadNotoFallbackSettings method

يقوم بتحميل إعدادات احتياطية محددة مسبقًا والتي تستخدم خطوط Google Noto.

```csharp
public void LoadNotoFallbackSettings()
```

## أمثلة

يوضح كيفية إضافة إعدادات الخطوط الاحتياطية المحددة مسبقًا لخطوط Google Noto.

```csharp
FontSettings fontSettings = new FontSettings();

// هذه الخطوط مجانية ومرخصة بموجب ترخيص SIL Open Font.
//يمكننا تنزيل الخطوط هنا:
// https://www.google.com/get/noto/#sans-lgc
fontSettings.SetFontsFolder(FontsDir + "Noto", false);

 // لاحظ أن الإعدادات المحددة مسبقًا تستخدم فقط خطوط Noto من نوع Sans ذات الوزن العادي.
//تستخدم بعض خطوط Noto ميزات الطباعة المتقدمة.
// قد لا يتم عرض الخطوط التي تتميز بالطباعة المتقدمة بشكل صحيح لأن Aspose.Words لا يدعمها حاليًا.
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
