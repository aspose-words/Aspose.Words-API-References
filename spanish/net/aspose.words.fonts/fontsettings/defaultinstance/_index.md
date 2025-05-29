---
title: FontSettings.DefaultInstance
linktitle: DefaultInstance
articleTitle: DefaultInstance
second_title: Aspose.Words para .NET
description: Descubre la propiedad FontSettings DefaultInstance para una gestión optimizada de fuentes estáticas. ¡Optimiza tu diseño con configuraciones predeterminadas personalizables!
type: docs
weight: 20
url: /es/net/aspose.words.fonts/fontsettings/defaultinstance/
---
## FontSettings.DefaultInstance property

Configuración de fuente predeterminada estática.

```csharp
public static FontSettings DefaultInstance { get; }
```

## Observaciones

Esta instancia se utiliza de forma predeterminada en un documento a menos que[`FontSettings`](../../../aspose.words/document/fontsettings/) se especifica.

## Ejemplos

Muestra cómo configurar la instancia de configuración de fuente predeterminada.

```csharp
// Configure la instancia de configuración de fuente predeterminada para utilizar la fuente "Courier New"
// como sustituto de respaldo cuando intentamos utilizar una fuente desconocida.
FontSettings.DefaultInstance.SubstitutionSettings.DefaultFontSubstitution.DefaultFontName = "Courier New";

Assert.True(FontSettings.DefaultInstance.SubstitutionSettings.DefaultFontSubstitution.Enabled);

Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Non-existent font";
builder.Write("Hello world!");

Este documento no tiene una configuración de FontSettings. Al renderizar el documento,
// la instancia FontSettings predeterminada resolverá la fuente faltante.
// Aspose.Words utilizará "Courier New" para representar el texto que utiliza la fuente desconocida.
Assert.Null(doc.FontSettings);

doc.Save(ArtifactsDir + "FontSettings.DefaultFontInstance.pdf");
```

Muestra cómo utilizar la interfaz IWarningCallback para monitorear las advertencias de sustitución de fuentes.

```csharp
public void SubstitutionWarning()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Font.Name = "Times New Roman";
    builder.Writeln("Hello world!");

    FontSubstitutionWarningCollector callback = new FontSubstitutionWarningCollector();
    doc.WarningCallback = callback;

    // Almacena la colección actual de fuentes, que será la fuente de fuente predeterminada para cada documento
    // para el cual no especificamos una fuente diferente.
    FontSourceBase[] originalFontSources = FontSettings.DefaultInstance.GetFontsSources();

    // Para fines de prueba, configuraremos Aspose.Words para que busque fuentes solo en una carpeta que no existe.
    FontSettings.DefaultInstance.SetFontsFolder(string.Empty, false);

    //Al renderizar el documento, no habrá lugar para encontrar la fuente "Times New Roman".
    // Esto provocará una advertencia de sustitución de fuente, que nuestra devolución de llamada detectará.
    doc.Save(ArtifactsDir + "FontSettings.SubstitutionWarning.pdf");

    FontSettings.DefaultInstance.SetFontsSources(originalFontSources);

    Assert.True(callback.FontSubstitutionWarnings[0].WarningType == WarningType.FontSubstitution);
    Assert.True(callback.FontSubstitutionWarnings[0].Description
        .Equals(
            "Font 'Times New Roman' has not been found. Using 'Fanwood' font instead. Reason: first available font."));
}

private class FontSubstitutionWarningCollector : IWarningCallback
{
    /// <summary>
    /// Se llama cada vez que ocurre una advertencia durante la carga/guardado.
    /// </summary>
    public void Warning(WarningInfo info)
    {
        if (info.WarningType == WarningType.FontSubstitution)
            FontSubstitutionWarnings.Warning(info);
    }

    public WarningInfoCollection FontSubstitutionWarnings = new WarningInfoCollection();
}
```

### Ver también

* class [FontSettings](../)
* espacio de nombres [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* asamblea [Aspose.Words](../../../)
