---
title: Merger.Merge
linktitle: Merge
articleTitle: Merge
second_title: Aspose.Words für .NET
description: Kombinieren Sie mühelos mehrere Dokumente mit unserer Merger-Merge-Methode zu einem einzigen. Optimieren Sie Ihren Workflow noch heute mit anpassbaren Dateioptionen!
type: docs
weight: 20
url: /de/net/aspose.words.lowcode/merger/merge/
---
## Merge(*string, string[]*) {#merge_8}

Fügt die angegebenen Eingabedokumente zu einem einzigen Ausgabedokument zusammen, wobei die angegebenen Eingabe und Ausgabedateinamen verwendet werden.KeepSourceFormatting .

```csharp
public static void Merge(string outputFile, string[] inputFiles)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| outputFile | String | Der Name der Ausgabedatei. |
| inputFiles | String[] | Die Namen der Eingabedateien. |

## Bemerkungen

Wenn das Ausgabeformat ein Bild (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP) ist, wird jede Seite der Ausgabe als separate Datei gespeichert. Der angegebene Ausgabedateiname wird verwendet, um Dateinamen für jedes Teil nach der Regel „outputFile_partIndex.extension“ zu generieren.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als einzelne TIFF-Datei mit mehreren Frames gespeichert.

## Beispiele

Zeigt, wie Dokumente zu einem einzigen Ausgabedokument zusammengeführt werden.

```csharp
//Es gibt mehrere Möglichkeiten, Dokumente zusammenzuführen:
string inputDoc1 = MyDir + "Big document.docx";
string inputDoc2 = MyDir + "Tables.docx";

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.1.docx", new[] { inputDoc1, inputDoc2 });

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.2.docx", new[] { inputDoc1, inputDoc2 }, saveOptions, MergeFormatMode.KeepSourceFormatting);

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.3.pdf", new[] { inputDoc1, inputDoc2 }, SaveFormat.Pdf, MergeFormatMode.KeepSourceLayout);

LoadOptions firstLoadOptions = new LoadOptions() { IgnoreOleData = true };
LoadOptions secondLoadOptions = new LoadOptions() { IgnoreOleData = false };
Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.4.docx", new[] { inputDoc1, inputDoc2 }, new[] { firstLoadOptions, secondLoadOptions }, saveOptions, MergeFormatMode.KeepSourceFormatting);

Document doc = Merger.Merge(new[] { inputDoc1, inputDoc2 }, MergeFormatMode.MergeFormatting);
doc.Save(ArtifactsDir + "LowCode.MergeDocument.5.docx");

doc = Merger.Merge(new[] { inputDoc1, inputDoc2 }, new[] { firstLoadOptions, secondLoadOptions }, MergeFormatMode.MergeFormatting);
doc.Save(ArtifactsDir + "LowCode.MergeDocument.6.docx");
```

### Siehe auch

* class [Merger](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)

---

## Merge(*string, string[], [SaveFormat](../../../aspose.words/saveformat/), [MergeFormatMode](../../mergeformatmode/)*) {#merge_10}

Fügt die angegebenen Eingabedokumente unter Verwendung der angegebenen Eingabe-/Ausgabedateinamen und des endgültigen Dokumentformats zu einem einzigen Ausgabedokument zusammen.

```csharp
public static void Merge(string outputFile, string[] inputFiles, SaveFormat saveFormat, 
    MergeFormatMode mergeFormatMode)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| outputFile | String | Der Name der Ausgabedatei. |
| inputFiles | String[] | Die Namen der Eingabedateien. |
| saveFormat | SaveFormat | Das Speicherformat. |
| mergeFormatMode | MergeFormatMode | Gibt an, wie kollidierende Formatierungen zusammengeführt werden. |

## Bemerkungen

Wenn das Ausgabeformat ein Bild (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP) ist, wird jede Seite der Ausgabe als separate Datei gespeichert. Der angegebene Ausgabedateiname wird verwendet, um Dateinamen für jedes Teil nach der Regel „outputFile_partIndex.extension“ zu generieren.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als einzelne TIFF-Datei mit mehreren Frames gespeichert.

