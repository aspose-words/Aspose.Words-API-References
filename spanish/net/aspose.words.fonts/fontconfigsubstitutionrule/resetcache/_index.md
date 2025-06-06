---
title: FontConfigSubstitutionRule.ResetCache
linktitle: ResetCache
articleTitle: ResetCache
second_title: Aspose.Words para .NET
description: Optimice la gestión de fuentes con el método FontConfigSubstitutionRule ResetCache. Borre fácilmente los resultados de fontconfig para un mejor rendimiento.
type: docs
weight: 30
url: /es/net/aspose.words.fonts/fontconfigsubstitutionrule/resetcache/
---
## FontConfigSubstitutionRule.ResetCache method

Restablece el caché de los resultados de las llamadas a fontconfig.

```csharp
public void ResetCache()
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

* class [FontConfigSubstitutionRule](../)
* espacio de nombres [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* asamblea [Aspose.Words](../../../)
