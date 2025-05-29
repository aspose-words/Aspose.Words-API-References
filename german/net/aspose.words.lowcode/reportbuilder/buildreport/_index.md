---
title: ReportBuilder.BuildReport
linktitle: BuildReport
articleTitle: BuildReport
second_title: Aspose.Words für .NET
description: Erstellen Sie mühelos benutzerdefinierte Berichte mit der BuildReport-Methode von ReportBuilder und füllen Sie Ihre Vorlage mit Daten, um jedes Mal professionelle Ergebnisse zu erzielen.
type: docs
weight: 20
url: /de/net/aspose.words.lowcode/reportbuilder/buildreport/
---
## BuildReport(*string, string, object, [ReportBuilderOptions](../../reportbuilderoptions/)*) {#buildreport_12}

Füllt das Vorlagendokument mit Daten aus der angegebenen Quelle und generiert einen vollständigen Bericht mit zusätzlichen Optionen.

```csharp
public static void BuildReport(string inputFileName, string outputFileName, object data, 
    ReportBuilderOptions reportBuilderOptions = null)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFileName | String | Der Name der Eingabedatei. |
| outputFileName | String | Der Name der Ausgabedatei. |
| data | Object | Ein Datenquellenobjekt. |
| reportBuilderOptions | ReportBuilderOptions | Zusätzliche Optionen zum Erstellen von Berichten. |

## Bemerkungen

Wenn das Ausgabeformat ein Bild (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP) ist, wird jede Seite der Ausgabe als separate Datei gespeichert. Der angegebene Ausgabedateiname wird verwendet, um Dateinamen für jedes Teil nach der Regel „outputFile_partIndex.extension“ zu generieren.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als einzelne TIFF-Datei mit mehreren Frames gespeichert.

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

* class [ReportBuilderOptions](../../reportbuilderoptions/)
* class [ReportBuilder](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)

---

## BuildReport(*string, string, [SaveFormat](../../../aspose.words/saveformat/), object, [ReportBuilderOptions](../../reportbuilderoptions/)*) {#buildreport_6}

Füllt das Vorlagendokument mit Daten aus der angegebenen Quelle und generiert einen vollständigen Bericht mit dem angegebenen Ausgabeformat und zusätzlichen Optionen.

```csharp
public static void BuildReport(string inputFileName, string outputFileName, SaveFormat saveFormat, 
    object data, ReportBuilderOptions reportBuilderOptions = null)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFileName | String | Der Name der Eingabedatei. |
| outputFileName | String | Der Name der Ausgabedatei. |
| saveFormat | SaveFormat | Das Speicherformat der Ausgabe. |
| data | Object | Ein Datenquellenobjekt. |
| reportBuilderOptions | ReportBuilderOptions | Zusätzliche Optionen zum Erstellen von Berichten. |

## Bemerkungen

Wenn das Ausgabeformat ein Bild (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP) ist, wird jede Seite der Ausgabe als separate Datei gespeichert. Der angegebene Ausgabedateiname wird verwendet, um Dateinamen für jedes Teil nach der Regel „outputFile_partIndex.extension“ zu generieren.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als einzelne TIFF-Datei mit mehreren Frames gespeichert.

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

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [ReportBuilderOptions](../../reportbuilderoptions/)
* class [ReportBuilder](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)

---

## BuildReport(*string, string, [SaveOptions](../../../aspose.words.saving/saveoptions/), object, [ReportBuilderOptions](../../reportbuilderoptions/)*) {#buildreport_9}

Füllt das Vorlagendokument mit Daten aus der angegebenen Quelle und generiert einen vollständigen Bericht mit dem angegebenen Ausgabeformat und zusätzlichen Optionen.