## Beispiele

Zeigt, wie Dokumente zu einem einzigen Ausgabedokument zusammengeführt werden.

```csharp
//Es gibt mehrere Möglichkeiten, Dokumente zusammenzuführen:
string inputDoc1 = MyDir + "Big document.docx";
string inputDoc2 = MyDir + "Tables.docx";

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.1.docx", new[] { inputDoc1, inputDoc2 });

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.2.docx", new[] { inputDoc1, inputDoc2 }, saveOptions, MergeFormatMode.KeepSourceFormatting);

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.3.pdf", new[] { inputDoc1, inputDoc2 }, SaveFormat.Pdf, MergeFormatMode.KeepSourceLayout);

LoadOptions firstLoadOptions = new LoadOptions() { IgnoreOleData = true };
LoadOptions secondLoadOptions = new LoadOptions() { IgnoreOleData = false };
Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.4.docx", new[] { inputDoc1, inputDoc2 }, new[] { firstLoadOptions, secondLoadOptions }, saveOptions, MergeFormatMode.KeepSourceFormatting);

Document doc = Merger.Merge(new[] { inputDoc1, inputDoc2 }, MergeFormatMode.MergeFormatting);
doc.Save(ArtifactsDir + "LowCode.MergeDocument.5.docx");

doc = Merger.Merge(new[] { inputDoc1, inputDoc2 }, new[] { firstLoadOptions, secondLoadOptions }, MergeFormatMode.MergeFormatting);
doc.Save(ArtifactsDir + "LowCode.MergeDocument.6.docx");
```

### Siehe auch

* enum [SaveFormat](../../../aspose.words/saveformat/)
* enum [MergeFormatMode](../../mergeformatmode/)
* class [Merger](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)

---

## Merge(*string, string[], [SaveOptions](../../../aspose.words.saving/saveoptions/), [MergeFormatMode](../../mergeformatmode/)*) {#merge_11}

Fügt die angegebenen Eingabedokumente unter Verwendung der angegebenen Eingabe-/Ausgabedateinamen und Speicheroptionen zu einem einzigen Ausgabedokument zusammen.

```csharp
public static void Merge(string outputFile, string[] inputFiles, SaveOptions saveOptions, 
    MergeFormatMode mergeFormatMode)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| outputFile | String | Der Name der Ausgabedatei. |
| inputFiles | String[] | Die Namen der Eingabedateien. |
| saveOptions | SaveOptions | Die Speicheroptionen. |
| mergeFormatMode | MergeFormatMode | Gibt an, wie kollidierende Formatierungen zusammengeführt werden. |

## Bemerkungen

Wenn das Ausgabeformat ein Bild (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP) ist, wird jede Seite der Ausgabe als separate Datei gespeichert. Der angegebene Ausgabedateiname wird verwendet, um Dateinamen für jedes Teil nach der Regel „outputFile_partIndex.extension“ zu generieren.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als einzelne TIFF-Datei mit mehreren Frames gespeichert.

## Beispiele

Zeigt, wie Dokumente zu einem einzigen Ausgabedokument zusammengeführt werden.

```csharp
//Es gibt mehrere Möglichkeiten, Dokumente zusammenzuführen:
string inputDoc1 = MyDir + "Big document.docx";
string inputDoc2 = MyDir + "Tables.docx";

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.1.docx", new[] { inputDoc1, inputDoc2 });

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.2.docx", new[] { inputDoc1, inputDoc2 }, saveOptions, MergeFormatMode.KeepSourceFormatting);

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.3.pdf", new[] { inputDoc1, inputDoc2 }, SaveFormat.Pdf, MergeFormatMode.KeepSourceLayout);

