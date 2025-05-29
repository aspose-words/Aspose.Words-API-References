---
title: WarningType Enum
linktitle: WarningType
articleTitle: WarningType
second_title: Aspose.Words para .NET
description: Descubra la enumeración Aspose.Words.WarningType, que categoriza las advertencias durante la carga o el guardado de documentos, mejorando su experiencia de administración de documentos.
type: docs
weight: 7510
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
| MajorFormattingLossCategory | `FF00` | El documento resultante o una ubicación particular en él podría verse sustancialmente diferente en comparación con el documento original. |
| MajorFormattingLoss | `100` | Pérdida de formato importante genérica, sin código específico. |
| MinorFormattingLossCategory | `FF0000` | El documento resultante o una ubicación particular en él podría verse algo diferente en comparación con el documento original. |
| MinorFormattingLoss | `10000` | Pérdida de formato menor genérica, sin código específico. |
| FontSubstitution | `20000` | La fuente ha sido sustituida. |
| FontEmbedding | `40000` | Pérdida de información de fuente incrustada al guardar el documento. |
| UnexpectedContentCategory | `F000000` | No se pudo reconocer algún contenido en el documento de origen (es decir, no es compatible), esto puede o no causar problemas o resultar en pérdida de datos o formato. |
| UnexpectedContent | `1000000` | Contenido genérico inesperado, sin código específico. |
| Hint | `10000000` | Avisa de un problema potencial o sugiere una mejora. |

## Ejemplos

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

* espacio de nombres [Aspose.Words](../../aspose.words/)
* asamblea [Aspose.Words](../../)