```csharp
public static void BuildReport(string inputFileName, string outputFileName, 
    SaveOptions saveOptions, object data, ReportBuilderOptions reportBuilderOptions = null)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFileName | String | Der Name der Eingabedatei. |
| outputFileName | String | Der Name der Ausgabedatei. |
| saveOptions | SaveOptions | Die Speicheroptionen der Ausgabe. |
| data | Object | Ein Datenquellenobjekt. |
| reportBuilderOptions | ReportBuilderOptions | Zusätzliche Optionen zum Erstellen von Berichten. |

## Bemerkungen

Wenn das Ausgabeformat ein Bild (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP) ist, wird jede Seite der Ausgabe als separate Datei gespeichert. Der angegebene Ausgabedateiname wird verwendet, um Dateinamen für jedes Teil nach der Regel „outputFile_partIndex.extension“ zu generieren.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als einzelne TIFF-Datei mit mehreren Frames gespeichert.

### Siehe auch

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [ReportBuilderOptions](../../reportbuilderoptions/)
* class [ReportBuilder](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)

---

## BuildReport(*Stream, Stream, [SaveFormat](../../../aspose.words/saveformat/), object, [ReportBuilderOptions](../../reportbuilderoptions/)*) {#buildreport}

Füllt das Vorlagendokument mit Daten aus der angegebenen Quelle und generiert aus Eingabe- und Ausgabeströmen einen vollständigen Bericht mit dem angegebenen Ausgabeformat und zusätzlichen Optionen.

```csharp
public static void BuildReport(Stream inputStream, Stream outputStream, SaveFormat saveFormat, 
    object data, ReportBuilderOptions reportBuilderOptions = null)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputStream | Stream | Der Eingabedateistream. |
| outputStream | Stream | Der Ausgabedateistream. |
| saveFormat | SaveFormat | Das Speicherformat der Ausgabe. |
| data | Object | Ein Datenquellenobjekt. |
| reportBuilderOptions | ReportBuilderOptions | Zusätzliche Optionen zum Erstellen von Berichten. |

## Bemerkungen

Wenn das Ausgabeformat ein Bild ist (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP), wird nur die erste Seite der Ausgabe im angegebenen Stream gespeichert.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als einzelnes TIFF mit mehreren Frames im angegebenen Stream gespeichert.

## Beispiele

Zeigt, wie Dokumente mithilfe von Dokumenten aus dem Stream mit Daten gefüllt werden.

```csharp
// Es gibt mehrere Möglichkeiten, Dokumente mithilfe von Dokumenten aus dem Stream mit Daten zu füllen:
AsposeData obj = new AsposeData { List = new List<string> { "abc" } };

using (FileStream streamIn = new FileStream(MyDir + "Reporting engine template - If greedy.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.BuildReportDataStream.1.docx", FileMode.Create, FileAccess.ReadWrite))
        ReportBuilder.BuildReport(streamIn, streamOut, SaveFormat.Docx, obj);

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.BuildReportDataStream.2.docx", FileMode.Create, FileAccess.ReadWrite))
        ReportBuilder.BuildReport(streamIn, streamOut, SaveFormat.Docx, obj, new ReportBuilderOptions() { Options = ReportBuildOptions.AllowMissingMembers });

    MessageTestClass sender = new MessageTestClass("LINQ Reporting Engine", "Hello World");
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.BuildReportDataStream.3.docx", FileMode.Create, FileAccess.ReadWrite))
        ReportBuilder.BuildReport(streamIn, streamOut, SaveFormat.Docx, new object[] { sender }, new[] { "s" }, new ReportBuilderOptions() { Options = ReportBuildOptions.AllowMissingMembers });
}
```

### Siehe auch

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [ReportBuilderOptions](../../reportbuilderoptions/)
* class [ReportBuilder](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)

---

## BuildReport(*Stream, Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/), object, [ReportBuilderOptions](../../reportbuilderoptions/)*) {#buildreport_3}

Füllt das Vorlagendokument mit Daten aus der angegebenen Quelle und generiert aus Eingabe- und Ausgabeströmen einen vollständigen Bericht mit dem angegebenen Ausgabeformat und zusätzlichen Optionen.