LoadOptions firstLoadOptions = new LoadOptions() { IgnoreOleData = true };
LoadOptions secondLoadOptions = new LoadOptions() { IgnoreOleData = false };
Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.4.docx", new[] { inputDoc1, inputDoc2 }, new[] { firstLoadOptions, secondLoadOptions }, saveOptions, MergeFormatMode.KeepSourceFormatting);

Document doc = Merger.Merge(new[] { inputDoc1, inputDoc2 }, MergeFormatMode.MergeFormatting);
doc.Save(ArtifactsDir + "LowCode.MergeDocument.5.docx");

doc = Merger.Merge(new[] { inputDoc1, inputDoc2 }, new[] { firstLoadOptions, secondLoadOptions }, MergeFormatMode.MergeFormatting);
doc.Save(ArtifactsDir + "LowCode.MergeDocument.6.docx");
```

### Siehe auch

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* enum [MergeFormatMode](../../mergeformatmode/)
* class [Merger](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)

---

## Merge(*string, string[], LoadOptions[], [SaveOptions](../../../aspose.words.saving/saveoptions/), [MergeFormatMode](../../mergeformatmode/)*) {#merge_9}

Fügt die angegebenen Eingabedokumente unter Verwendung der angegebenen Eingabe-/Ausgabedateinamen und Speicheroptionen zu einem einzigen Ausgabedokument zusammen.

```csharp
public static void Merge(string outputFile, string[] inputFiles, LoadOptions[] loadOptions, 
    SaveOptions saveOptions, MergeFormatMode mergeFormatMode)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| outputFile | String | Der Name der Ausgabedatei. |
| inputFiles | String[] | Die Namen der Eingabedateien. |
| loadOptions | LoadOptions[] | Ladeoptionen für die Eingabedateien. |
| saveOptions | SaveOptions | Die Speicheroptionen. |
| mergeFormatMode | MergeFormatMode | Gibt an, wie kollidierende Formatierungen zusammengeführt werden. |

## Bemerkungen

Wenn das Ausgabeformat ein Bild (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP) ist, wird jede Seite der Ausgabe als separate Datei gespeichert. Der angegebene Ausgabedateiname wird verwendet, um Dateinamen für jedes Teil nach der Regel „outputFile_partIndex.extension“ zu generieren.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als einzelne TIFF-Datei mit mehreren Frames gespeichert.

## Beispiele

Zeigt, wie Dokumente zu einem einzigen Ausgabedokument zusammengeführt werden.

```csharp
//Es gibt mehrere Möglichkeiten, Dokumente zusammenzuführen:
string inputDoc1 = MyDir + "Big document.docx";
string inputDoc2 = MyDir + "Tables.docx";

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.1.docx", new[] { inputDoc1, inputDoc2 });

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.2.docx", new[] { inputDoc1, inputDoc2 }, saveOptions, MergeFormatMode.KeepSourceFormatting);

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.3.pdf", new[] { inputDoc1, inputDoc2 }, SaveFormat.Pdf, MergeFormatMode.KeepSourceLayout);

LoadOptions firstLoadOptions = new LoadOptions() { IgnoreOleData = true };
LoadOptions secondLoadOptions = new LoadOptions() { IgnoreOleData = false };
Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.4.docx", new[] { inputDoc1, inputDoc2 }, new[] { firstLoadOptions, secondLoadOptions }, saveOptions, MergeFormatMode.KeepSourceFormatting);

Document doc = Merger.Merge(new[] { inputDoc1, inputDoc2 }, MergeFormatMode.MergeFormatting);
doc.Save(ArtifactsDir + "LowCode.MergeDocument.5.docx");

doc = Merger.Merge(new[] { inputDoc1, inputDoc2 }, new[] { firstLoadOptions, secondLoadOptions }, MergeFormatMode.MergeFormatting);
doc.Save(ArtifactsDir + "LowCode.MergeDocument.6.docx");
```

### Siehe auch

* class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* enum [MergeFormatMode](../../mergeformatmode/)
* class [Merger](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)

---

