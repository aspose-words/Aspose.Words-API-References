---
title: XlsxDateTimeParsingMode Enum
linktitle: XlsxDateTimeParsingMode
articleTitle: XlsxDateTimeParsingMode
second_title: Aspose.Words para .NET
description: Descubra la enumeración XlsxDateTimeParsingMode de Aspose.Words para un análisis eficiente del texto de sus documentos. ¡Identifique fácilmente los valores de fecha y hora en sus archivos!
type: docs
weight: 6510
url: /es/net/aspose.words.saving/xlsxdatetimeparsingmode/
---
## XlsxDateTimeParsingMode enumeration

Especifica cómo se analiza el texto del documento para identificar los valores de fecha y hora.

```csharp
public enum XlsxDateTimeParsingMode
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| UseCurrentLocale | `0` | El formato de fecha y hora establecido para el hilo actual se utiliza primero para analizar los valores de cadena. Si el análisis falla, se prueban otros formatos de fecha y hora comunes. |
| Auto | `1` | El formato de fecha y hora de un documento se determina automáticamente. Esto puede tardar más tiempo. |

## Ejemplos

Muestra cómo especificar la detección automática del formato de fecha y hora.

```csharp
Document doc = new Document(MyDir + "Xlsx DateTime.docx");

XlsxSaveOptions saveOptions = new XlsxSaveOptions();
// Especifique el uso de la detección automática del formato de fecha y hora.
saveOptions.DateTimeParsingMode = XlsxDateTimeParsingMode.Auto;

doc.Save(ArtifactsDir + "XlsxSaveOptions.DateTimeParsingMode.xlsx", saveOptions);
```

### Ver también

* espacio de nombres [Aspose.Words.Saving](../../aspose.words.saving/)
* asamblea [Aspose.Words](../../)