```csharp
public static void BuildReport(Stream inputStream, Stream outputStream, SaveOptions saveOptions, 
    object data, ReportBuilderOptions reportBuilderOptions = null)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputStream | Stream | Der Eingabedateistream. |
| outputStream | Stream | Der Ausgabedateistream. |
| saveOptions | SaveOptions | Die Speicheroptionen der Ausgabe. |
| data | Object | Ein Datenquellenobjekt. |
| reportBuilderOptions | ReportBuilderOptions | Zusätzliche Optionen zum Erstellen von Berichten. |

## Bemerkungen

Wenn das Ausgabeformat ein Bild ist (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP), wird nur die erste Seite der Ausgabe im angegebenen Stream gespeichert.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als einzelnes TIFF mit mehreren Frames im angegebenen Stream gespeichert.

### Siehe auch

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [ReportBuilderOptions](../../reportbuilderoptions/)
* class [ReportBuilder](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)

---

## BuildReport(*string, string, object, string, [ReportBuilderOptions](../../reportbuilderoptions/)*) {#buildreport_13}

Füllt das Vorlagendokument mit Daten aus der angegebenen Quelle und generiert einen vollständigen Bericht mit einer benannten Datenquellenreferenz und zusätzlichen Optionen.

```csharp
public static void BuildReport(string inputFileName, string outputFileName, object data, 
    string dataSourceName, ReportBuilderOptions reportBuilderOptions = null)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFileName | String | Der Name der Eingabedatei. |
| outputFileName | String | Der Name der Ausgabedatei. |
| data | Object | Ein Datenquellenobjekt. |
| dataSourceName | String | Ein Name zum Verweisen auf das Datenquellenobjekt in der Vorlage. |
| reportBuilderOptions | ReportBuilderOptions | Zusätzliche Optionen zum Erstellen von Berichten. |

## Bemerkungen

Wenn das Ausgabeformat ein Bild (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP) ist, wird jede Seite der Ausgabe als separate Datei gespeichert. Der angegebene Ausgabedateiname wird verwendet, um Dateinamen für jedes Teil nach der Regel „outputFile_partIndex.extension“ zu generieren.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als einzelne TIFF-Datei mit mehreren Frames gespeichert.

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

* class [ReportBuilderOptions](../../reportbuilderoptions/)
* class [ReportBuilder](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)

---

## BuildReport(*string, string, [SaveFormat](../../../aspose.words/saveformat/), object, string, [ReportBuilderOptions](../../reportbuilderoptions/)*) {#buildreport_7}

Füllt das Vorlagendokument mit Daten aus der angegebenen Quelle und generiert einen vollständigen Bericht mit dem angegebenen Ausgabeformat, einer benannten Datenquellenreferenz und zusätzlichen Optionen.

```csharp
public static void BuildReport(string inputFileName, string outputFileName, SaveFormat saveFormat, 
    object data, string dataSourceName, ReportBuilderOptions reportBuilderOptions = null)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFileName | String | Der Name der Eingabedatei. |
| outputFileName | String | Der Name der Ausgabedatei. |
| saveFormat | SaveFormat | Das Speicherformat der Ausgabe. |
| data | Object | Ein Datenquellenobjekt. |
| dataSourceName | String | Ein Name zum Verweisen auf das Datenquellenobjekt in der Vorlage. |
| reportBuilderOptions | ReportBuilderOptions | Zusätzliche Optionen zum Erstellen von Berichten. |

## Bemerkungen

Wenn das Ausgabeformat ein Bild (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP) ist, wird jede Seite der Ausgabe als separate Datei gespeichert. Der angegebene Ausgabedateiname wird verwendet, um Dateinamen für jedes Teil nach der Regel „outputFile_partIndex.extension“ zu generieren.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als einzelne TIFF-Datei mit mehreren Frames gespeichert.

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

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [ReportBuilderOptions](../../reportbuilderoptions/)
* class [ReportBuilder](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)

---

## BuildReport(*string, string, [SaveOptions](../../../aspose.words.saving/saveoptions/), object, string, [ReportBuilderOptions](../../reportbuilderoptions/)*) {#buildreport_10}

Füllt das Vorlagendokument mit Daten aus der angegebenen Quelle und generiert einen vollständigen Bericht mit dem angegebenen Ausgabeformat, einer benannten Datenquellenreferenz und zusätzlichen Optionen.

```csharp
public static void BuildReport(string inputFileName, string outputFileName, 
    SaveOptions saveOptions, object data, string dataSourceName, 
    ReportBuilderOptions reportBuilderOptions = null)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFileName | String | Der Name der Eingabedatei. |
| outputFileName | String | Der Name der Ausgabedatei. |
| saveOptions | SaveOptions | Die Speicheroptionen der Ausgabe. |
| data | Object | Ein Datenquellenobjekt. |
| dataSourceName | String | Ein Name zum Verweisen auf das Datenquellenobjekt in der Vorlage. |
| reportBuilderOptions | ReportBuilderOptions | Zusätzliche Optionen zum Erstellen von Berichten. |