## Merge(*string[], [MergeFormatMode](../../mergeformatmode/)*) {#merge_4}

Fügt die angegebenen Eingabedokumente zu einem einzigen Dokument zusammen und gibt[`Document`](../../../aspose.words/document/) Instanz des endgültigen Dokuments.

```csharp
public static Document Merge(string[] inputFiles, MergeFormatMode mergeFormatMode)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFiles | String[] | Die Namen der Eingabedateien. |
| mergeFormatMode | MergeFormatMode | Gibt an, wie kollidierende Formatierungen zusammengeführt werden. |

## Beispiele

Zeigt, wie Dokumente zu einem einzigen Ausgabedokument zusammengeführt werden.

```csharp
//Es gibt mehrere Möglichkeiten, Dokumente zusammenzuführen:
string inputDoc1 = MyDir + "Big document.docx";
string inputDoc2 = MyDir + "Tables.docx";

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.1.docx", new[] { inputDoc1, inputDoc2 });

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.2.docx", new[] { inputDoc1, inputDoc2 }, saveOptions, MergeFormatMode.KeepSourceFormatting);

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.3.pdf", new[] { inputDoc1, inputDoc2 }, SaveFormat.Pdf, MergeFormatMode.KeepSourceLayout);

LoadOptions firstLoadOptions = new LoadOptions() { IgnoreOleData = true };
LoadOptions secondLoadOptions = new LoadOptions() { IgnoreOleData = false };
Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.4.docx", new[] { inputDoc1, inputDoc2 }, new[] { firstLoadOptions, secondLoadOptions }, saveOptions, MergeFormatMode.KeepSourceFormatting);

Document doc = Merger.Merge(new[] { inputDoc1, inputDoc2 }, MergeFormatMode.MergeFormatting);
doc.Save(ArtifactsDir + "LowCode.MergeDocument.5.docx");

doc = Merger.Merge(new[] { inputDoc1, inputDoc2 }, new[] { firstLoadOptions, secondLoadOptions }, MergeFormatMode.MergeFormatting);
doc.Save(ArtifactsDir + "LowCode.MergeDocument.6.docx");
```

### Siehe auch

* class [Document](../../../aspose.words/document/)
* enum [MergeFormatMode](../../mergeformatmode/)
* class [Merger](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)

---

## Merge(*string[], LoadOptions[], [MergeFormatMode](../../mergeformatmode/)*) {#merge_3}

Fügt die angegebenen Eingabedokumente zu einem einzigen Dokument zusammen und gibt[`Document`](../../../aspose.words/document/) Instanz des endgültigen Dokuments.

```csharp
public static Document Merge(string[] inputFiles, LoadOptions[] loadOptions, 
    MergeFormatMode mergeFormatMode)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFiles | String[] | Die Namen der Eingabedateien. |
| loadOptions | LoadOptions[] | Ladeoptionen für die Eingabedateien. |
| mergeFormatMode | MergeFormatMode | Gibt an, wie kollidierende Formatierungen zusammengeführt werden. |

## Beispiele

Zeigt, wie Dokumente zu einem einzigen Ausgabedokument zusammengeführt werden.

```csharp
//Es gibt mehrere Möglichkeiten, Dokumente zusammenzuführen:
string inputDoc1 = MyDir + "Big document.docx";
string inputDoc2 = MyDir + "Tables.docx";

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.1.docx", new[] { inputDoc1, inputDoc2 });

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.2.docx", new[] { inputDoc1, inputDoc2 }, saveOptions, MergeFormatMode.KeepSourceFormatting);

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.3.pdf", new[] { inputDoc1, inputDoc2 }, SaveFormat.Pdf, MergeFormatMode.KeepSourceLayout);

LoadOptions firstLoadOptions = new LoadOptions() { IgnoreOleData = true };
LoadOptions secondLoadOptions = new LoadOptions() { IgnoreOleData = false };
Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.4.docx", new[] { inputDoc1, inputDoc2 }, new[] { firstLoadOptions, secondLoadOptions }, saveOptions, MergeFormatMode.KeepSourceFormatting);

Document doc = Merger.Merge(new[] { inputDoc1, inputDoc2 }, MergeFormatMode.MergeFormatting);
doc.Save(ArtifactsDir + "LowCode.MergeDocument.5.docx");

doc = Merger.Merge(new[] { inputDoc1, inputDoc2 }, new[] { firstLoadOptions, secondLoadOptions }, MergeFormatMode.MergeFormatting);
doc.Save(ArtifactsDir + "LowCode.MergeDocument.6.docx");
```

