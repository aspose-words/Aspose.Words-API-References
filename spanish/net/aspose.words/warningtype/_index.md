---
title: WarningType Enum
linktitle: WarningType
articleTitle: WarningType
second_title: Aspose.Words para .NET
description: Aspose.Words.WarningType enumeración. Especifica el tipo de advertencia que emite Aspose.Words durante la carga o el guardado del documento en C#.
type: docs
weight: 6660
url: /es/net/aspose.words/warningtype/
---
## WarningType enumeration

Especifica el tipo de advertencia que emite Aspose.Words durante la carga o el guardado del documento.

```csharp
[Flags]
public enum WarningType
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| DataLossCategory | `FF` | Faltarán algunos textos, caracteres, imágenes u otros datos en el árbol del documento después de la carga, o en el documento creado después de guardar. |
| DataLoss | `1` | Pérdida de datos genérica, sin código específico. |
| MajorFormattingLossCategory | `FF00` | El documento resultante o una ubicación particular en él puede verse sustancialmente diferente en comparación con el documento original. |
| MajorFormattingLoss | `100` | Pérdida de formato importante genérica, sin código específico. |
| MinorFormattingLossCategory | `FF0000` | El documento resultante o una ubicación particular en él puede verse algo diferente en comparación con el documento original. |
| MinorFormattingLoss | `10000` | Pérdida de formato menor genérica, sin código específico. |
| FontSubstitution | `20000` | Se ha sustituido la fuente. |
| FontEmbedding | `40000` | Pérdida de información de fuente incrustada durante el guardado del documento. |
| UnexpectedContentCategory | `F000000` | Parte del contenido del documento fuente no se pudo reconocer (es decir, no es compatible), esto puede o no causar problemas o provocar pérdida de datos/formato. |
| UnexpectedContent | `1000000` | Contenido inesperado genérico, sin código específico. |
| Hint | `10000000` | Advierte de un problema potencial o sugiere una mejora. |

## Ejemplos

Muestra cómo configurar la propiedad para encontrar la coincidencia más cercana para una fuente faltante entre las fuentes de fuentes disponibles.

```csharp
public void EnableFontSubstitution()
{
    // Abra un documento que contenga texto formateado con una fuente que no existe en ninguna de nuestras fuentes de fuentes.
    Document doc = new Document(MyDir + "Missing font.docx");

    // Asigna una devolución de llamada para manejar las advertencias de sustitución de fuentes.
    HandleDocumentSubstitutionWarnings substitutionWarningHandler = new HandleDocumentSubstitutionWarnings();
    doc.WarningCallback = substitutionWarningHandler;

    // Establece un nombre de fuente predeterminado y habilita la sustitución de fuentes.
    FontSettings fontSettings = new FontSettings();
    fontSettings.SubstitutionSettings.DefaultFontSubstitution.DefaultFontName = "Arial";
    ;
    fontSettings.SubstitutionSettings.FontInfoSubstitution.Enabled = true;

    // Las métricas de fuente originales deben usarse después de la sustitución de fuentes.
    doc.LayoutOptions.KeepOriginalFontMetrics = true;

    // Recibiremos una advertencia de sustitución de fuente si guardamos un documento al que le falta una fuente.
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

* espacio de nombres [Aspose.Words](../../aspose.words/)
* asamblea [Aspose.Words](../../)
