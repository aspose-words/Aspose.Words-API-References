---
title: FontConfigSubstitutionRule Class
linktitle: FontConfigSubstitutionRule
articleTitle: FontConfigSubstitutionRule
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Fonts.FontConfigSubstitutionRule لإدارة وتخصيص الخطوط بسلاسة في مستنداتك. حسّن تنسيق نصوصك اليوم!
type: docs
weight: 3300
url: /ar/net/aspose.words.fonts/fontconfigsubstitutionrule/
---
## FontConfigSubstitutionRule class

قاعدة استبدال تكوين الخط.

لمعرفة المزيد، قم بزيارة[العمل مع الخطوط](https://docs.aspose.com/words/net/working-with-fonts/) مقالة توثيقية.

```csharp
public class FontConfigSubstitutionRule : FontSubstitutionRule
```

## الخصائص

| اسم | وصف |
| --- | --- |
| override [Enabled](../../aspose.words.fonts/fontconfigsubstitutionrule/enabled/) { set; } | يحدد ما إذا كانت القاعدة ممكّنة أم لا. |

## طُرق

| اسم | وصف |
| --- | --- |
| [IsFontConfigAvailable](../../aspose.words.fonts/fontconfigsubstitutionrule/isfontconfigavailable/)() | تحقق مما إذا كانت أداة fontconfig متاحة أم لا. |
| [ResetCache](../../aspose.words.fonts/fontconfigsubstitutionrule/resetcache/)() | إعادة تعيين ذاكرة التخزين المؤقت لنتائج استدعاء fontconfig. |

## ملاحظات

تستخدم هذه القاعدة أداة fontconfig على أنظمة Linux (وأنظمة أخرى شبيهة بـ Unix) للحصول على substitution إذا لم يكن الخط الأصلي متاحًا.

إذا لم تكن أداة fontconfig متاحة، فسيتم تجاهل هذه القاعدة.

## أمثلة

يعرض استبدال تكوين الخط المعتمد على نظام التشغيل.

```csharp
FontSettings fontSettings = new FontSettings();
FontConfigSubstitutionRule fontConfigSubstitution =
    fontSettings.SubstitutionSettings.FontConfigSubstitution;

bool isWindows = new[] {PlatformID.Win32NT, PlatformID.Win32S, PlatformID.Win32Windows, PlatformID.WinCE}
    .Any(p => Environment.OSVersion.Platform == p);

// يعمل كائن FontConfigSubstitutionRule بشكل مختلف على أنظمة التشغيل Windows/غير Windows.
// على نظام التشغيل Windows، غير متوفر.
if (isWindows)
{
    Assert.False(fontConfigSubstitution.Enabled);
    Assert.False(fontConfigSubstitution.IsFontConfigAvailable());
}

bool isLinuxOrMac =
    new[] {PlatformID.Unix, PlatformID.MacOSX}.Any(p => Environment.OSVersion.Platform == p);

// على Linux/Mac، سيكون لدينا إمكانية الوصول إليه، وسنكون قادرين على إجراء العمليات.
if (isLinuxOrMac)
{
    Assert.True(fontConfigSubstitution.Enabled);
    Assert.True(fontConfigSubstitution.IsFontConfigAvailable());

    fontConfigSubstitution.ResetCache();
}
```

### أنظر أيضا

* class [FontSubstitutionRule](../fontsubstitutionrule/)
* مساحة الاسم [Aspose.Words.Fonts](../../aspose.words.fonts/)
* المجسم [Aspose.Words](../../)
