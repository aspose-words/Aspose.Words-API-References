---
title: FontSubstitutionSettings.FontConfigSubstitution
linktitle: FontConfigSubstitution
articleTitle: FontConfigSubstitution
second_title: Aspose.Words für .NET
description: Entdecken Sie FontSubstitutionSettings für eine optimierte Schriftkonfiguration. Entdecken Sie, wie Sie die Typografie mit effektiven Substitutionsregeln für ein besseres Design verbessern.
type: docs
weight: 20
url: /de/net/aspose.words.fonts/fontsubstitutionsettings/fontconfigsubstitution/
---
## FontSubstitutionSettings.FontConfigSubstitution property

Einstellungen im Zusammenhang mit der Schriftarten-Ersetzungsregel.

```csharp
public FontConfigSubstitutionRule FontConfigSubstitution { get; }
```

## Beispiele

Zeigt die betriebssystemabhängige Schriftartkonfigurationsersetzung an.

```csharp
FontSettings fontSettings = new FontSettings();
FontConfigSubstitutionRule fontConfigSubstitution =
    fontSettings.SubstitutionSettings.FontConfigSubstitution;

bool isWindows = new[] {PlatformID.Win32NT, PlatformID.Win32S, PlatformID.Win32Windows, PlatformID.WinCE}
    .Any(p => Environment.OSVersion.Platform == p);

// Das FontConfigSubstitutionRule-Objekt funktioniert auf Windows-/Nicht-Windows-Plattformen unterschiedlich.
// Unter Windows ist es nicht verfügbar.
if (isWindows)
{
    Assert.False(fontConfigSubstitution.Enabled);
    Assert.False(fontConfigSubstitution.IsFontConfigAvailable());
}

bool isLinuxOrMac =
    new[] {PlatformID.Unix, PlatformID.MacOSX}.Any(p => Environment.OSVersion.Platform == p);

// Unter Linux/Mac haben wir Zugriff darauf und können Vorgänge ausführen.
if (isLinuxOrMac)
{
    Assert.True(fontConfigSubstitution.Enabled);
    Assert.True(fontConfigSubstitution.IsFontConfigAvailable());

    fontConfigSubstitution.ResetCache();
}
```

### Siehe auch

* class [FontConfigSubstitutionRule](../../fontconfigsubstitutionrule/)
* class [FontSubstitutionSettings](../)
* namensraum [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* Montage [Aspose.Words](../../../)
