---
title: ReportBuildOptions Enum
linktitle: ReportBuildOptions
articleTitle: ReportBuildOptions
second_title: Aspose.Words per .NET
description: Scopri le opzioni di Aspose.Words ReportingEngine per una creazione efficiente di report. Personalizza i tuoi report con impostazioni flessibili per risultati ottimali.
type: docs
weight: 5460
url: /it/net/aspose.words.reporting/reportbuildoptions/
---
## ReportBuildOptions enumeration

Specifica le opzioni che controllano il comportamento di[`ReportingEngine`](../reportingengine/) durante la creazione di un report.

```csharp
[Flags]
public enum ReportBuildOptions
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| None | `0` | Specifica le opzioni predefinite. |
| AllowMissingMembers | `1` | Specifica che i membri mancanti dell'oggetto devono essere trattati come letterali nulli dal motore. Questa opzione riguarda solo l'accesso ai membri dell'oggetto istanza (ovvero non statici) e ai metodi di estensione. Se questa opzione non è impostata, il motore genera un'eccezione quando rileva un membro mancante dell'oggetto. |
| RemoveEmptyParagraphs | `2` | Specifica che il motore dovrebbe rimuovere i paragrafi che diventano vuoti dopo che i tag della sintassi del modello vengono rimossi o sostituiti con valori vuoti. |
| InlineErrorMessages | `4` | Specifica che il motore deve incorporare i messaggi di errore di sintassi del modello nei documenti di output. Se questa opzione non è impostata, il motore genera un'eccezione quando incontra un errore di sintassi. |
| UseLegacyHeaderFooterVisiting | `8` | Specifica che il motore deve visitare i nodi figlio della sezione (intestazioni, piè di pagina, corpi) in un ordine compatibile con le versioni di Aspose.Words precedenti alla 21.9. |
| RespectJpegExifOrientation | `10` | Specifica che il motore deve utilizzare i valori di orientamento dell'immagine EXIF ​​per ruotare in modo appropriato le immagini JPEG inserite. |
| UpdateFieldsSyntaxAware | `20` | Specifica che il motore deve ignorare la sintassi del modello nei risultati dei campi e aggiornare i campi dopo la creazione di un report . |

### Guarda anche

* spazio dei nomi [Aspose.Words.Reporting](../../aspose.words.reporting/)
* assemblea [Aspose.Words](../../)
