---
title: IsFontConfigAvailable
second_title: Aspose.Words for .NET API Reference
description: FontConfigSubstitutionRule method. Check if fontconfig utility is available or not in C#.
type: docs
weight: 20
url: /net/aspose.words.fonts/fontconfigsubstitutionrule/isfontconfigavailable/
---
## FontConfigSubstitutionRule.IsFontConfigAvailable method

Check if fontconfig utility is available or not.

```csharp
public bool IsFontConfigAvailable()
```

## Examples

Shows operating system-dependent font config substitution.

```csharp
FontSettings fontSettings = new FontSettings();
FontConfigSubstitutionRule fontConfigSubstitution =
    fontSettings.SubstitutionSettings.FontConfigSubstitution;

bool isWindows = new[] {PlatformID.Win32NT, PlatformID.Win32S, PlatformID.Win32Windows, PlatformID.WinCE}
    .Any(p => Environment.OSVersion.Platform == p);

// The FontConfigSubstitutionRule object works differently on Windows/non-Windows platforms.
// On Windows, it is unavailable.
if (isWindows)
{
    Assert.False(fontConfigSubstitution.Enabled);
    Assert.False(fontConfigSubstitution.IsFontConfigAvailable());
}

bool isLinuxOrMac =
    new[] {PlatformID.Unix, PlatformID.MacOSX}.Any(p => Environment.OSVersion.Platform == p);

// On Linux/Mac, we will have access to it, and will be able to perform operations.
if (isLinuxOrMac)
{
    Assert.True(fontConfigSubstitution.Enabled);
    Assert.True(fontConfigSubstitution.IsFontConfigAvailable());

    fontConfigSubstitution.ResetCache();
}
```

### See Also

* class [FontConfigSubstitutionRule](../)
* namespace [Aspose.Words.Fonts](../../fontconfigsubstitutionrule/)
* assembly [Aspose.Words](../../../)
