---
title: ReportBuilder.Create
linktitle: Create
articleTitle: Create
second_title: Aspose.Words per .NET
description: Crea report efficaci senza sforzo con il metodo Create di ReportBuilder, progettato per semplificare il processo di generazione dei report e aumentare la produttività.
type: docs
weight: 10
url: /it/net/aspose.words.lowcode/reportbuilder/create/
---
## Create() {#create}

Crea una nuova istanza del processore del generatore di report.

```csharp
public static ReportBuilder Create()
```

### Guarda anche

* class [ReportBuilder](../)
* spazio dei nomi [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../../)

---

## Create(*[ReportBuilderContext](../../reportbuildercontext/)*) {#create_1}

Crea una nuova istanza del processore del generatore di report.

```csharp
public static ReportBuilder Create(ReportBuilderContext context)
```

## Esempi

Mostra come popolare un documento con origini dati utilizzando documenti provenienti dal flusso.

```csharp
// Esistono diversi modi per popolare un documento con origini dati utilizzando documenti dal flusso:
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

Mostra come popolare un documento con origini dati.

```csharp
public void BuildReportDataSource()
{
    // Esistono diversi modi per popolare un documento con le origini dati:
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

### Guarda anche

* class [ReportBuilderContext](../../reportbuildercontext/)
* class [ReportBuilder](../)
* spazio dei nomi [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../../)
