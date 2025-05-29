---
title: FontConfigSubstitutionRule.IsFontConfigAvailable
linktitle: IsFontConfigAvailable
articleTitle: IsFontConfigAvailable
second_title: Aspose.Words für .NET
description: Ermitteln Sie mit der Methode IsFontConfigAvailable, ob das Dienstprogramm FontConfig verfügbar ist. Sorgen Sie für optimales Schriftartenmanagement für Ihre Anwendungen.
type: docs
weight: 20
url: /de/net/aspose.words.fonts/fontconfigsubstitutionrule/isfontconfigavailable/
---
## FontConfigSubstitutionRule.IsFontConfigAvailable method

Überprüfen Sie, ob das Dienstprogramm „fontconfig“ verfügbar ist oder nicht.

```csharp
public bool IsFontConfigAvailable()
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

* class [FontConfigSubstitutionRule](../)
* namensraum [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* Montage [Aspose.Words](../../../)
