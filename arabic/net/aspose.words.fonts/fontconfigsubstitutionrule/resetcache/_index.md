---
title: FontConfigSubstitutionRule.ResetCache
second_title: Aspose.Words لمراجع .NET API
description: FontConfigSubstitutionRule طريقة. إعادة تعيين ذاكرة التخزين المؤقت لنتائج استدعاء Fontconfig.
type: docs
weight: 30
url: /ar/net/aspose.words.fonts/fontconfigsubstitutionrule/resetcache/
---
## FontConfigSubstitutionRule.ResetCache method

إعادة تعيين ذاكرة التخزين المؤقت لنتائج استدعاء Fontconfig.

```csharp
public void ResetCache()
```

### أمثلة

يعرض استبدال تكوين الخط المعتمد على نظام التشغيل.

```csharp
FontSettings fontSettings = new FontSettings();
FontConfigSubstitutionRule fontConfigSubstitution =
    fontSettings.SubstitutionSettings.FontConfigSubstitution;

bool isWindows = new[] {PlatformID.Win32NT, PlatformID.Win32S, PlatformID.Win32Windows, PlatformID.WinCE}
    .Any(p => Environment.OSVersion.Platform == p);

// يعمل كائن FontConfigSubstitutionRule بشكل مختلف على الأنظمة الأساسية التي تعمل بنظام Windows/غير Windows.
// على نظام التشغيل Windows، فهو غير متوفر.
if (isWindows)
{
    Assert.False(fontConfigSubstitution.Enabled);
    Assert.False(fontConfigSubstitution.IsFontConfigAvailable());
}

bool isLinuxOrMac =
    new[] {PlatformID.Unix, PlatformID.MacOSX}.Any(p => Environment.OSVersion.Platform == p);

// على Linux/Mac، سيكون لدينا إمكانية الوصول إليه وسنكون قادرين على تنفيذ العمليات.
if (isLinuxOrMac)
{
    Assert.True(fontConfigSubstitution.Enabled);
    Assert.True(fontConfigSubstitution.IsFontConfigAvailable());

    fontConfigSubstitution.ResetCache();
}
```

### أنظر أيضا

* class [FontConfigSubstitutionRule](../)
* مساحة الاسم [Aspose.Words.Fonts](../../fontconfigsubstitutionrule/)
* المجسم [Aspose.Words](../../../)