## Bemerkungen

Wenn das Ausgabeformat ein Bild (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP) ist, wird jede Seite der Ausgabe als separate Datei gespeichert. Der angegebene Ausgabedateiname wird verwendet, um Dateinamen für jedes Teil nach der Regel „outputFile_partIndex.extension“ zu generieren.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als einzelne TIFF-Datei mit mehreren Frames gespeichert.

### Siehe auch

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [ReportBuilderOptions](../../reportbuilderoptions/)
* class [ReportBuilder](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)

---

## BuildReport(*Stream, Stream, [SaveFormat](../../../aspose.words/saveformat/), object, string, [ReportBuilderOptions](../../reportbuilderoptions/)*) {#buildreport_1}

Füllt das Vorlagendokument mit Daten aus der angegebenen Quelle und generiert einen vollständigen Bericht mit einer benannten Datenquellenreferenz und zusätzlichen Optionen.

```csharp
public static void BuildReport(Stream inputStream, Stream outputStream, SaveFormat saveFormat, 
    object data, string dataSourceName, ReportBuilderOptions reportBuilderOptions = null)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputStream | Stream | Der Eingabedateistream. |
| outputStream | Stream | Der Ausgabedateistream. |
| saveFormat | SaveFormat | Das Speicherformat der Ausgabe. |
| data | Object | Ein Datenquellenobjekt. |
| dataSourceName | String | Ein Name zum Verweisen auf das Datenquellenobjekt in der Vorlage. |
| reportBuilderOptions | ReportBuilderOptions | Zusätzliche Optionen zum Erstellen von Berichten. |

## Bemerkungen

Wenn das Ausgabeformat ein Bild ist (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP), wird nur die erste Seite der Ausgabe im angegebenen Stream gespeichert.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als einzelnes TIFF mit mehreren Frames im angegebenen Stream gespeichert.

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

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [ReportBuilderOptions](../../reportbuilderoptions/)
* class [ReportBuilder](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)

---

## BuildReport(*Stream, Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/), object, string, [ReportBuilderOptions](../../reportbuilderoptions/)*) {#buildreport_4}

Füllt das Vorlagendokument mit Daten aus der angegebenen Quelle und generiert einen vollständigen Bericht mit einer benannten Datenquellenreferenz und zusätzlichen Optionen.

```csharp
public static void BuildReport(Stream inputStream, Stream outputStream, SaveOptions saveOptions, 
    object data, string dataSourceName, ReportBuilderOptions reportBuilderOptions = null)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputStream | Stream | Der Eingabedateistream. |
| outputStream | Stream | Der Ausgabedateistream. |
| saveOptions | SaveOptions | Die Speicheroptionen der Ausgabe. |
| data | Object | Ein Datenquellenobjekt. |
| dataSourceName | String | Ein Name zum Verweisen auf das Datenquellenobjekt in der Vorlage. |
| reportBuilderOptions | ReportBuilderOptions | Zusätzliche Optionen zum Erstellen von Berichten. |

## Bemerkungen

Wenn das Ausgabeformat ein Bild ist (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP), wird nur die erste Seite der Ausgabe im angegebenen Stream gespeichert.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als einzelnes TIFF mit mehreren Frames im angegebenen Stream gespeichert.

### Siehe auch

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [ReportBuilderOptions](../../reportbuilderoptions/)
* class [ReportBuilder](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)

---

## BuildReport(*string, string, object[], string[], [ReportBuilderOptions](../../reportbuilderoptions/)*) {#buildreport_14}

Füllt das Vorlagendokument mit Daten aus mehreren Quellen und generiert einen vollständigen Bericht mit zusätzlichen Optionen. Diese Überladung bestimmt automatisch das Speicherformat basierend auf der Ausgabedateierweiterung.

