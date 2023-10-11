---
title: Merger.Merge
second_title: Aspose.Words für .NET-API-Referenz
description: Merger methode. Führt die angegebenen Eingabedokumente unter Verwendung der angegebenen Eingabe und Ausgabedateinamen zu einem einzigen Ausgabedokument zusammen.
type: docs
weight: 10
url: /de/net/aspose.words.lowcode/merger/merge/
---
## Merge(string, string[]) {#merge_4}

Führt die angegebenen Eingabedokumente unter Verwendung der angegebenen Eingabe- und Ausgabedateinamen zu einem einzigen Ausgabedokument zusammen.

```csharp
public static void Merge(string outputFile, string[] inputFiles)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| outputFile | String | Der Name der Ausgabedatei. |
| inputFiles | String[] | Die Namen der Eingabedateien. |

### Bemerkungen

StandardmäßigKeepSourceFormatting wird eingesetzt.

### Beispiele

Zeigt, wie Dokumente zu einem einzigen Ausgabedokument zusammengeführt werden.

```csharp
//Es gibt mehrere Möglichkeiten, Dokumente zusammenzuführen:
Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.SimpleMerge.docx", new[] { MyDir + "Big document.docx", MyDir + "Tables.docx" });

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.SaveOptions.docx", new[] { MyDir + "Big document.docx", MyDir + "Tables.docx" }, new OoxmlSaveOptions() { Password = "Aspose.Words" }, MergeFormatMode.KeepSourceFormatting);

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.SaveFormat.pdf", new[] { MyDir + "Big document.docx", MyDir + "Tables.docx" }, SaveFormat.Pdf, MergeFormatMode.KeepSourceLayout);

Document doc = Merger.Merge(new[] { MyDir + "Big document.docx", MyDir + "Tables.docx" }, MergeFormatMode.MergeFormatting);
doc.Save(ArtifactsDir + "LowCode.MergeDocument.DocumentInstance.docx");
```

### Siehe auch

* class [Merger](../)
* namensraum [Aspose.Words.LowCode](../../merger/)
* Montage [Aspose.Words](../../../)

---

## Merge(string, string[], SaveFormat, MergeFormatMode) {#merge_5}

Führt die angegebenen Eingabedokumente unter Verwendung der angegebenen Eingabe-Ausgabedateinamen und des endgültigen Dokumentformats zu einem einzigen Ausgabedokument zusammen.

```csharp
public static void Merge(string outputFile, string[] inputFiles, SaveFormat saveFormat, 
    MergeFormatMode mergeFormatMode)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| outputFile | String | Der Name der Ausgabedatei. |
| inputFiles | String[] | Die Namen der Eingabedateien. |
| saveFormat | SaveFormat | Das Speicherformat. |
| mergeFormatMode | MergeFormatMode | Gibt an, wie widersprüchliche Formatierungen zusammengeführt werden. |

### Beispiele

Zeigt, wie Dokumente zu einem einzigen Ausgabedokument zusammengeführt werden.

```csharp
//Es gibt mehrere Möglichkeiten, Dokumente zusammenzuführen:
Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.SimpleMerge.docx", new[] { MyDir + "Big document.docx", MyDir + "Tables.docx" });

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.SaveOptions.docx", new[] { MyDir + "Big document.docx", MyDir + "Tables.docx" }, new OoxmlSaveOptions() { Password = "Aspose.Words" }, MergeFormatMode.KeepSourceFormatting);

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.SaveFormat.pdf", new[] { MyDir + "Big document.docx", MyDir + "Tables.docx" }, SaveFormat.Pdf, MergeFormatMode.KeepSourceLayout);

Document doc = Merger.Merge(new[] { MyDir + "Big document.docx", MyDir + "Tables.docx" }, MergeFormatMode.MergeFormatting);
doc.Save(ArtifactsDir + "LowCode.MergeDocument.DocumentInstance.docx");
```

### Siehe auch

* enum [SaveFormat](../../../aspose.words/saveformat/)
* enum [MergeFormatMode](../../mergeformatmode/)
* class [Merger](../)
* namensraum [Aspose.Words.LowCode](../../merger/)
* Montage [Aspose.Words](../../../)

---

## Merge(string, string[], SaveOptions, MergeFormatMode) {#merge_6}

Führt die angegebenen Eingabedokumente unter Verwendung der angegebenen Eingabe-Ausgabedateinamen und Speicheroptionen zu einem einzigen Ausgabedokument zusammen.

