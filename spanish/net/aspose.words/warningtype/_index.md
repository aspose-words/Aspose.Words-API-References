---
title: Enum WarningType
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.WarningType enumeración. Especifica el tipo de advertencia que emite Aspose.Words durante la carga o el guardado del documento.
type: docs
weight: 6350
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
| DataLossCategory | `FF` | Faltará algún texto/caracter/imagen u otros datos del árbol del documento después de la carga, o del documento creado después de guardar. |
| DataLoss | `1` | Pérdida de datos genéricos, sin código específico. |
| MajorFormattingLossCategory | `FF00` | El documento resultante o una ubicación particular en él puede verse sustancialmente diferente en comparación con el documento original. |
| MajorFormattingLoss | `100` | Pérdida de formato mayor genérica, sin código específico. |
| MinorFormattingLossCategory | `FF0000` | El documento resultante o una ubicación particular en él puede verse algo diferente en comparación con el documento original. |
| MinorFormattingLoss | `10000` | Pérdida de formato menor genérico, sin código específico. |
| FontSubstitution | `20000` | Se ha sustituido la fuente. |
| FontEmbedding | `40000` | Pérdida de información de fuente incrustada durante el guardado del documento. |
| UnexpectedContentCategory | `F000000` | Parte del contenido del documento de origen no se pudo reconocer (es decir, no es compatible), esto puede o no causar problemas o provocar la pérdida de datos/formato. |
| UnexpectedContent | `1000000` | Contenido inesperado genérico, sin código específico. |
| Hint | `10000000` | Avisa de un problema potencial o sugiere una mejora. |

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


