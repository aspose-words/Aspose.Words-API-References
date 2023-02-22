---
title: Class WarningInfo
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.WarningInfo clase. Contiene información sobre una advertencia que emitió Aspose.Words durante la carga o el guardado del documento.
type: docs
weight: 6320
url: /es/net/aspose.words/warninginfo/
---
## WarningInfo class

Contiene información sobre una advertencia que emitió Aspose.Words durante la carga o el guardado del documento.

```csharp
public class WarningInfo
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Description](../../aspose.words/warninginfo/description/) { get; } | Devuelve la descripción de la advertencia. |
| [Source](../../aspose.words/warninginfo/source/) { get; } | Devuelve el origen de la advertencia. |
| [WarningType](../../aspose.words/warninginfo/warningtype/) { get; } | Devuelve el tipo de aviso. |

### Observaciones

Usted no crea instancias de esta clase. Los objetos de esta clase se crean y Aspose.Words los pasa al[`Warning`](../iwarningcallback/warning/) método.

### Ejemplos

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

* espacio de nombres [Aspose.Words](../../aspose.words/)
* asamblea [Aspose.Words](../../)


