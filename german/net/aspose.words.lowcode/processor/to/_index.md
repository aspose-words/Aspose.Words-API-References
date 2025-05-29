---
title: Processor.To
linktitle: To
articleTitle: To
second_title: Aspose.Words für .NET
description: Optimieren Sie Ihren Arbeitsablauf mit unserer Prozessormethode, die Ausgabedateien klar definiert, die Effizienz steigert und Ihre Datenverwaltungsaufgaben rationalisiert.
type: docs
weight: 30
url: /de/net/aspose.words.lowcode/processor/to/
---
## To(*string, [SaveOptions](../../../aspose.words.saving/saveoptions/)*) {#to_5}

Gibt die Ausgabedatei für den Prozessor an.

```csharp
public Processor To(string output, SaveOptions saveOptions = null)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| output | String | Name der Ausgabedatei. |
| saveOptions | SaveOptions | Optionale Speicheroptionen. Wenn keine Optionen angegeben sind, wird das Speicherformat durch die Dateierweiterung bestimmt. |

### Rückgabewert

Gibt den Prozessor mit der angegebenen Ausgabedatei zurück.

## Bemerkungen

Wenn die Ausgabe aus mehreren Dateien besteht, wird der angegebene Ausgabedateiname verwendet, um den Dateinamen für jeden Teil gemäß der Regel „outputFile_partIndex.extension“ zu generieren.

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

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Processor](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)

---

## To(*string, [SaveFormat](../../../aspose.words/saveformat/)*) {#to_4}

Gibt die Ausgabedatei für den Prozessor an.

```csharp
public Processor To(string output, SaveFormat saveFormat)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| output | String | Name der Ausgabedatei. |
| saveFormat | SaveFormat | Speicherformat. Wenn nicht angegeben, wird das Speicherformat durch die Dateierweiterung bestimmt. |

### Rückgabewert

Gibt den Prozessor mit der angegebenen Ausgabedatei zurück.

## Bemerkungen

Wenn die Ausgabe aus mehreren Dateien besteht, wird der angegebene Ausgabedateiname verwendet, um den Dateinamen für jeden Teil gemäß der Regel „outputFile_partIndex.extension“ zu generieren.

## Beispiele

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

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [Processor](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)

---

## To(*Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/)*) {#to_3}

Gibt den Ausgabestream für den Prozessor an.

```csharp
public Processor To(Stream output, SaveOptions saveOptions)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| output | Stream | Ausgabestream. |
| saveOptions | SaveOptions | Optionen speichern. |

### Rückgabewert

Gibt den Prozessor mit dem angegebenen Ausgabestrom zurück.

## Bemerkungen

Wenn die Ausgabe aus mehreren Dateien besteht, wird nur der erste Teil im angegebenen Stream gespeichert.

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

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Processor](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)

---

## To(*Stream, [SaveFormat](../../../aspose.words/saveformat/)*) {#to_2}

Gibt den Ausgabestream für den Prozessor an.

```csharp
public Processor To(Stream output, SaveFormat saveFormat)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| output | Stream | Ausgabestream. |
| saveFormat | SaveFormat | Format speichern. |

### Rückgabewert

Gibt den Prozessor mit dem angegebenen Ausgabestrom zurück.

## Bemerkungen

Wenn die Ausgabe aus mehreren Dateien besteht, wird nur der erste Teil im angegebenen Stream gespeichert.

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

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [Processor](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)

---

## To(*List&lt;Stream&gt;, [SaveOptions](../../../aspose.words.saving/saveoptions/)*) {#to_1}

Gibt die Liste der Ausgabedokumentströme an.

```csharp
public Processor To(List<Stream> output, SaveOptions saveOptions)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| output | List`1 | Liste der Ausgabedokumentströme. |
| saveOptions | SaveOptions | Optionen speichern. |

### Rückgabewert

Gibt den Prozessor mit der angegebenen Liste der Ausgabedokumentströme zurück.

## Bemerkungen

Wenn die Ausgabe aus mehreren Dateien besteht (z. B. Bildern oder aufgeteilten Dokumentteilen), wird der angegebenen Liste für jeden Teil ein Stream hinzugefügt. Wenn die Ausgabe eine einzelne Datei ist, wird der Liste nur ein Stream hinzugefügt. Es liegt in der Verantwortung des Endbenutzers, die erstellten Streams zu entsorgen.

### Siehe auch

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Processor](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)

---

## To(*List&lt;Stream&gt;, [SaveFormat](../../../aspose.words/saveformat/)*) {#to}

Gibt die Liste der Ausgabedokumentströme an.

```csharp
public Processor To(List<Stream> output, SaveFormat saveFormat)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| output | List`1 | Liste der Ausgabedokumentströme. |
| saveFormat | SaveFormat | Format speichern. |

### Rückgabewert

Gibt den Prozessor mit der angegebenen Liste der Ausgabedokumentströme zurück.

## Bemerkungen

Wenn die Ausgabe aus mehreren Dateien besteht (z. B. Bildern oder aufgeteilten Dokumentteilen), wird der angegebenen Liste für jeden Teil ein Stream hinzugefügt. Wenn die Ausgabe eine einzelne Datei ist, wird der Liste nur ein Stream hinzugefügt. Es liegt in der Verantwortung des Endbenutzers, die erstellten Streams zu entsorgen.

### Siehe auch

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [Processor](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)
