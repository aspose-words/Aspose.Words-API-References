---
title: XlsxDateTimeParsingMode Enum
linktitle: XlsxDateTimeParsingMode
articleTitle: XlsxDateTimeParsingMode
second_title: Aspose.Words per .NET
description: Scopri l'enum XlsxDateTimeParsingMode di Aspose.Words per un'analisi efficiente del testo dei documenti. Identifica facilmente i valori di data e ora nei tuoi file!
type: docs
weight: 6510
url: /it/net/aspose.words.saving/xlsxdatetimeparsingmode/
---
## XlsxDateTimeParsingMode enumeration

Specifica come il testo del documento viene analizzato per identificare i valori di data e ora.

```csharp
public enum XlsxDateTimeParsingMode
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| UseCurrentLocale | `0` | Il formato data/ora impostato per il thread corrente viene utilizzato per primo per analizzare i valori stringa. Se l'analisi fallisce, vengono provati altri formati data/ora comuni. |
| Auto | `1` | Il formato data/ora utilizzato in un documento viene determinato automaticamente. Questa operazione potrebbe richiedere tempo aggiuntivo. |

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

* spazio dei nomi [Aspose.Words.Saving](../../aspose.words.saving/)
* assemblea [Aspose.Words](../../)
