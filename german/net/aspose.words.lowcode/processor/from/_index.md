---
title: Processor.From
linktitle: From
articleTitle: From
second_title: Aspose.Words für .NET
description: Verbessern Sie Ihren Arbeitsablauf mit unserem Prozessor, der Eingabedokumente effizient verarbeitet und so für eine nahtlose Verarbeitung und verbesserte Produktivität sorgt.
type: docs
weight: 20
url: /de/net/aspose.words.lowcode/processor/from/
---
## From(*string, [LoadOptions](../../../aspose.words.loading/loadoptions/)*) {#from_1}

Gibt das Eingabedokument für die Verarbeitung an.

```csharp
public Processor From(string input, LoadOptions loadOptions = null)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| input | String | Geben Sie den Dateinamen des Dokuments ein. |
| loadOptions | LoadOptions | Optionale Ladeoptionen zum Laden des Dokuments. |

### Rückgabewert

Gibt den Prozessor mit der angegebenen Eingabedatei zurück.

## Bemerkungen

Wenn der Prozessor nur eine Datei als Eingabe akzeptiert, wird nur die zuletzt angegebene Datei verarbeitet. [`Merger`](../../merger/) Der Prozessor akzeptiert mehrere Dateien als Eingabe, als Ergebnis werden alle angegebenen Dokumente zusammengeführt. [`Converter`](../../converter/) Der Prozessor akzeptiert nur eine Datei als Eingabe, daher wird nur die zuletzt angegebene Datei konvertiert.

## Beispiele

Zeigt, wie Dokumente mithilfe von Kontext mit einer einzigen Codezeile konvertiert werden.

```csharp
string doc = MyDir + "Big document.docx";

Converter.Create(new ConverterContext())
    .From(doc)
    .To(ArtifactsDir + "LowCode.ConvertContext.1.pdf")
    .Execute();

Converter.Create(new ConverterContext())
    .From(doc)
    .To(ArtifactsDir + "LowCode.ConvertContext.2.pdf", SaveFormat.Rtf)
    .Execute();

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
LoadOptions loadOptions = new LoadOptions() { IgnoreOleData = true };
Converter.Create(new ConverterContext())
    .From(doc, loadOptions)
    .To(ArtifactsDir + "LowCode.ConvertContext.3.docx", saveOptions)
    .Execute();

Converter.Create(new ConverterContext())
    .From(doc)
    .To(ArtifactsDir + "LowCode.ConvertContext.4.png", new ImageSaveOptions(SaveFormat.Png))
    .Execute();
```

Zeigt, wie Dokumente mithilfe des Kontexts zu einem einzigen Ausgabedokument zusammengeführt werden.

```csharp
//Es gibt mehrere Möglichkeiten, Dokumente zusammenzuführen:
string inputDoc1 = MyDir + "Big document.docx";
string inputDoc2 = MyDir + "Tables.docx";

Merger.Create(new MergerContext() { MergeFormatMode = MergeFormatMode.KeepSourceFormatting })
    .From(inputDoc1)
    .From(inputDoc2)
    .To(ArtifactsDir + "LowCode.MergeContextDocuments.1.docx")
    .Execute();

LoadOptions firstLoadOptions = new LoadOptions() { IgnoreOleData = true };
LoadOptions secondLoadOptions = new LoadOptions() { IgnoreOleData = false };
Merger.Create(new MergerContext() { MergeFormatMode = MergeFormatMode.KeepSourceFormatting })
    .From(inputDoc1, firstLoadOptions)
    .From(inputDoc2, secondLoadOptions)
    .To(ArtifactsDir + "LowCode.MergeContextDocuments.2.docx", SaveFormat.Docx)
    .Execute();

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
Merger.Create(new MergerContext() { MergeFormatMode = MergeFormatMode.KeepSourceFormatting })
    .From(inputDoc1)
    .From(inputDoc2)
    .To(ArtifactsDir + "LowCode.MergeContextDocuments.3.docx", saveOptions)
    .Execute();
```

### Siehe auch

* class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* class [Processor](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)

---

## From(*Stream, [LoadOptions](../../../aspose.words.loading/loadoptions/)*) {#from}

Gibt das Eingabedokument für die Verarbeitung an.

```csharp
public Processor From(Stream input, LoadOptions loadOptions = null)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| input | Stream | Eingabedokumentenstrom. |
| loadOptions | LoadOptions | Optionale Ladeoptionen zum Laden des Dokuments. |

### Rückgabewert

Gibt den Prozessor mit dem angegebenen Eingabedateistream zurück.

## Bemerkungen

Wenn der Prozessor nur eine Datei als Eingabe akzeptiert, wird nur die zuletzt angegebene Datei verarbeitet. [`Merger`](../../merger/) Der Prozessor akzeptiert mehrere Dateien als Eingabe, als Ergebnis werden alle angegebenen Dokumente zusammengeführt. [`Converter`](../../converter/) Der Prozessor akzeptiert nur eine Datei als Eingabe, daher wird nur die zuletzt angegebene Datei konvertiert.

## Beispiele

Zeigt, wie Dokumente aus einem Stream mithilfe von Kontext mit einer einzigen Codezeile konvertiert werden.

```csharp
string doc = MyDir + "Document.docx";
using (FileStream streamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ConvertContextStream.1.docx", FileMode.Create, FileAccess.ReadWrite))
        Converter.Create(new ConverterContext())
            .From(streamIn)
            .To(streamOut, SaveFormat.Rtf)
            .Execute();

    OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
    LoadOptions loadOptions = new LoadOptions() { IgnoreOleData = true };
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ConvertContextStream.2.docx", FileMode.Create, FileAccess.ReadWrite))
        Converter.Create(new ConverterContext())
            .From(streamIn, loadOptions)
            .To(streamOut, saveOptions)
            .Execute();

    List<Stream> pages = new List<Stream>();
    Converter.Create(new ConverterContext())
        .From(doc)
        .To(pages, new ImageSaveOptions(SaveFormat.Png))
        .Execute();
}
```

Zeigt, wie Dokumente aus einem Stream mithilfe des Kontexts in ein einzelnes Ausgabedokument zusammengeführt werden.

```csharp
//Es gibt mehrere Möglichkeiten, Dokumente zusammenzuführen:
string inputDoc1 = MyDir + "Big document.docx";
string inputDoc2 = MyDir + "Tables.docx";

using (FileStream firstStreamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream secondStreamIn = new FileStream(MyDir + "Tables.docx", FileMode.Open, FileAccess.Read))
    {
        OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamContextDocuments.1.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Create(new MergerContext() { MergeFormatMode = MergeFormatMode.KeepSourceFormatting })
            .From(firstStreamIn)
            .From(secondStreamIn)
            .To(streamOut, saveOptions)
            .Execute();

        LoadOptions firstLoadOptions = new LoadOptions() { IgnoreOleData = true };
        LoadOptions secondLoadOptions = new LoadOptions() { IgnoreOleData = false };
        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamContextDocuments.2.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Create(new MergerContext() { MergeFormatMode = MergeFormatMode.KeepSourceFormatting })
            .From(firstStreamIn, firstLoadOptions)
            .From(secondStreamIn, secondLoadOptions)
            .To(streamOut, SaveFormat.Docx)
            .Execute();
    }
}
```

### Siehe auch

* class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* class [Processor](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)
