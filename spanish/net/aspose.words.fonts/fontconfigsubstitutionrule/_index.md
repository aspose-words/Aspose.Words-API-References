---
title: FontConfigSubstitutionRule Class
linktitle: FontConfigSubstitutionRule
articleTitle: FontConfigSubstitutionRule
second_title: Aspose.Words para .NET
description: Descubra la clase Aspose.Words.Fonts.FontConfigSubstitutionRule para una gestión y personalización de fuentes fluidas en sus documentos. ¡Mejore el estilo de su texto hoy mismo!
type: docs
weight: 3300
url: /es/net/aspose.words.fonts/fontconfigsubstitutionrule/
---
## FontConfigSubstitutionRule class

Regla de sustitución de configuración de fuente.

Para obtener más información, visite el[Trabajar con fuentes](https://docs.aspose.com/words/net/working-with-fonts/) Artículo de documentación.

```csharp
public class FontConfigSubstitutionRule : FontSubstitutionRule
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| override [Enabled](../../aspose.words.fonts/fontconfigsubstitutionrule/enabled/) { set; } | Especifica si la regla está habilitada o no. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [IsFontConfigAvailable](../../aspose.words.fonts/fontconfigsubstitutionrule/isfontconfigavailable/)() | Comprueba si la utilidad fontconfig está disponible o no. |
| [ResetCache](../../aspose.words.fonts/fontconfigsubstitutionrule/resetcache/)() | Restablece el caché de los resultados de las llamadas a fontconfig. |

## Observaciones

Esta regla utiliza la utilidad fontconfig en plataformas Linux (y otras similares a Unix) para obtener la sustitución si la fuente original no está disponible.

Si la utilidad fontconfig no está disponible, esta regla se ignorará.

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

* class [FontSubstitutionRule](../fontsubstitutionrule/)
* espacio de nombres [Aspose.Words.Fonts](../../aspose.words.fonts/)
* asamblea [Aspose.Words](../../)