```csharp
public static void Merge(string outputFile, string[] inputFiles, SaveOptions saveOptions, 
    MergeFormatMode mergeFormatMode)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| outputFile | String | Der Name der Ausgabedatei. |
| inputFiles | String[] | Die Namen der Eingabedateien. |
| saveOptions | SaveOptions | Die Speicheroptionen. |
| mergeFormatMode | MergeFormatMode | Gibt an, wie widersprüchliche Formatierungen zusammengeführt werden. |

### Beispiele

Zeigt, wie Dokumente zu einem einzigen Ausgabedokument zusammengeführt werden.

```csharp
//Es gibt mehrere Möglichkeiten, Dokumente zusammenzuführen:
Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.SimpleMerge.docx", new[] { MyDir + "Big document.docx", MyDir + "Tables.docx" });

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.SaveOptions.docx", new[] { MyDir + "Big document.docx", MyDir + "Tables.docx" }, new OoxmlSaveOptions() { Password = "Aspose.Words" }, MergeFormatMode.KeepSourceFormatting);

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.SaveFormat.pdf", new[] { MyDir + "Big document.docx", MyDir + "Tables.docx" }, SaveFormat.Pdf, MergeFormatMode.KeepSourceLayout);

Document doc = Merger.Merge(new[] { MyDir + "Big document.docx", MyDir + "Tables.docx" }, MergeFormatMode.MergeFormatting);
doc.Save(ArtifactsDir + "LowCode.MergeDocument.DocumentInstance.docx");
```

### Siehe auch

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* enum [MergeFormatMode](../../mergeformatmode/)
* class [Merger](../)
* namensraum [Aspose.Words.LowCode](../../merger/)
* Montage [Aspose.Words](../../../)

---

## Merge(string[], MergeFormatMode) {#merge_1}

Führt die angegebenen Eingabedokumente zu einem einzigen Dokument zusammen und gibt zurück[`Document`](../../../aspose.words/document/) Instanz des endgültigen Dokuments.

```csharp
public static Document Merge(string[] inputFiles, MergeFormatMode mergeFormatMode)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFiles | String[] | Die Namen der Eingabedateien. |
| mergeFormatMode | MergeFormatMode | Gibt an, wie widersprüchliche Formatierungen zusammengeführt werden. |

### Beispiele

Zeigt, wie Dokumente zu einem einzigen Ausgabedokument zusammengeführt werden.

```csharp
//Es gibt mehrere Möglichkeiten, Dokumente zusammenzuführen:
Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.SimpleMerge.docx", new[] { MyDir + "Big document.docx", MyDir + "Tables.docx" });

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.SaveOptions.docx", new[] { MyDir + "Big document.docx", MyDir + "Tables.docx" }, new OoxmlSaveOptions() { Password = "Aspose.Words" }, MergeFormatMode.KeepSourceFormatting);

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.SaveFormat.pdf", new[] { MyDir + "Big document.docx", MyDir + "Tables.docx" }, SaveFormat.Pdf, MergeFormatMode.KeepSourceLayout);

Document doc = Merger.Merge(new[] { MyDir + "Big document.docx", MyDir + "Tables.docx" }, MergeFormatMode.MergeFormatting);
doc.Save(ArtifactsDir + "LowCode.MergeDocument.DocumentInstance.docx");
```

### Siehe auch

* class [Document](../../../aspose.words/document/)
* enum [MergeFormatMode](../../mergeformatmode/)
* class [Merger](../)
* namensraum [Aspose.Words.LowCode](../../merger/)
* Montage [Aspose.Words](../../../)

---

## Merge(Stream, Stream[], SaveFormat) {#merge_2}

Führt die angegebenen Eingabedokumente unter Verwendung der angegebenen Eingabe-Ausgabe-Streams und des endgültigen Dokumentformats zu einem einzigen Ausgabedokument zusammen.

