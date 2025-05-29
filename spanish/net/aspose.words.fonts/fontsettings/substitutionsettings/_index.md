---
title: FontSettings.SubstitutionSettings
linktitle: SubstitutionSettings
articleTitle: SubstitutionSettings
second_title: Aspose.Words para .NET
description: Explore la propiedad SubstitutionSettings de FontSettings para optimizar su proceso de sustitución de fuentes y mejorar la calidad de visualización del texto sin esfuerzo.
type: docs
weight: 40
url: /es/net/aspose.words.fonts/fontsettings/substitutionsettings/
---
## FontSettings.SubstitutionSettings property

Configuraciones relacionadas con el mecanismo de sustitución de fuentes.

```csharp
public FontSubstitutionSettings SubstitutionSettings { get; }
```

## Ejemplos

Muestra cómo acceder a la fuente de fuente del sistema de un documento y establecer sustitutos de fuentes.

```csharp
Document doc = new Document();
doc.FontSettings = new FontSettings();

//De forma predeterminada, un documento en blanco siempre contiene una fuente del sistema.
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

// Establezca una fuente que exista en el directorio de fuentes de Windows como sustituto de una que no exista.
doc.FontSettings.SubstitutionSettings.FontInfoSubstitution.Enabled = true;
doc.FontSettings.SubstitutionSettings.TableSubstitution.AddSubstitutes("Kreon-Regular", new[] {"Calibri"});

Assert.AreEqual(1,
    doc.FontSettings.SubstitutionSettings.TableSubstitution.GetSubstitutes("Kreon-Regular").Count());
Assert.Contains("Calibri",
    doc.FontSettings.SubstitutionSettings.TableSubstitution.GetSubstitutes("Kreon-Regular").ToArray());

// Alternativamente, podríamos agregar una carpeta de origen de fuente en la que la carpeta correspondiente contenga la fuente.
FolderFontSource folderFontSource = new FolderFontSource(FontsDir, false);
doc.FontSettings.SetFontsSources(new FontSourceBase[] {systemFontSource, folderFontSource});
Assert.AreEqual(2, doc.FontSettings.GetFontsSources().Length);

// Al restablecer las fuentes de fuentes aún nos queda la fuente de fuente del sistema y nuestros sustitutos.
doc.FontSettings.ResetFontSources();

Assert.AreEqual(1, doc.FontSettings.GetFontsSources().Length);
Assert.AreEqual(FontSourceType.SystemFonts, doc.FontSettings.GetFontsSources()[0].Type);
Assert.AreEqual(1,
    doc.FontSettings.SubstitutionSettings.TableSubstitution.GetSubstitutes("Kreon-Regular").Count());
Assert.True(doc.FontSettings.SubstitutionSettings.FontNameSubstitution.Enabled);
```

### Ver también

* class [FontSubstitutionSettings](../../fontsubstitutionsettings/)
* class [FontSettings](../)
* espacio de nombres [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* asamblea [Aspose.Words](../../../)
