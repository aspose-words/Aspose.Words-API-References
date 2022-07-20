---
title: IWarningCallback
second_title: Referencia de API de Aspose.Words para .NET
description: Implemente esta interfaz si desea que se llame a su propio método personalizado para capturar las advertencias de pérdida de fidelidad que pueden ocurrir durante la carga o el guardado del documento.
type: docs
weight: 3010
url: /es/net/aspose.words/iwarningcallback/
---
## IWarningCallback interface

Implemente esta interfaz si desea que se llame a su propio método personalizado para capturar las advertencias de pérdida de fidelidad que pueden ocurrir durante la carga o el guardado del documento.

```csharp
public interface IWarningCallback
```

## Métodos

| Nombre | Descripción |
| --- | --- |
| [Warning](../../aspose.words/iwarningcallback/warning)(WarningInfo) | Aspose.Words invoca este método cuando encuentra algún problema durante la carga del documento o al guardarlo que podría provocar la pérdida del formato o la fidelidad de los datos. |

### Ejemplos

Muestra cómo usar la interfaz IWarningCallback para monitorear las advertencias de sustitución de fuentes.

```csharp
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Font.Name = "Times New Roman";
    builder.Writeln("Hello world!");

    FontSubstitutionWarningCollector callback = new FontSubstitutionWarningCollector();
    doc.WarningCallback = callback;

    // Almacenar la colección actual de fuentes de fuentes, que será la fuente de fuentes predeterminada para cada documento
    // para el cual no especificamos una fuente de fuente diferente.
    FontSourceBase[] originalFontSources = FontSettings.DefaultInstance.GetFontsSources();

    // Con fines de prueba, configuraremos Aspose.Words para buscar fuentes solo en una carpeta que no existe.
    FontSettings.DefaultInstance.SetFontsFolder(string.Empty, false);

    // Al renderizar el documento, no habrá lugar para encontrar la fuente "Times New Roman".
    // Esto provocará una advertencia de sustitución de fuente, que nuestra devolución de llamada detectará.
    doc.Save(ArtifactsDir + "FontSettings.SubstitutionWarning.pdf");

    FontSettings.DefaultInstance.SetFontsSources(originalFontSources);

    Assert.True(callback.FontSubstitutionWarnings[0].Description
        .Equals(
            "Font 'Times New Roman' has not been found. Using 'Fanwood' font instead. Reason: first available font."));
}

private class FontSubstitutionWarningCollector : IWarningCallback
{
    /// <summary>
    /// Llamado cada vez que ocurre una advertencia durante la carga/guardado.
    /// </summary>
    public void Warning(WarningInfo info)
    {
        if (info.WarningType == WarningType.FontSubstitution)
            FontSubstitutionWarnings.Warning(info);
    }

    public WarningInfoCollection FontSubstitutionWarnings = new WarningInfoCollection();
}
```

Los espectáculos agregaron una alternativa a la representación de mapas de bits y cambiaron el tipo de advertencias sobre registros de metarchivos no admitidos.

```csharp
{
    Document doc = new Document(MyDir + "WMF with image.docx");

    MetafileRenderingOptions metafileRenderingOptions = new MetafileRenderingOptions();

    // Establezca la propiedad "EmulateRasterOperations" en "false" para volver al mapa de bits cuando
    // encuentra un metarchivo, que requerirá operaciones de trama para representar en el PDF de salida.
    metafileRenderingOptions.EmulateRasterOperations = false;

    // Establezca la propiedad "RenderingMode" en "VectorWithFallback" para intentar representar cada metarchivo utilizando gráficos vectoriales.
    metafileRenderingOptions.RenderingMode = MetafileRenderingMode.VectorWithFallback;

    // Crea un objeto "PdfSaveOptions" que podemos pasar al método "Guardar" del documento
    // para modificar cómo ese método convierte el documento a .PDF y aplica la configuración
    // en nuestro objeto MetafileRenderingOptions para la operación de guardado.
    PdfSaveOptions saveOptions = new PdfSaveOptions();
    saveOptions.MetafileRenderingOptions = metafileRenderingOptions;

    HandleDocumentWarnings callback = new HandleDocumentWarnings();
    doc.WarningCallback = callback;

    doc.Save(ArtifactsDir + "PdfSaveOptions.HandleBinaryRasterWarnings.pdf", saveOptions);

    Assert.AreEqual(1, callback.Warnings.Count);
    Assert.AreEqual("'R2_XORPEN' binary raster operation is partly supported.",
        callback.Warnings[0].Description);
}

/// <summary>
/// Imprime y recopila advertencias relacionadas con la pérdida de formato que se producen al guardar un documento.
/// </summary>
public class HandleDocumentWarnings : IWarningCallback
{
    public void Warning(WarningInfo info)
    {
        if (info.WarningType == WarningType.MinorFormattingLoss)
        {
            Console.WriteLine("Unsupported operation: " + info.Description);
            Warnings.Warning(info);
        }
    }

    public WarningInfoCollection Warnings = new WarningInfoCollection();
}
```

Muestra cómo establecer la propiedad para encontrar la coincidencia más cercana para una fuente faltante de las fuentes de fuentes disponibles.

```csharp
[Test]
public void EnableFontSubstitution()
{
    // Abra un documento que contenga texto formateado con una fuente que no existe en ninguna de nuestras fuentes de fuentes.
    Document doc = new Document(MyDir + "Missing font.docx");

    // Asigne una devolución de llamada para manejar las advertencias de sustitución de fuentes.
    HandleDocumentSubstitutionWarnings substitutionWarningHandler = new HandleDocumentSubstitutionWarnings();
    doc.WarningCallback = substitutionWarningHandler;

    // Establecer un nombre de fuente predeterminado y habilitar la sustitución de fuentes.
    FontSettings fontSettings = new FontSettings();
    fontSettings.SubstitutionSettings.DefaultFontSubstitution.DefaultFontName = "Arial";
    ;
    fontSettings.SubstitutionSettings.FontInfoSubstitution.Enabled = true;

    // Obtendremos una advertencia de sustitución de fuente si guardamos un documento al que le falta una fuente.
    doc.FontSettings = fontSettings;
    doc.Save(ArtifactsDir + "FontSettings.EnableFontSubstitution.pdf");

    using (IEnumerator<WarningInfo> warnings = substitutionWarningHandler.FontWarnings.GetEnumerator())
        while (warnings.MoveNext())
            Console.WriteLine(warnings.Current.Description);

    // También podemos verificar las advertencias en la colección y borrarlas.
    Assert.AreEqual(WarningSource.Layout, substitutionWarningHandler.FontWarnings[0].Source);
    Assert.AreEqual(
        "Font '28 Days Later' has not been found. Using 'Calibri' font instead. Reason: alternative name from document.",
        substitutionWarningHandler.FontWarnings[0].Description);

    substitutionWarningHandler.FontWarnings.Clear();

    Assert.That(substitutionWarningHandler.FontWarnings, Is.Empty);
}

public class HandleDocumentSubstitutionWarnings : IWarningCallback
{
    /// <summary>
    /// Llamado cada vez que ocurre una advertencia durante la carga/guardado.
    /// </summary>
    public void Warning(WarningInfo info)
    {
        if (info.WarningType == WarningType.FontSubstitution)
            FontWarnings.Warning(info);
    }

    public WarningInfoCollection FontWarnings = new WarningInfoCollection();
}
```

### Ver también

* espacio de nombres [Aspose.Words](../../aspose.words)
* asamblea [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