### Siehe auch

* class [Document](../../../aspose.words/document/)
* class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* enum [MergeFormatMode](../../mergeformatmode/)
* class [Merger](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)

---

## Merge(*Document[], [MergeFormatMode](../../mergeformatmode/)*) {#merge}

Fügt die angegebenen Eingabedokumente zu einem einzigen Dokument zusammen und gibt[`Document`](../../../aspose.words/document/) Instanz des endgültigen Dokuments.

```csharp
public static Document Merge(Document[] inputDocuments, MergeFormatMode mergeFormatMode)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputDocuments | Document[] | Die Eingabedokumente. |
| mergeFormatMode | MergeFormatMode | Gibt an, wie kollidierende Formatierungen zusammengeführt werden. |

## Beispiele

Zeigt, wie Eingabedokumente zu einer einzigen Dokumentinstanz zusammengeführt werden.

```csharp
DocumentBuilder firstDoc = new DocumentBuilder();
firstDoc.Font.Size = 16;
firstDoc.Font.Color = Color.Blue;
firstDoc.Write("Hello first word!");

DocumentBuilder secondDoc = new DocumentBuilder();
secondDoc.Write("Hello second word!");

Document mergedDoc = Merger.Merge(new Document[] { firstDoc.Document, secondDoc.Document }, MergeFormatMode.KeepSourceLayout);
Assert.AreEqual("Hello first word!\fHello second word!\f", mergedDoc.GetText());
```

### Siehe auch

* class [Document](../../../aspose.words/document/)
* enum [MergeFormatMode](../../mergeformatmode/)
* class [Merger](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)

---

## Merge(*Stream, Stream[], [SaveFormat](../../../aspose.words/saveformat/)*) {#merge_6}

Fügt die angegebenen Eingabedokumente unter Verwendung der angegebenen Eingabe-/Ausgabeströme und des endgültigen Dokumentformats zu einem einzigen Ausgabedokument zusammen.

```csharp
public static void Merge(Stream outputStream, Stream[] inputStreams, SaveFormat saveFormat)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| outputStream | Stream | Der Ausgabestream. |
| inputStreams | Stream[] | Die Eingabestreams. |
| saveFormat | SaveFormat | Das Speicherformat. |

## Bemerkungen

Wenn das Ausgabeformat ein Bild ist (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP), wird nur die erste Seite der Ausgabe im angegebenen Stream gespeichert.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als einzelnes TIFF mit mehreren Frames im angegebenen Stream gespeichert.

## Beispiele

Zeigt, wie Dokumente aus einem Stream in ein einzelnes Ausgabedokument zusammengeführt werden.