```csharp
public static void BuildReport(string inputFileName, string outputFileName, object[] data, 
    string[] dataSourceNames, ReportBuilderOptions reportBuilderOptions = null)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFileName | String | Der Name der Eingabedatei. |
| outputFileName | String | Der Name der Ausgabedatei. |
| data | Object[] | Ein Array von Datenquellenobjekten. |
| dataSourceNames | String[] | Ein Array von Namen zum Verweisen auf die Datenquellenobjekte innerhalb der Vorlage. |
| reportBuilderOptions | ReportBuilderOptions | Zusätzliche Optionen zum Erstellen von Berichten. |

## Bemerkungen

Wenn das Ausgabeformat ein Bild (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP) ist, wird jede Seite der Ausgabe als separate Datei gespeichert. Der angegebene Ausgabedateiname wird verwendet, um Dateinamen für jedes Teil nach der Regel „outputFile_partIndex.extension“ zu generieren.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als einzelne TIFF-Datei mit mehreren Frames gespeichert.

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

* class [ReportBuilderOptions](../../reportbuilderoptions/)
* class [ReportBuilder](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)

---

## BuildReport(*string, string, [SaveFormat](../../../aspose.words/saveformat/), object[], string[], [ReportBuilderOptions](../../reportbuilderoptions/)*) {#buildreport_8}

Füllt das Vorlagendokument mit Daten aus mehreren Quellen und generiert einen vollständigen Bericht mit einem angegebenen Ausgabeformat und zusätzlichen Optionen.

```csharp
public static void BuildReport(string inputFileName, string outputFileName, SaveFormat saveFormat, 
    object[] data, string[] dataSourceNames, ReportBuilderOptions reportBuilderOptions = null)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFileName | String | Der Name der Eingabedatei. |
| outputFileName | String | Der Name der Ausgabedatei. |
| saveFormat | SaveFormat | Das Speicherformat der Ausgabe. |
| data | Object[] | Ein Array von Datenquellenobjekten. |
| dataSourceNames | String[] | Ein Array von Namen zum Verweisen auf die Datenquellenobjekte innerhalb der Vorlage. |
| reportBuilderOptions | ReportBuilderOptions | Zusätzliche Optionen zum Erstellen von Berichten. |

## Bemerkungen

Wenn das Ausgabeformat ein Bild (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP) ist, wird jede Seite der Ausgabe als separate Datei gespeichert. Der angegebene Ausgabedateiname wird verwendet, um Dateinamen für jedes Teil nach der Regel „outputFile_partIndex.extension“ zu generieren.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als einzelne TIFF-Datei mit mehreren Frames gespeichert.

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

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [ReportBuilderOptions](../../reportbuilderoptions/)
* class [ReportBuilder](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)

---

## BuildReport(*string, string, [SaveOptions](../../../aspose.words.saving/saveoptions/), object[], string[], [ReportBuilderOptions](../../reportbuilderoptions/)*) {#buildreport_11}

Füllt das Vorlagendokument mit Daten aus mehreren Quellen und generiert einen vollständigen Bericht mit einem angegebenen Ausgabeformat und zusätzlichen Optionen.

```csharp
public static void BuildReport(string inputFileName, string outputFileName, 
    SaveOptions saveOptions, object[] data, string[] dataSourceNames, 
    ReportBuilderOptions reportBuilderOptions = null)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFileName | String | Der Name der Eingabedatei. |
| outputFileName | String | Der Name der Ausgabedatei. |
| saveOptions | SaveOptions | Die Speicheroptionen der Ausgabe. |
| data | Object[] | Ein Array von Datenquellenobjekten. |
| dataSourceNames | String[] | Ein Array von Namen zum Verweisen auf die Datenquellenobjekte innerhalb der Vorlage. |
| reportBuilderOptions | ReportBuilderOptions | Zusätzliche Optionen zum Erstellen von Berichten. |

## Bemerkungen

Wenn das Ausgabeformat ein Bild (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP) ist, wird jede Seite der Ausgabe als separate Datei gespeichert. Der angegebene Ausgabedateiname wird verwendet, um Dateinamen für jedes Teil nach der Regel „outputFile_partIndex.extension“ zu generieren.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als einzelne TIFF-Datei mit mehreren Frames gespeichert.

### Siehe auch

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [ReportBuilderOptions](../../reportbuilderoptions/)
* class [ReportBuilder](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)

---

## BuildReport(*Stream, Stream, [SaveFormat](../../../aspose.words/saveformat/), object[], string[], [ReportBuilderOptions](../../reportbuilderoptions/)*) {#buildreport_2}

Füllt das Vorlagendokument mit Daten aus mehreren Quellen und generiert einen vollständigen Bericht mit dem angegebenen Ausgabeformat und zusätzlichen Optionen aus den angegebenen Eingabe- und Ausgabedateiströmen.

```csharp
public static void BuildReport(Stream inputStream, Stream outputStream, SaveFormat saveFormat, 
    object[] data, string[] dataSourceNames, ReportBuilderOptions reportBuilderOptions = null)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputStream | Stream | Der Eingabedateistream. |
