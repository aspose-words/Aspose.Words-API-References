---
title: FontSettings.SubstitutionSettings
second_title: Referencia de API de Aspose.Words para .NET
description: FontSettings propiedad. Ajustes relacionados con el mecanismo de sustitución de fuentes.
type: docs
weight: 40
url: /es/net/aspose.words.fonts/fontsettings/substitutionsettings/
---
## FontSettings.SubstitutionSettings property

Ajustes relacionados con el mecanismo de sustitución de fuentes.

```csharp
public FontSubstitutionSettings SubstitutionSettings { get; }
```

### Ejemplos

Muestra cómo acceder a la fuente de fuentes del sistema de un documento y establecer fuentes sustitutas.

```csharp
Document doc = new Document();
doc.FontSettings = new FontSettings();

// De forma predeterminada, un documento en blanco siempre contiene una fuente de fuente del sistema.
Assert.AreEqual(1, doc.FontSettings.GetFontsSources().Length);

SystemFontSource systemFontSource = (SystemFontSource) doc.FontSettings.GetFontsSources()[0];
Assert.AreEqual(FontSourceType.SystemFonts, systemFontSource.Type);
Assert.AreEqual(0, systemFontSource.Priority);

PlatformID pid = Environment.OSVersion.Platform;
bool isWindows = (pid == PlatformID.Win32NT) || (pid == PlatformID.Win32S) ||
                 (pid == PlatformID.Win32Windows) || (pid == PlatformID.WinCE);
if (isWindows)
{
    const string fontsPath = @"C:\WINDOWS\Fonts";
    Assert.AreEqual(fontsPath.ToLower(),
        SystemFontSource.GetSystemFontFolders().FirstOrDefault()?.ToLower());
}

foreach (string systemFontFolder in SystemFontSource.GetSystemFontFolders())
{
    Console.WriteLine(systemFontFolder);
}

// Establecer una fuente que existe en el directorio de fuentes de Windows como sustituto de una que no existe.
doc.FontSettings.SubstitutionSettings.FontInfoSubstitution.Enabled = true;
doc.FontSettings.SubstitutionSettings.TableSubstitution.AddSubstitutes("Kreon-Regular", new[] {"Calibri"});

Assert.AreEqual(1,
    doc.FontSettings.SubstitutionSettings.TableSubstitution.GetSubstitutes("Kreon-Regular").Count());
Assert.Contains("Calibri",
    doc.FontSettings.SubstitutionSettings.TableSubstitution.GetSubstitutes("Kreon-Regular").ToArray());

// Alternativamente, podríamos agregar una fuente de fuente de carpeta en la que la carpeta correspondiente contenga la fuente.
FolderFontSource folderFontSource = new FolderFontSource(FontsDir, false);
doc.FontSettings.SetFontsSources(new FontSourceBase[] {systemFontSource, folderFontSource});
Assert.AreEqual(2, doc.FontSettings.GetFontsSources().Length);

// Restablecer las fuentes de fuente aún nos deja con la fuente de fuente del sistema, así como con nuestros sustitutos.
doc.FontSettings.ResetFontSources();

Assert.AreEqual(1, doc.FontSettings.GetFontsSources().Length);
Assert.AreEqual(FontSourceType.SystemFonts, doc.FontSettings.GetFontsSources()[0].Type);
Assert.AreEqual(1,
    doc.FontSettings.SubstitutionSettings.TableSubstitution.GetSubstitutes("Kreon-Regular").Count());
```

### Ver también

* class [FontSubstitutionSettings](../../fontsubstitutionsettings/)
* class [FontSettings](../)
* espacio de nombres [Aspose.Words.Fonts](../../fontsettings/)
* asamblea [Aspose.Words](../../../)


