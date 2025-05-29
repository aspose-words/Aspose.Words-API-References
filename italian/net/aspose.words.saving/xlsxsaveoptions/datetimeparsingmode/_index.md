---
title: XlsxSaveOptions.DateTimeParsingMode
linktitle: DateTimeParsingMode
articleTitle: DateTimeParsingMode
second_title: Aspose.Words per .NET
description: Scopri la proprietà DateTimeParsingMode di XlsxSaveOptions per personalizzare il modo in cui il tuo documento analizza date e ore, garantendo un'interpretazione accurata dei dati.
type: docs
weight: 30
url: /it/net/aspose.words.saving/xlsxsaveoptions/datetimeparsingmode/
---
## XlsxSaveOptions.DateTimeParsingMode property

Ottiene o imposta la modalità che specifica come il testo del documento viene analizzato per identificare i valori di data e ora. Il valore predefinito èUseCurrentLocale .

```csharp
public XlsxDateTimeParsingMode DateTimeParsingMode { get; set; }
```

## Esempi

Mostra come specificare il rilevamento automatico del formato data/ora.

```csharp
Document doc = new Document(MyDir + "Xlsx DateTime.docx");

XlsxSaveOptions saveOptions = new XlsxSaveOptions();
// Specificare l'utilizzo del rilevamento automatico del formato data/ora.
saveOptions.DateTimeParsingMode = XlsxDateTimeParsingMode.Auto;

doc.Save(ArtifactsDir + "XlsxSaveOptions.DateTimeParsingMode.xlsx", saveOptions);
```

### Guarda anche

* enum [XlsxDateTimeParsingMode](../../xlsxdatetimeparsingmode/)
* class [XlsxSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