```csharp
public static void Merge(Stream outputStream, Stream[] inputStreams, SaveFormat saveFormat)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| outputStream | Stream | Der Ausgabestream. |
| inputStreams | Stream[] | Die Eingabeströme. |
| saveFormat | SaveFormat | Das Speicherformat. |

### Beispiele

Zeigt, wie Dokumente aus einem Stream in einem einzigen Ausgabedokument zusammengeführt werden.

```csharp
//Es gibt mehrere Möglichkeiten, Dokumente aus einem Stream zusammenzuführen:
using (FileStream firstStreamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream secondStreamIn = new FileStream(MyDir + "Tables.docx", FileMode.Open, FileAccess.Read))
    {
        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamDocument.SaveOptions.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Merge(streamOut, new[] { firstStreamIn, secondStreamIn }, new OoxmlSaveOptions() { Password = "Aspose.Words" }, MergeFormatMode.KeepSourceFormatting);

        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamDocument.SaveFormat.docx", FileMode.Create, FileAccess.ReadWrite))                    
            Merger.Merge(streamOut, new[] { firstStreamIn, secondStreamIn }, SaveFormat.Docx);

        Document doc = Merger.Merge(new[] { firstStreamIn, secondStreamIn }, MergeFormatMode.MergeFormatting);
        doc.Save(ArtifactsDir + "LowCode.MergeStreamDocument.DocumentInstance.docx");
    }
}
```

### Siehe auch

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [Merger](../)
* namensraum [Aspose.Words.LowCode](../../merger/)
* Montage [Aspose.Words](../../../)

---

## Merge(Stream, Stream[], SaveOptions, MergeFormatMode) {#merge_3}

Führt die angegebenen Eingabedokumente unter Verwendung der angegebenen Eingabe-Ausgabe-Streams und Speicheroptionen zu einem einzigen Ausgabedokument zusammen.

```csharp
public static void Merge(Stream outputStream, Stream[] inputStreams, SaveOptions saveOptions, 
    MergeFormatMode mergeFormatMode)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| outputStream | Stream | Der Ausgabestream. |
| inputStreams | Stream[] | Die Eingabeströme. |
| saveOptions | SaveOptions | Die Speicheroptionen. |
| mergeFormatMode | MergeFormatMode | Gibt an, wie widersprüchliche Formatierungen zusammengeführt werden. |

### Beispiele

Zeigt, wie Dokumente aus einem Stream in einem einzigen Ausgabedokument zusammengeführt werden.

```csharp
//Es gibt mehrere Möglichkeiten, Dokumente aus einem Stream zusammenzuführen:
using (FileStream firstStreamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream secondStreamIn = new FileStream(MyDir + "Tables.docx", FileMode.Open, FileAccess.Read))
    {
        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamDocument.SaveOptions.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Merge(streamOut, new[] { firstStreamIn, secondStreamIn }, new OoxmlSaveOptions() { Password = "Aspose.Words" }, MergeFormatMode.KeepSourceFormatting);

        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamDocument.SaveFormat.docx", FileMode.Create, FileAccess.ReadWrite))                    
            Merger.Merge(streamOut, new[] { firstStreamIn, secondStreamIn }, SaveFormat.Docx);

        Document doc = Merger.Merge(new[] { firstStreamIn, secondStreamIn }, MergeFormatMode.MergeFormatting);
        doc.Save(ArtifactsDir + "LowCode.MergeStreamDocument.DocumentInstance.docx");
    }
}
```

### Siehe auch

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* enum [MergeFormatMode](../../mergeformatmode/)
* class [Merger](../)
* namensraum [Aspose.Words.LowCode](../../merger/)
* Montage [Aspose.Words](../../../)

---

## Merge(Stream[], MergeFormatMode) {#merge}

Führt die angegebenen Eingabedokumente zu einem einzigen Dokument zusammen und gibt zurück[`Document`](../../../aspose.words/document/) Instanz des endgültigen Dokuments.

```csharp
public static Document Merge(Stream[] inputStreams, MergeFormatMode mergeFormatMode)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputStreams | Stream[] | Die Eingabeströme. |
| mergeFormatMode | MergeFormatMode | Gibt an, wie widersprüchliche Formatierungen zusammengeführt werden. |

### Beispiele

Zeigt, wie Dokumente aus einem Stream in einem einzigen Ausgabedokument zusammengeführt werden.

```csharp
//Es gibt mehrere Möglichkeiten, Dokumente aus einem Stream zusammenzuführen:
using (FileStream firstStreamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream secondStreamIn = new FileStream(MyDir + "Tables.docx", FileMode.Open, FileAccess.Read))
    {
        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamDocument.SaveOptions.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Merge(streamOut, new[] { firstStreamIn, secondStreamIn }, new OoxmlSaveOptions() { Password = "Aspose.Words" }, MergeFormatMode.KeepSourceFormatting);

        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamDocument.SaveFormat.docx", FileMode.Create, FileAccess.ReadWrite))                    
            Merger.Merge(streamOut, new[] { firstStreamIn, secondStreamIn }, SaveFormat.Docx);

        Document doc = Merger.Merge(new[] { firstStreamIn, secondStreamIn }, MergeFormatMode.MergeFormatting);
        doc.Save(ArtifactsDir + "LowCode.MergeStreamDocument.DocumentInstance.docx");
    }
}
```

### Siehe auch

* class [Document](../../../aspose.words/document/)
* enum [MergeFormatMode](../../mergeformatmode/)
* class [Merger](../)
* namensraum [Aspose.Words.LowCode](../../merger/)
* Montage [Aspose.Words](../../../)


