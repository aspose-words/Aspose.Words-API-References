---
title: ReportBuilderContext Class
linktitle: ReportBuilderContext
articleTitle: ReportBuilderContext
second_title: Aspose.Words für .NET
description: Entdecken Sie die Aspose.Words LowCode ReportBuilderContext-Klasse für die nahtlose Dokumenterstellung mit der LINQ Reporting Engine. Optimieren Sie Ihren Workflow noch heute.
type: docs
weight: 4370
url: /de/net/aspose.words.lowcode/reportbuildercontext/
---
## ReportBuilderContext class

LINQ Reporting Engine-Kontext.

```csharp
public class ReportBuilderContext : ProcessorContext
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [ReportBuilderContext](reportbuildercontext/)() | Default_Constructor |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [DataSources](../../aspose.words.lowcode/reportbuildercontext/datasources/) { get; } | Zum Erstellen des Berichts verwendete Datenquellen. |
| [FontSettings](../../aspose.words.lowcode/processorcontext/fontsettings/) { get; set; } | Vom Prozessor verwendete Schriftarteinstellungen. |
| [LayoutOptions](../../aspose.words.lowcode/processorcontext/layoutoptions/) { get; } | Vom Prozessor verwendete Dokumentlayoutoptionen. |
| [ReportBuilderOptions](../../aspose.words.lowcode/reportbuildercontext/reportbuilderoptions/) { get; } | Optionen zum Erstellen von Berichten. |
| [WarningCallback](../../aspose.words.lowcode/processorcontext/warningcallback/) { get; set; } | Vom Prozessor verwendeter Warn-Callback. |

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

* class [ProcessorContext](../processorcontext/)
* namensraum [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../)