```csharp
//Es gibt mehrere Möglichkeiten, Dokumente aus einem Stream zusammenzuführen:
using (FileStream firstStreamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream secondStreamIn = new FileStream(MyDir + "Tables.docx", FileMode.Open, FileAccess.Read))
    {
        OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamDocument.1.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Merge(streamOut, new[] { firstStreamIn, secondStreamIn }, saveOptions, MergeFormatMode.KeepSourceFormatting);

        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamDocument.2.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Merge(streamOut, new[] { firstStreamIn, secondStreamIn }, SaveFormat.Docx);

        LoadOptions firstLoadOptions = new LoadOptions() { IgnoreOleData = true };
        LoadOptions secondLoadOptions = new LoadOptions() { IgnoreOleData = false };
        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamDocument.3.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Merge(streamOut, new[] { firstStreamIn, secondStreamIn }, new[] { firstLoadOptions, secondLoadOptions }, saveOptions, MergeFormatMode.KeepSourceFormatting);

        Document firstDoc = Merger.Merge(new[] { firstStreamIn, secondStreamIn }, MergeFormatMode.MergeFormatting);
        firstDoc.Save(ArtifactsDir + "LowCode.MergeStreamDocument.4.docx");

        Document secondDoc = Merger.Merge(new[] { firstStreamIn, secondStreamIn }, new[] { firstLoadOptions, secondLoadOptions }, MergeFormatMode.MergeFormatting);
        secondDoc.Save(ArtifactsDir + "LowCode.MergeStreamDocument.5.docx");
    }
}
```

### Siehe auch

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [Merger](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)

---

## Merge(*Stream, Stream[], [SaveOptions](../../../aspose.words.saving/saveoptions/), [MergeFormatMode](../../mergeformatmode/)*) {#merge_7}

Fügt die angegebenen Eingabedokumente unter Verwendung der angegebenen Eingabe-/Ausgabeströme und Speicheroptionen zu einem einzigen Ausgabedokument zusammen.

```csharp
public static void Merge(Stream outputStream, Stream[] inputStreams, SaveOptions saveOptions, 
    MergeFormatMode mergeFormatMode)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| outputStream | Stream | Der Ausgabestream. |
| inputStreams | Stream[] | Die Eingabestreams. |
| saveOptions | SaveOptions | Die Speicheroptionen. |
| mergeFormatMode | MergeFormatMode | Gibt an, wie kollidierende Formatierungen zusammengeführt werden. |

## Bemerkungen

Wenn das Ausgabeformat ein Bild ist (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP), wird nur die erste Seite der Ausgabe im angegebenen Stream gespeichert.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als einzelnes TIFF mit mehreren Frames im angegebenen Stream gespeichert.

## Beispiele

Zeigt, wie Dokumente aus einem Stream in ein einzelnes Ausgabedokument zusammengeführt werden.

```csharp
//Es gibt mehrere Möglichkeiten, Dokumente aus einem Stream zusammenzuführen:
using (FileStream firstStreamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream secondStreamIn = new FileStream(MyDir + "Tables.docx", FileMode.Open, FileAccess.Read))
    {
        OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamDocument.1.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Merge(streamOut, new[] { firstStreamIn, secondStreamIn }, saveOptions, MergeFormatMode.KeepSourceFormatting);

        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamDocument.2.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Merge(streamOut, new[] { firstStreamIn, secondStreamIn }, SaveFormat.Docx);

        LoadOptions firstLoadOptions = new LoadOptions() { IgnoreOleData = true };
        LoadOptions secondLoadOptions = new LoadOptions() { IgnoreOleData = false };
        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamDocument.3.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Merge(streamOut, new[] { firstStreamIn, secondStreamIn }, new[] { firstLoadOptions, secondLoadOptions }, saveOptions, MergeFormatMode.KeepSourceFormatting);

        Document firstDoc = Merger.Merge(new[] { firstStreamIn, secondStreamIn }, MergeFormatMode.MergeFormatting);
        firstDoc.Save(ArtifactsDir + "LowCode.MergeStreamDocument.4.docx");

        Document secondDoc = Merger.Merge(new[] { firstStreamIn, secondStreamIn }, new[] { firstLoadOptions, secondLoadOptions }, MergeFormatMode.MergeFormatting);
        secondDoc.Save(ArtifactsDir + "LowCode.MergeStreamDocument.5.docx");
    }
}
```

### Siehe auch

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* enum [MergeFormatMode](../../mergeformatmode/)
* class [Merger](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)

---

## Merge(*Stream, Stream[], LoadOptions[], [SaveOptions](../../../aspose.words.saving/saveoptions/), [MergeFormatMode](../../mergeformatmode/)*) {#merge_5}

Fügt die angegebenen Eingabedokumente unter Verwendung der angegebenen Eingabe-/Ausgabeströme und Speicheroptionen zu einem einzigen Ausgabedokument zusammen.

```csharp
public static void Merge(Stream outputStream, Stream[] inputStreams, LoadOptions[] loadOptions, 
    SaveOptions saveOptions, MergeFormatMode mergeFormatMode)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| outputStream | Stream | Der Ausgabestream. |
