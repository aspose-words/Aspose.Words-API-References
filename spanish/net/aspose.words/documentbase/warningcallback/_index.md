---
title: WarningCallback
second_title: Referencia de API de Aspose.Words para .NET
description: Llamado durante varios procedimientos de procesamiento de documentos cuando se detecta un problema que podría resultar en datos o pérdida de fidelidad de formato.
type: docs
weight: 90
url: /es/net/aspose.words/documentbase/warningcallback/
---
## DocumentBase.WarningCallback property

Llamado durante varios procedimientos de procesamiento de documentos cuando se detecta un problema que podría resultar en datos o pérdida de fidelidad de formato.

```csharp
public IWarningCallback WarningCallback { get; set; }
```

### Observaciones

El documento puede generar advertencias en cualquier etapa de su existencia, por lo que es importante configurar la devolución de llamada de advertencia lo antes posible para evitar la pérdida de advertencias. Por ejemplo, propiedades tales como[`PageCount`](../../document/pagecount) en realidad crea el diseño del documento que se usa más tarde para la representación, y las advertencias de diseño pueden perderse si se especifica la devolución de llamada de advertencia solo para las llamadas de representación posteriores.

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

* interface [IWarningCallback](../../iwarningcallback)
* class [DocumentBase](../../documentbase)
* espacio de nombres [Aspose.Words](../../documentbase)
* asamblea [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