| outputStream | Stream | Der Ausgabedateistream. |
| saveFormat | SaveFormat | Das Speicherformat der Ausgabe. |
| data | Object[] | Ein Array von Datenquellenobjekten. |
| dataSourceNames | String[] | Ein Array von Namen zum Verweisen auf die Datenquellenobjekte innerhalb der Vorlage. |
| reportBuilderOptions | ReportBuilderOptions | Zusätzliche Optionen zum Erstellen von Berichten. |

## Bemerkungen

Wenn das Ausgabeformat ein Bild ist (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP), wird nur die erste Seite der Ausgabe im angegebenen Stream gespeichert.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als einzelnes TIFF mit mehreren Frames im angegebenen Stream gespeichert.

## Beispiele

Zeigt, wie Dokumente mithilfe von Dokumenten aus dem Stream mit Daten gefüllt werden.

```csharp
// Es gibt mehrere Möglichkeiten, Dokumente mithilfe von Dokumenten aus dem Stream mit Daten zu füllen:
AsposeData obj = new AsposeData { List = new List<string> { "abc" } };

using (FileStream streamIn = new FileStream(MyDir + "Reporting engine template - If greedy.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.BuildReportDataStream.1.docx", FileMode.Create, FileAccess.ReadWrite))
        ReportBuilder.BuildReport(streamIn, streamOut, SaveFormat.Docx, obj);

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.BuildReportDataStream.2.docx", FileMode.Create, FileAccess.ReadWrite))
        ReportBuilder.BuildReport(streamIn, streamOut, SaveFormat.Docx, obj, new ReportBuilderOptions() { Options = ReportBuildOptions.AllowMissingMembers });

    MessageTestClass sender = new MessageTestClass("LINQ Reporting Engine", "Hello World");
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.BuildReportDataStream.3.docx", FileMode.Create, FileAccess.ReadWrite))
        ReportBuilder.BuildReport(streamIn, streamOut, SaveFormat.Docx, new object[] { sender }, new[] { "s" }, new ReportBuilderOptions() { Options = ReportBuildOptions.AllowMissingMembers });
}
```

### Siehe auch

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [ReportBuilderOptions](../../reportbuilderoptions/)
* class [ReportBuilder](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)

---

## BuildReport(*Stream, Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/), object[], string[], [ReportBuilderOptions](../../reportbuilderoptions/)*) {#buildreport_5}

Füllt das Vorlagendokument mit Daten aus mehreren Quellen und generiert einen vollständigen Bericht mit dem angegebenen Ausgabeformat und zusätzlichen Optionen aus den angegebenen Eingabe- und Ausgabedateiströmen.

```csharp
public static void BuildReport(Stream inputStream, Stream outputStream, SaveOptions saveOptions, 
    object[] data, string[] dataSourceNames, ReportBuilderOptions reportBuilderOptions = null)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputStream | Stream | Der Eingabedateistream. |
| outputStream | Stream | Der Ausgabedateistream. |
| saveOptions | SaveOptions | Die Speicheroptionen der Ausgabe. |
| data | Object[] | Ein Array von Datenquellenobjekten. |
| dataSourceNames | String[] | Ein Array von Namen zum Verweisen auf die Datenquellenobjekte innerhalb der Vorlage. |
| reportBuilderOptions | ReportBuilderOptions | Zusätzliche Optionen zum Erstellen von Berichten. |

## Bemerkungen

Wenn das Ausgabeformat ein Bild ist (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP), wird nur die erste Seite der Ausgabe im angegebenen Stream gespeichert.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als einzelnes TIFF mit mehreren Frames im angegebenen Stream gespeichert.

### Siehe auch

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [ReportBuilderOptions](../../reportbuilderoptions/)
* class [ReportBuilder](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)
