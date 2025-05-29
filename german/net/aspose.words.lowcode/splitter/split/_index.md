---
title: Splitter.Split
linktitle: Split
articleTitle: Split
second_title: Aspose.Words für .NET
description: Teilen Sie Dokumente mühelos in mehrere Abschnitte auf – mit unserer flexiblen Splitter-Split-Methode. Speichern Sie Dokumente in Ihrem bevorzugten Format für eine einfache Dateiverwaltung!
type: docs
weight: 40
url: /de/net/aspose.words.lowcode/splitter/split/
---
## Split(*string, string, [SplitOptions](../../splitoptions/)*) {#split_2}

Teilt ein Dokument basierend auf den angegebenen Teiloptionen in mehrere Teile auf und speichert die resultierenden Teile in Dateien. Das Ausgabedateiformat wird durch die Erweiterung des Ausgabedateinamens bestimmt.

```csharp
public static void Split(string inputFileName, string outputFileName, SplitOptions options)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFileName | String | Der Name der Eingabedatei. |
| outputFileName | String | Der Ausgabedateiname, der zum Generieren von Dateinamen für Dokumentteile mithilfe der Regel „outputFile_partIndex.extension“ verwendet wird. |
| options | SplitOptions | Optionen zum Aufteilen von Dokumenten. |

## Beispiele

Zeigt, wie ein Dokument nach Seiten aufgeteilt wird.

```csharp
string doc = MyDir + "Big document.docx";

SplitOptions options = new SplitOptions();
options.SplitCriteria = SplitCriteria.Page;
Splitter.Split(doc, ArtifactsDir + "LowCode.SplitDocument.1.docx", options);
Splitter.Split(doc, ArtifactsDir + "LowCode.SplitDocument.2.docx", SaveFormat.Docx, options);
```

### Siehe auch

* class [SplitOptions](../../splitoptions/)
* class [Splitter](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)

---

## Split(*string, string, [SaveFormat](../../../aspose.words/saveformat/), [SplitOptions](../../splitoptions/)*) {#split_3}

Teilt ein Dokument basierend auf den angegebenen Teiloptionen in mehrere Teile auf und speichert die resultierenden Teile in Dateien im angegebenen Speicherformat.

```csharp
public static void Split(string inputFileName, string outputFileName, SaveFormat saveFormat, 
    SplitOptions options)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFileName | String | Der Name der Eingabedatei. |
| outputFileName | String | Der Ausgabedateiname, der zum Generieren von Dateinamen für Dokumentteile mithilfe der Regel „outputFile_partIndex.extension“ verwendet wird. |
| saveFormat | SaveFormat | Das Speicherformat. |
| options | SplitOptions | Optionen zum Aufteilen von Dokumenten. |

## Beispiele

Zeigt, wie ein Dokument nach Seiten aufgeteilt wird.

```csharp
string doc = MyDir + "Big document.docx";

SplitOptions options = new SplitOptions();
options.SplitCriteria = SplitCriteria.Page;
Splitter.Split(doc, ArtifactsDir + "LowCode.SplitDocument.1.docx", options);
Splitter.Split(doc, ArtifactsDir + "LowCode.SplitDocument.2.docx", SaveFormat.Docx, options);
```

### Siehe auch

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [SplitOptions](../../splitoptions/)
* class [Splitter](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)

---

## Split(*string, string, [SaveOptions](../../../aspose.words.saving/saveoptions/), [SplitOptions](../../splitoptions/)*) {#split_4}

Teilt ein Dokument basierend auf den angegebenen Teiloptionen in mehrere Teile auf und speichert die resultierenden Teile in Dateien im angegebenen Speicherformat.

```csharp
public static void Split(string inputFileName, string outputFileName, SaveOptions saveOptions, 
    SplitOptions options)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFileName | String | Der Name der Eingabedatei. |
| outputFileName | String | Der Ausgabedateiname, der zum Generieren von Dateinamen für Dokumentteile mithilfe der Regel „outputFile_partIndex.extension“ verwendet wird. |
| saveOptions | SaveOptions | Die Speicheroptionen. |
| options | SplitOptions | Optionen zum Aufteilen von Dokumenten. |

### Siehe auch

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [SplitOptions](../../splitoptions/)
* class [Splitter](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)

---

## Split(*Stream, [SaveFormat](../../../aspose.words/saveformat/), [SplitOptions](../../splitoptions/)*) {#split}

Teilt ein Dokument aus einem Eingabestream basierend auf den angegebenen Teilungsoptionen in mehrere Teile auf und gibt die resultierenden Teile als Array von Streams im angegebenen Speicherformat zurück.

```csharp
public static Stream[] Split(Stream inputStream, SaveFormat saveFormat, SplitOptions options)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputStream | Stream | Der Eingabestream. |
| saveFormat | SaveFormat | Das Speicherformat. |
| options | SplitOptions | Optionen zum Aufteilen von Dokumenten. |

## Beispiele

Zeigt, wie Dokumente seitenweise aus dem Stream aufgeteilt werden.

```csharp
using (FileStream streamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    SplitOptions options = new SplitOptions();
    options.SplitCriteria = SplitCriteria.Page;
    Stream[] stream = Splitter.Split(streamIn, SaveFormat.Docx, options);
}
```

### Siehe auch

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [SplitOptions](../../splitoptions/)
* class [Splitter](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)

---

## Split(*Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/), [SplitOptions](../../splitoptions/)*) {#split_1}

Teilt ein Dokument aus einem Eingabestream basierend auf den angegebenen Teilungsoptionen in mehrere Teile auf und gibt die resultierenden Teile als Array von Streams im angegebenen Speicherformat zurück.

```csharp
public static Stream[] Split(Stream inputStream, SaveOptions saveOptions, SplitOptions options)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputStream | Stream | Der Eingabestream. |
| saveOptions | SaveOptions | Die Speicheroptionen. |
| options | SplitOptions | Optionen zum Aufteilen von Dokumenten. |

### Siehe auch

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [SplitOptions](../../splitoptions/)
* class [Splitter](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)
