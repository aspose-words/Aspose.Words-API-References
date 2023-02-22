---
title: FontConfigSubstitutionRule.Enabled
second_title: Aspose.Words für .NET-API-Referenz
description: FontConfigSubstitutionRule eigendom. Gibt an ob die Regel aktiviert ist oder nicht.
type: docs
weight: 10
url: /de/net/aspose.words.fonts/fontconfigsubstitutionrule/enabled/
---
## FontConfigSubstitutionRule.Enabled property

Gibt an, ob die Regel aktiviert ist oder nicht.

```csharp
public override bool Enabled { set; }
```

### Beispiele

Zeigt die vom Betriebssystem abhängige Ersetzung der Schriftartkonfiguration an.

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

// Unter Linux/Mac haben wir Zugriff darauf und können Operationen ausführen.
if (isLinuxOrMac)
{
    Assert.True(fontConfigSubstitution.Enabled);
    Assert.True(fontConfigSubstitution.IsFontConfigAvailable());

    fontConfigSubstitution.ResetCache();
}
```

### Siehe auch

* class [FontConfigSubstitutionRule](../)
* namensraum [Aspose.Words.Fonts](../../fontconfigsubstitutionrule/)
* Montage [Aspose.Words](../../../)


