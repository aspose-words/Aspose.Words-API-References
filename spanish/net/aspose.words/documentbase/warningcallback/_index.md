---
title: DocumentBase.WarningCallback
linktitle: WarningCallback
articleTitle: WarningCallback
second_title: Aspose.Words para .NET
description: Descubra la propiedad DocumentBase WarningCallback, vital para garantizar la integridad de los datos durante el procesamiento de documentos al detectar posibles problemas de formato.
type: docs
weight: 100
url: /es/net/aspose.words/documentbase/warningcallback/
---
## DocumentBase.WarningCallback property

Se llama durante varios procedimientos de procesamiento de documentos cuando se detecta un problema que podría resultar en pérdida de fidelidad de datos o formato.

```csharp
public IWarningCallback WarningCallback { get; set; }
```

## Observaciones

El documento puede generar advertencias en cualquier etapa de su existencia, por lo que es importante configurar la devolución de llamada de advertencia lo antes posible para evitar la pérdida de advertencias. Por ejemplo, propiedades como[`PageCount`](../../document/pagecount/) en realidad crea el diseño del documento que se usa más adelante para la representación, y las advertencias de diseño se pueden perder si se especifica la devolución de llamada de advertencia solo para las llamadas de representación posteriores.

## Ejemplos

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

Muestra cómo configurar la propiedad para encontrar la coincidencia más cercana para una fuente faltante entre las fuentes de fuentes disponibles.

```csharp
public void EnableFontSubstitution()
{
    // Abra un documento que contenga texto formateado con una fuente que no existe en ninguna de nuestras fuentes de fuentes.
    Document doc = new Document(MyDir + "Missing font.docx");

    // Asignar una devolución de llamada para manejar advertencias de sustitución de fuentes.
    HandleDocumentSubstitutionWarnings substitutionWarningHandler = new HandleDocumentSubstitutionWarnings();
    doc.WarningCallback = substitutionWarningHandler;

    // Establezca un nombre de fuente predeterminado y habilite la sustitución de fuente.
    FontSettings fontSettings = new FontSettings();
    fontSettings.SubstitutionSettings.DefaultFontSubstitution.DefaultFontName = "Arial";
    ;
    fontSettings.SubstitutionSettings.FontInfoSubstitution.Enabled = true;

    // Las métricas de fuente originales deben utilizarse después de la sustitución de la fuente.
    doc.LayoutOptions.KeepOriginalFontMetrics = true;

    //Recibiremos una advertencia de sustitución de fuente si guardamos un documento con una fuente faltante.
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

    Assert.AreEqual(0, substitutionWarningHandler.FontWarnings.Count);
}

public class HandleDocumentSubstitutionWarnings : IWarningCallback
{
    /// <summary>
    /// Se llama cada vez que ocurre una advertencia durante la carga/guardado.
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

* interface [IWarningCallback](../../iwarningcallback/)
* class [DocumentBase](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
