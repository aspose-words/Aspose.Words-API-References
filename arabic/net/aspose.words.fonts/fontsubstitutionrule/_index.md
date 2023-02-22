---
title: Class FontSubstitutionRule
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Fonts.FontSubstitutionRule فصل. هذه فئة أساسية مجردة لقاعدة استبدال الخط.
type: docs
weight: 2820
url: /ar/net/aspose.words.fonts/fontsubstitutionrule/
---
## FontSubstitutionRule class

هذه فئة أساسية مجردة لقاعدة استبدال الخط.

```csharp
public abstract class FontSubstitutionRule
```

## الخصائص

| اسم | وصف |
| --- | --- |
| virtual [Enabled](../../aspose.words.fonts/fontsubstitutionrule/enabled/) { get; set; } | يحدد ما إذا كانت القاعدة ممكّنة أم لا. |

### أمثلة

يعرض استبدال تكوين الخط المعتمد على نظام التشغيل.

```csharp
FontSettings fontSettings = new FontSettings();
FontConfigSubstitutionRule fontConfigSubstitution =
    fontSettings.SubstitutionSettings.FontConfigSubstitution;

bool isWindows = new[] {PlatformID.Win32NT, PlatformID.Win32S, PlatformID.Win32Windows, PlatformID.WinCE}
    .Any(p => Environment.OSVersion.Platform == p);

// يعمل كائن FontConfigSubstitutionRule بشكل مختلف على أنظمة تشغيل Windows / غير أنظمة تشغيل Windows.
// في Windows ، إنه غير متوفر.
if (isWindows)
{
    Assert.False(fontConfigSubstitution.Enabled);
    Assert.False(fontConfigSubstitution.IsFontConfigAvailable());
}

bool isLinuxOrMac =
    new[] {PlatformID.Unix, PlatformID.MacOSX}.Any(p => Environment.OSVersion.Platform == p);

// في Linux / Mac ، سنتمكن من الوصول إليه ، وسنكون قادرين على إجراء العمليات.
if (isLinuxOrMac)
{
    Assert.True(fontConfigSubstitution.Enabled);
    Assert.True(fontConfigSubstitution.IsFontConfigAvailable());

    fontConfigSubstitution.ResetCache();
}
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Fonts](../../aspose.words.fonts/)
* المجسم [Aspose.Words](../../)


