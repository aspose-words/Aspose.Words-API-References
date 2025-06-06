---
title: FontSubstitutionSettings.FontConfigSubstitution
linktitle: FontConfigSubstitution
articleTitle: FontConfigSubstitution
second_title: Aspose.Words para .NET
description: Explora FontSubstitutionSettings para optimizar la configuración de fuentes. Descubre cómo optimizar la tipografía con reglas de sustitución efectivas para un mejor diseño.
type: docs
weight: 20
url: /es/net/aspose.words.fonts/fontsubstitutionsettings/fontconfigsubstitution/
---
## FontSubstitutionSettings.FontConfigSubstitution property

Configuraciones relacionadas con la regla de sustitución de configuración de fuente.

```csharp
public FontConfigSubstitutionRule FontConfigSubstitution { get; }
```

## Ejemplos

Muestra la sustitución de configuración de fuentes dependiente del sistema operativo.

```csharp
FontSettings fontSettings = new FontSettings();
FontConfigSubstitutionRule fontConfigSubstitution =
    fontSettings.SubstitutionSettings.FontConfigSubstitution;

bool isWindows = new[] {PlatformID.Win32NT, PlatformID.Win32S, PlatformID.Win32Windows, PlatformID.WinCE}
    .Any(p => Environment.OSVersion.Platform == p);

// El objeto FontConfigSubstitutionRule funciona de manera diferente en plataformas Windows y no Windows.
// En Windows, no está disponible.
if (isWindows)
{
    Assert.False(fontConfigSubstitution.Enabled);
    Assert.False(fontConfigSubstitution.IsFontConfigAvailable());
}

bool isLinuxOrMac =
    new[] {PlatformID.Unix, PlatformID.MacOSX}.Any(p => Environment.OSVersion.Platform == p);

// En Linux/Mac, tendremos acceso a él y podremos realizar operaciones.
if (isLinuxOrMac)
{
    Assert.True(fontConfigSubstitution.Enabled);
    Assert.True(fontConfigSubstitution.IsFontConfigAvailable());

    fontConfigSubstitution.ResetCache();
}
```

### Ver también

* class [FontConfigSubstitutionRule](../../fontconfigsubstitutionrule/)
* class [FontSubstitutionSettings](../)
* espacio de nombres [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* asamblea [Aspose.Words](../../../)
