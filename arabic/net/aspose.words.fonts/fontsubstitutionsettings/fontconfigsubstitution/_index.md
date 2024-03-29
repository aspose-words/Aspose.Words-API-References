---
title: FontSubstitutionSettings.FontConfigSubstitution
linktitle: FontConfigSubstitution
articleTitle: FontConfigSubstitution
second_title: Aspose.Words لـ .NET
description: FontSubstitutionSettings FontConfigSubstitution ملكية. الإعدادات المتعلقة بقاعدة استبدال تكوين الخط في C#.
type: docs
weight: 20
url: /ar/net/aspose.words.fonts/fontsubstitutionsettings/fontconfigsubstitution/
---
## FontSubstitutionSettings.FontConfigSubstitution property

الإعدادات المتعلقة بقاعدة استبدال تكوين الخط.

```csharp
public FontConfigSubstitutionRule FontConfigSubstitution { get; }
```

## أمثلة

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

* class [FontConfigSubstitutionRule](../../fontconfigsubstitutionrule/)
* class [FontSubstitutionSettings](../)
* مساحة الاسم [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* المجسم [Aspose.Words](../../../)
