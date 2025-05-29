---
title: ReportBuilderOptions Class
linktitle: ReportBuilderOptions
articleTitle: ReportBuilderOptions
second_title: Aspose.Words für .NET
description: Entdecken Sie die Aspose.Words LowCode ReportBuilderOptions-Klasse, die Ihre Erfahrung mit der LINQ Reporting Engine mit anpassbaren Optionen für die nahtlose Dokumenterstellung verbessern soll.
type: docs
weight: 4380
url: /de/net/aspose.words.lowcode/reportbuilderoptions/
---
## ReportBuilderOptions class

Stellt Optionen für die LINQ Reporting Engine-Funktionalität dar.

```csharp
public class ReportBuilderOptions
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [ReportBuilderOptions](reportbuilderoptions/)() | Default_Constructor |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [KnownTypes](../../aspose.words.lowcode/reportbuilderoptions/knowntypes/) { get; } | Ruft einen ungeordneten Satz (d. h. eine Sammlung eindeutiger Elemente) ab, der enthältType Objekte , deren vollständig oder teilweise qualifizierte Namen in Berichtsvorlagen verwendet werden können, die von dieser Engine -Instanz verarbeitet werden, um die statischen Mitglieder der entsprechenden Typen aufzurufen, Typumwandlungen durchzuführen usw. |
| [MissingMemberMessage](../../aspose.words.lowcode/reportbuilderoptions/missingmembermessage/) { get; set; } | Ruft einen Zeichenfolgenwert ab oder legt ihn fest, der anstelle eines Vorlagenausdrucks ausgegeben wird und einen einfachen Verweis auf ein fehlendes Element eines Objekts darstellt. Der Standardwert ist eine leere Zeichenfolge. |
| [Options](../../aspose.words.lowcode/reportbuilderoptions/options/) { get; set; } | Ruft eine Reihe von Flags ab oder setzt diese, die das Verhalten dieses[`ReportingEngine`](../../aspose.words.reporting/reportingengine/) Instanz beim Erstellen eines Berichts. |

## Beispiele

Zeigt, wie ein Dokument mit Daten gefüllt wird.

```csharp
public void BuildReportData()
{
    // Es gibt mehrere Möglichkeiten, ein Dokument mit Daten zu füllen:
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

### Siehe auch

* namensraum [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../)
