---
title: FontConfigSubstitutionRule.IsFontConfigAvailable
linktitle: IsFontConfigAvailable
articleTitle: IsFontConfigAvailable
second_title: Aspose.Words for .NET
description: Discover if the FontConfig utility is available with the IsFontConfigAvailable method. Ensure optimal font management for your applications.
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
    Assert.That(fontConfigSubstitution.Enabled, Is.False);
    Assert.That(fontConfigSubstitution.IsFontConfigAvailable(), Is.False);
}

bool isLinuxOrMac =
    new[] {PlatformID.Unix, PlatformID.MacOSX}.Any(p => Environment.OSVersion.Platform == p);

// On Linux/Mac, we will have access to it, and will be able to perform operations.
if (isLinuxOrMac)
{
    Assert.That(fontConfigSubstitution.Enabled, Is.True);
    Assert.That(fontConfigSubstitution.IsFontConfigAvailable(), Is.True);

    fontConfigSubstitution.ResetCache();
}
```

### See Also

* class [FontConfigSubstitutionRule](../)
* namespace [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* assembly [Aspose.Words](../../../)
