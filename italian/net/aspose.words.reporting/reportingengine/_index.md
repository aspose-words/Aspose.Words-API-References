---
title: ReportingEngine Class
linktitle: ReportingEngine
articleTitle: ReportingEngine
second_title: Aspose.Words per .NET
description: Sblocca una potente automazione dei documenti con Aspose.Words.ReportingEngine. Popola facilmente i modelli con i dati e personalizza le impostazioni per un reporting impeccabile.
type: docs
weight: 5470
url: /it/net/aspose.words.reporting/reportingengine/
---
## ReportingEngine class

Fornisce routine per popolare i documenti modello con dati e un set di impostazioni per controllare queste routine.

Per saperne di più, visita il[Motore di reporting LINQ](https://docs.aspose.com/words/net/linq-reporting-engine/) articolo di documentazione.

```csharp
public class ReportingEngine
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [ReportingEngine](reportingengine/)() | Inizializza una nuova istanza di questa classe. |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [KnownTypes](../../aspose.words.reporting/reportingengine/knowntypes/) { get; } | Ottiene un set non ordinato (ovvero una raccolta di elementi unici) contenenteType oggetti i cui nomi completamente o parzialmente qualificati possono essere utilizzati all'interno dei modelli di report elaborati da questa istanza di engine per richiamare i membri statici dei tipi corrispondenti, eseguire cast di tipo, ecc. |
| [MissingMemberMessage](../../aspose.words.reporting/reportingengine/missingmembermessage/) { get; set; } | Ottiene o imposta un valore stringa stampato al posto di un'espressione modello che rappresenta un semplice riferimento a , un membro mancante di un oggetto. Il valore predefinito è una stringa vuota. |
| [Options](../../aspose.words.reporting/reportingengine/options/) { get; set; } | Ottiene o imposta un set di flag che controllano il comportamento di questo`ReportingEngine` istanza durante la creazione di un report. |
| static [UseReflectionOptimization](../../aspose.words.reporting/reportingengine/usereflectionoptimization/) { get; set; } | Ottiene o imposta un valore che indica se le invocazioni dei membri di tipo personalizzato eseguite tramite l'API di riflessione sono ottimizzate utilizzando la generazione dinamica di classi o meno. Il valore predefinito è`VERO` . |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [BuildReport](../../aspose.words.reporting/reportingengine/buildreport/#buildreport)(*[Document](../../aspose.words/document/), object*) | Popola il documento modello specificato con dati provenienti dalla fonte specificata, rendendolo un report pronto. |
| [BuildReport](../../aspose.words.reporting/reportingengine/buildreport/#buildreport_1)(*[Document](../../aspose.words/document/), object, string*) | Popola il documento modello specificato con dati provenienti dalla fonte specificata, rendendolo un report pronto. |
| [BuildReport](../../aspose.words.reporting/reportingengine/buildreport/#buildreport_2)(*[Document](../../aspose.words/document/), object[], string[]*) | Popola il documento modello specificato con dati provenienti dalle fonti specificate, rendendolo un report pronto. |
| static [GetRestrictedTypes](../../aspose.words.reporting/reportingengine/getrestrictedtypes/)() | Restituisce i tipi, quali membri e quali membri dei tipi derivati non dovrebbero essere accessibili al motore tramite la sintassi del modello. |
| static [SetRestrictedTypes](../../aspose.words.reporting/reportingengine/setrestrictedtypes/)(*params Type[]*) | Specifica i tipi, quali membri e quali membri dei tipi derivati non devono essere accessibili al motore tramite la sintassi del modello. |

### Guarda anche

* spazio dei nomi [Aspose.Words.Reporting](../../aspose.words.reporting/)
* assemblea [Aspose.Words](../../)
