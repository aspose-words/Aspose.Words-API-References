---
title: ReportBuilder.BuildReportToImages
linktitle: BuildReportToImages
articleTitle: BuildReportToImages
second_title: Aspose.Words für .NET
description: Transformieren Sie Ihre Vorlagendokumente mühelos mit der BuildReportToImages-Methode von ReportBuilder und kombinieren Sie Daten aus verschiedenen Quellen zu beeindruckenden Bildern.
type: docs
weight: 30
url: /de/net/aspose.words.lowcode/reportbuilder/buildreporttoimages/
---
## BuildReportToImages(*string, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), object[], string[], [ReportBuilderOptions](../../reportbuilderoptions/)*) {#buildreporttoimages_1}

Füllt das Vorlagendokument mit Daten aus mehreren Quellen. Rendert die Ausgabe in Bilder.

```csharp
public static Stream[] BuildReportToImages(string inputFileName, ImageSaveOptions saveOptions, 
    object[] data, string[] dataSourceNames, ReportBuilderOptions reportBuilderOptions = null)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFileName | String | Der Name der Eingabedatei. |
| saveOptions | ImageSaveOptions | Die Speicheroptionen der Ausgabe. |
| data | Object[] | Ein Array von Datenquellenobjekten. |
| dataSourceNames | String[] | Ein Array von Namen zum Verweisen auf die Datenquellenobjekte innerhalb der Vorlage. |
| reportBuilderOptions | ReportBuilderOptions | Zusätzliche Optionen zum Erstellen von Berichten. |

## Beispiele

Zeigt, wie ein Dokument mit Datenquellen gefüllt wird.

```csharp
public void BuildReportDataSource()
{
    // Es gibt mehrere Möglichkeiten, ein Dokument mit Datenquellen zu füllen:
    string doc = MyDir + "Report building.docx";

    MessageTestClass sender = new MessageTestClass("LINQ Reporting Engine", "Hello World");

    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportDataSource.1.docx", sender, "s");
    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportDataSource.2.docx", new object[] { sender }, new[] { "s" });
    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportDataSource.3.docx", sender, "s", new ReportBuilderOptions() { Options = ReportBuildOptions.AllowMissingMembers });
    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportDataSource.4.docx", SaveFormat.Docx, sender, "s");
    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportDataSource.5.docx", SaveFormat.Docx, new object[] { sender }, new[] { "s" });
    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportDataSource.6.docx", SaveFormat.Docx, sender, "s", new ReportBuilderOptions() { Options = ReportBuildOptions.AllowMissingMembers });
    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportDataSource.7.docx", SaveFormat.Docx, new object[] { sender }, new[] { "s" }, new ReportBuilderOptions() { Options = ReportBuildOptions.AllowMissingMembers });
    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportDataSource.8.docx", new object[] { sender }, new[] { "s" }, new ReportBuilderOptions() { Options = ReportBuildOptions.AllowMissingMembers });

    Stream[] images = ReportBuilder.BuildReportToImages(doc, new ImageSaveOptions(SaveFormat.Png), new object[] { sender }, new[] { "s" }, new ReportBuilderOptions() { Options = ReportBuildOptions.AllowMissingMembers });

    ReportBuilderContext reportBuilderContext = new ReportBuilderContext();
    reportBuilderContext.ReportBuilderOptions.MissingMemberMessage = "Missed members";
    reportBuilderContext.DataSources.Add(sender, "s");

    ReportBuilder.Create(reportBuilderContext)
        .From(doc)
        .To(ArtifactsDir + "LowCode.BuildReportDataSource.9.docx")
        .Execute();
}

public class MessageTestClass
{
    public string Name { get; set; }
    public string Message { get; set; }

    public MessageTestClass(string name, string message)
    {
        Name = name;
        Message = message;
    }
}
```

### Siehe auch

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [ReportBuilderOptions](../../reportbuilderoptions/)
* class [ReportBuilder](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)

---

## BuildReportToImages(*Stream, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), object[], string[], [ReportBuilderOptions](../../reportbuilderoptions/)*) {#buildreporttoimages}

Füllt das Vorlagendokument mit Daten aus mehreren Quellen. Rendert die Ausgabe in Bilder.

```csharp
public static Stream[] BuildReportToImages(Stream inputStream, ImageSaveOptions saveOptions, 
    object[] data, string[] dataSourceNames, ReportBuilderOptions reportBuilderOptions = null)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputStream | Stream | Der Eingabedateistream. |
| saveOptions | ImageSaveOptions | Die Speicheroptionen der Ausgabe. |
| data | Object[] | Ein Array von Datenquellenobjekten. |
| dataSourceNames | String[] | Ein Array von Namen zum Verweisen auf die Datenquellenobjekte innerhalb der Vorlage. |
| reportBuilderOptions | ReportBuilderOptions | Zusätzliche Optionen zum Erstellen von Berichten. |

## Beispiele

Zeigt, wie Dokumente mithilfe von Dokumenten aus dem Stream mit Datenquellen gefüllt werden.

```csharp
// Es gibt mehrere Möglichkeiten, Dokumente mit Datenquellen zu füllen, indem Dokumente aus dem Stream verwendet werden:
MessageTestClass sender = new MessageTestClass("LINQ Reporting Engine", "Hello World");

using (FileStream streamIn = new FileStream(MyDir + "Report building.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.BuildReportDataSourceStream.1.docx", FileMode.Create, FileAccess.ReadWrite))
        ReportBuilder.BuildReport(streamIn, streamOut, SaveFormat.Docx, new object[] { sender }, new[] { "s" });

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.BuildReportDataSourceStream.2.docx", FileMode.Create, FileAccess.ReadWrite))
        ReportBuilder.BuildReport(streamIn, streamOut, SaveFormat.Docx, sender, "s");

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.BuildReportDataSourceStream.3.docx", FileMode.Create, FileAccess.ReadWrite))
        ReportBuilder.BuildReport(streamIn, streamOut, SaveFormat.Docx, sender, "s", new ReportBuilderOptions() { Options = ReportBuildOptions.AllowMissingMembers });

    Stream[] images = ReportBuilder.BuildReportToImages(streamIn, new ImageSaveOptions(SaveFormat.Png), new object[] { sender }, new[] { "s" }, new ReportBuilderOptions() { Options = ReportBuildOptions.AllowMissingMembers });

    ReportBuilderContext reportBuilderContext = new ReportBuilderContext();
    reportBuilderContext.ReportBuilderOptions.MissingMemberMessage = "Missed members";
    reportBuilderContext.DataSources.Add(sender, "s");

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.BuildReportDataSourceStream.4.docx", FileMode.Create, FileAccess.ReadWrite))
        ReportBuilder.Create(reportBuilderContext)
            .From(streamIn)
            .To(streamOut, SaveFormat.Docx)
            .Execute();
}
```

### Siehe auch

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [ReportBuilderOptions](../../reportbuilderoptions/)
* class [ReportBuilder](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)