| inputStreams | Stream[] | Die Eingabestreams. |
| loadOptions | LoadOptions[] | Ladeoptionen für die Eingabedateien. |
| saveOptions | SaveOptions | Die Speicheroptionen. |
| mergeFormatMode | MergeFormatMode | Gibt an, wie kollidierende Formatierungen zusammengeführt werden. |

## Bemerkungen

Wenn das Ausgabeformat ein Bild ist (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP), wird nur die erste Seite der Ausgabe im angegebenen Stream gespeichert.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als einzelnes TIFF mit mehreren Frames im angegebenen Stream gespeichert.

## Beispiele

Zeigt, wie Dokumente aus einem Stream in ein einzelnes Ausgabedokument zusammengeführt werden.

```csharp
//Es gibt mehrere Möglichkeiten, Dokumente aus einem Stream zusammenzuführen:
using (FileStream firstStreamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream secondStreamIn = new FileStream(MyDir + "Tables.docx", FileMode.Open, FileAccess.Read))
    {
        OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamDocument.1.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Merge(streamOut, new[] { firstStreamIn, secondStreamIn }, saveOptions, MergeFormatMode.KeepSourceFormatting);

        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamDocument.2.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Merge(streamOut, new[] { firstStreamIn, secondStreamIn }, SaveFormat.Docx);

        LoadOptions firstLoadOptions = new LoadOptions() { IgnoreOleData = true };
        LoadOptions secondLoadOptions = new LoadOptions() { IgnoreOleData = false };
        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamDocument.3.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Merge(streamOut, new[] { firstStreamIn, secondStreamIn }, new[] { firstLoadOptions, secondLoadOptions }, saveOptions, MergeFormatMode.KeepSourceFormatting);

        Document firstDoc = Merger.Merge(new[] { firstStreamIn, secondStreamIn }, MergeFormatMode.MergeFormatting);
        firstDoc.Save(ArtifactsDir + "LowCode.MergeStreamDocument.4.docx");

        Document secondDoc = Merger.Merge(new[] { firstStreamIn, secondStreamIn }, new[] { firstLoadOptions, secondLoadOptions }, MergeFormatMode.MergeFormatting);
        secondDoc.Save(ArtifactsDir + "LowCode.MergeStreamDocument.5.docx");
    }
}
```

### Siehe auch

* class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* enum [MergeFormatMode](../../mergeformatmode/)
* class [Merger](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)

---

## Merge(*Stream[], [MergeFormatMode](../../mergeformatmode/)*) {#merge_2}

Fügt die angegebenen Eingabedokumente zu einem einzigen Dokument zusammen und gibt[`Document`](../../../aspose.words/document/) Instanz des endgültigen Dokuments.

