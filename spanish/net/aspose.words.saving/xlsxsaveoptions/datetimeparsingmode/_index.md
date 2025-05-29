---
title: XlsxSaveOptions.DateTimeParsingMode
linktitle: DateTimeParsingMode
articleTitle: DateTimeParsingMode
second_title: Aspose.Words para .NET
description: Descubra la propiedad DateTimeParsingMode de XlsxSaveOptions para personalizar cómo su documento analiza fechas y horas, garantizando una interpretación precisa de los datos.
type: docs
weight: 30
url: /es/net/aspose.words.saving/xlsxsaveoptions/datetimeparsingmode/
---
## XlsxSaveOptions.DateTimeParsingMode property

Obtiene o establece el modo que especifica cómo se analiza el texto del documento para identificar valores de fecha y hora. El valor predeterminado esUseCurrentLocale .

```csharp
public XlsxDateTimeParsingMode DateTimeParsingMode { get; set; }
```

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

* enum [XlsxDateTimeParsingMode](../../xlsxdatetimeparsingmode/)
* class [XlsxSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
