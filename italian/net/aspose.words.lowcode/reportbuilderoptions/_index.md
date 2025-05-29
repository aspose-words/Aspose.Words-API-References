---
title: ReportBuilderOptions Class
linktitle: ReportBuilderOptions
articleTitle: ReportBuilderOptions
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words LowCode ReportBuilderOptions, progettata per migliorare la tua esperienza con LINQ Reporting Engine con opzioni personalizzabili per una generazione di documenti senza interruzioni.
type: docs
weight: 4380
url: /it/net/aspose.words.lowcode/reportbuilderoptions/
---
## ReportBuilderOptions class

Rappresenta le opzioni per la funzionalità LINQ Reporting Engine.

```csharp
public class ReportBuilderOptions
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [ReportBuilderOptions](reportbuilderoptions/)() | Default_Costruttore |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [KnownTypes](../../aspose.words.lowcode/reportbuilderoptions/knowntypes/) { get; } | Ottiene un set non ordinato (ovvero una raccolta di elementi unici) contenenteType oggetti i cui nomi completamente o parzialmente qualificati possono essere utilizzati all'interno dei modelli di report elaborati da questa istanza di engine per richiamare i membri statici dei tipi corrispondenti, eseguire cast di tipo, ecc. |
| [MissingMemberMessage](../../aspose.words.lowcode/reportbuilderoptions/missingmembermessage/) { get; set; } | Ottiene o imposta un valore stringa stampato al posto di un'espressione modello che rappresenta un semplice riferimento a , un membro mancante di un oggetto. Il valore predefinito è una stringa vuota. |
| [Options](../../aspose.words.lowcode/reportbuilderoptions/options/) { get; set; } | Ottiene o imposta un set di flag che controllano il comportamento di questo[`ReportingEngine`](../../aspose.words.reporting/reportingengine/) istanza durante la creazione di un report. |

## Esempi

Mostra come popolare un documento con i dati.

```csharp
public void BuildReportData()
{
    // Esistono diversi modi per popolare un documento con i dati:
    string doc = MyDir + "Reporting engine template - If greedy.docx";

    AsposeData obj = new AsposeData { List = new List<string> { "abc" } };

    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportWithObject.1.docx", obj);
    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportWithObject.2.docx", obj, new ReportBuilderOptions() { Options = ReportBuildOptions.AllowMissingMembers });
    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportWithObject.3.docx", SaveFormat.Docx, obj);
    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportWithObject.4.docx", SaveFormat.Docx, obj, new ReportBuilderOptions() { Options = ReportBuildOptions.AllowMissingMembers });
}

public class AsposeData
{
    public List<string> List { get; set; }
}
```

### Guarda anche

* spazio dei nomi [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../)
