---
title: FontSubstitutionSettings Class
linktitle: FontSubstitutionSettings
articleTitle: FontSubstitutionSettings
second_title: Aspose.Words para .NET
description: Descubra Aspose.Words.Fonts.FontSubstitutionSettings para una gestión eficiente de fuentes. Optimice la representación de documentos con opciones personalizables de sustitución de fuentes.
type: docs
weight: 3440
url: /es/net/aspose.words.fonts/fontsubstitutionsettings/
---
## FontSubstitutionSettings class

Especifica la configuración del mecanismo de sustitución de fuentes.

Para obtener más información, visite el[Trabajar con fuentes](https://docs.aspose.com/words/net/working-with-fonts/) Artículo de documentación.

```csharp
public class FontSubstitutionSettings
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [DefaultFontSubstitution](../../aspose.words.fonts/fontsubstitutionsettings/defaultfontsubstitution/) { get; } | Configuraciones relacionadas con la regla de sustitución de fuente predeterminada. |
| [FontConfigSubstitution](../../aspose.words.fonts/fontsubstitutionsettings/fontconfigsubstitution/) { get; } | Configuraciones relacionadas con la regla de sustitución de configuración de fuente. |
| [FontInfoSubstitution](../../aspose.words.fonts/fontsubstitutionsettings/fontinfosubstitution/) { get; } | Configuraciones relacionadas con la regla de sustitución de información de fuente. |
| [FontNameSubstitution](../../aspose.words.fonts/fontsubstitutionsettings/fontnamesubstitution/) { get; } | Configuraciones relacionadas con la regla de sustitución del nombre de fuente. |
| [TableSubstitution](../../aspose.words.fonts/fontsubstitutionsettings/tablesubstitution/) { get; } | Configuraciones relacionadas con la regla de sustitución de tablas. |

## Observaciones

El proceso de sustitución de fuentes consta de varias reglas que se comprueban una por una en un orden específico. Si la primera regla no puede resolver la fuente, se comprueba la segunda regla y así sucesivamente.

El orden de las reglas es el siguiente: 1. Regla de sustitución de nombre de fuente (habilitada de forma predeterminada) 2. Regla de sustitución de configuración de fuente (deshabilitada de forma predeterminada) 3. Regla de sustitución de tabla (habilitada de forma predeterminada) 4. Regla de sustitución de información de fuente (habilitada de forma predeterminada) 5. Regla de fuente predeterminada (habilitada de forma predeterminada)

Tenga en cuenta que la regla de sustitución de información de fuente siempre resolverá la fuente si[`FontInfo`](../fontinfo/) Está disponible y anulará la regla de fuente predeterminada. Si desea usar la regla de fuente predeterminada, debe deshabilitar la regla de sustitución de información de fuente .

Tenga en cuenta que la regla de sustitución de configuración de fuente resolverá la fuente en la mayoría de los casos y, por lo tanto, anulará todas las demás reglas.

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

* espacio de nombres [Aspose.Words.Fonts](../../aspose.words.fonts/)
* asamblea [Aspose.Words](../../)