```csharp
public static Document Merge(Stream[] inputStreams, MergeFormatMode mergeFormatMode)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputStreams | Stream[] | Die Eingabestreams. |
| mergeFormatMode | MergeFormatMode | Gibt an, wie kollidierende Formatierungen zusammengeführt werden. |

## Beispiele

Zeigt, wie Dokumente aus einem Stream in ein einzelnes Ausgabedokument zusammengeführt werden.

```csharp
//Es gibt mehrere Möglichkeiten, Dokumente aus einem Stream zusammenzuführen:
using (FileStream firstStreamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream secondStreamIn = new FileStream(MyDir + "Tables.docx", FileMode.Open, FileAccess.Read))
    {
        OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamDocument.1.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Merge(streamOut, new[] { firstStreamIn, secondStreamIn }, saveOptions, MergeFormatMode.KeepSourceFormatting);

        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamDocument.2.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Merge(streamOut, new[] { firstStreamIn, secondStreamIn }, SaveFormat.Docx);

        LoadOptions firstLoadOptions = new LoadOptions() { IgnoreOleData = true };
        LoadOptions secondLoadOptions = new LoadOptions() { IgnoreOleData = false };
        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamDocument.3.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Merge(streamOut, new[] { firstStreamIn, secondStreamIn }, new[] { firstLoadOptions, secondLoadOptions }, saveOptions, MergeFormatMode.KeepSourceFormatting);

        Document firstDoc = Merger.Merge(new[] { firstStreamIn, secondStreamIn }, MergeFormatMode.MergeFormatting);
        firstDoc.Save(ArtifactsDir + "LowCode.MergeStreamDocument.4.docx");

        Document secondDoc = Merger.Merge(new[] { firstStreamIn, secondStreamIn }, new[] { firstLoadOptions, secondLoadOptions }, MergeFormatMode.MergeFormatting);
        secondDoc.Save(ArtifactsDir + "LowCode.MergeStreamDocument.5.docx");
    }
}
```

### Siehe auch

* class [Document](../../../aspose.words/document/)
* enum [MergeFormatMode](../../mergeformatmode/)
* class [Merger](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)

---

## Merge(*Stream[], LoadOptions[], [MergeFormatMode](../../mergeformatmode/)*) {#merge_1}

Fügt die angegebenen Eingabedokumente zu einem einzigen Dokument zusammen und gibt[`Document`](../../../aspose.words/document/) Instanz des endgültigen Dokuments.

```csharp
public static Document Merge(Stream[] inputStreams, LoadOptions[] loadOptions, 
    MergeFormatMode mergeFormatMode)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputStreams | Stream[] | Die Eingabestreams. |
| loadOptions | LoadOptions[] | Ladeoptionen für die Eingabedateien. |
| mergeFormatMode | MergeFormatMode | Gibt an, wie kollidierende Formatierungen zusammengeführt werden. |

## Beispiele

Zeigt, wie Dokumente aus einem Stream in ein einzelnes Ausgabedokument zusammengeführt werden.

```csharp
//Es gibt mehrere Möglichkeiten, Dokumente aus einem Stream zusammenzuführen:
using (FileStream firstStreamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream secondStreamIn = new FileStream(MyDir + "Tables.docx", FileMode.Open, FileAccess.Read))
    {
        OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamDocument.1.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Merge(streamOut, new[] { firstStreamIn, secondStreamIn }, saveOptions, MergeFormatMode.KeepSourceFormatting);

        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamDocument.2.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Merge(streamOut, new[] { firstStreamIn, secondStreamIn }, SaveFormat.Docx);

        LoadOptions firstLoadOptions = new LoadOptions() { IgnoreOleData = true };
        LoadOptions secondLoadOptions = new LoadOptions() { IgnoreOleData = false };
        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamDocument.3.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Merge(streamOut, new[] { firstStreamIn, secondStreamIn }, new[] { firstLoadOptions, secondLoadOptions }, saveOptions, MergeFormatMode.KeepSourceFormatting);

        Document firstDoc = Merger.Merge(new[] { firstStreamIn, secondStreamIn }, MergeFormatMode.MergeFormatting);
        firstDoc.Save(ArtifactsDir + "LowCode.MergeStreamDocument.4.docx");

        Document secondDoc = Merger.Merge(new[] { firstStreamIn, secondStreamIn }, new[] { firstLoadOptions, secondLoadOptions }, MergeFormatMode.MergeFormatting);
        secondDoc.Save(ArtifactsDir + "LowCode.MergeStreamDocument.5.docx");
    }
}
```

### Siehe auch

* class [Document](../../../aspose.words/document/)
* class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* enum [MergeFormatMode](../../mergeformatmode/)
* class [Merger](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)
