---
title: Splitter.RemoveBlankPages
linktitle: RemoveBlankPages
articleTitle: RemoveBlankPages
second_title: Aspose.Words für .NET
description: Entfernen Sie mühelos leere Seiten aus Ihren Dokumenten mit der Splitter-Methode „RemoveBlankPages“. Sparen Sie Zeit und verbessern Sie Ihren Workflow!
type: docs
weight: 30
url: /de/net/aspose.words.lowcode/splitter/removeblankpages/
---
## RemoveBlankPages(*string, string*) {#removeblankpages_2}

Entfernt leere Seiten aus dem Dokument und speichert die Ausgabe. Gibt eine Liste der entfernten Seitenzahlen zurück.

```csharp
public static List<int> RemoveBlankPages(string inputFileName, string outputFileName)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFileName | String | Der Name der Eingabedatei. |
| outputFileName | String | Der Name der Ausgabedatei. |

### Rückgabewert

Die Liste der Seitenzahlen wurde als leer betrachtet und entfernt.

## Beispiele

Zeigt, wie leere Seiten aus dem Dokument entfernt werden.

```csharp
// Es gibt mehrere Möglichkeiten, leere Seiten aus dem Dokument zu entfernen:
string doc = MyDir + "Blank pages.docx";

Splitter.RemoveBlankPages(doc, ArtifactsDir + "LowCode.RemoveBlankPages.1.docx");
Splitter.RemoveBlankPages(doc, ArtifactsDir + "LowCode.RemoveBlankPages.2.docx", SaveFormat.Docx);
```

### Siehe auch

* class [Splitter](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)

---

## RemoveBlankPages(*string, string, [SaveFormat](../../../aspose.words/saveformat/)*) {#removeblankpages_3}

Entfernt leere Seiten aus dem Dokument und speichert die Ausgabe im angegebenen Format. Gibt eine Liste der entfernten Seitenzahlen zurück.

```csharp
public static List<int> RemoveBlankPages(string inputFileName, string outputFileName, 
    SaveFormat saveFormat)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFileName | String | Der Name der Eingabedatei. |
| outputFileName | String | Der Name der Ausgabedatei. |
| saveFormat | SaveFormat | Das Speicherformat. |

### Rückgabewert

Die Liste der Seitenzahlen wurde als leer betrachtet und entfernt.

## Beispiele

Zeigt, wie leere Seiten aus dem Dokument entfernt werden.

```csharp
// Es gibt mehrere Möglichkeiten, leere Seiten aus dem Dokument zu entfernen:
string doc = MyDir + "Blank pages.docx";

Splitter.RemoveBlankPages(doc, ArtifactsDir + "LowCode.RemoveBlankPages.1.docx");
Splitter.RemoveBlankPages(doc, ArtifactsDir + "LowCode.RemoveBlankPages.2.docx", SaveFormat.Docx);
```

### Siehe auch

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [Splitter](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)

---

## RemoveBlankPages(*string, string, [SaveOptions](../../../aspose.words.saving/saveoptions/)*) {#removeblankpages_4}

Entfernt leere Seiten aus dem Dokument und speichert die Ausgabe im angegebenen Format. Gibt eine Liste der entfernten Seitenzahlen zurück.

```csharp
public static List<int> RemoveBlankPages(string inputFileName, string outputFileName, 
    SaveOptions saveOptions)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFileName | String | Der Name der Eingabedatei. |
| outputFileName | String | Der Name der Ausgabedatei. |
| saveOptions | SaveOptions | Die Speicheroptionen. |

### Rückgabewert

Die Liste der Seitenzahlen wurde als leer betrachtet und entfernt.

### Siehe auch

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Splitter](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)

---

## RemoveBlankPages(*Stream, Stream, [SaveFormat](../../../aspose.words/saveformat/)*) {#removeblankpages}

Entfernt leere Seiten aus einem Dokument, das in einem Eingabestream bereitgestellt wird, und speichert das aktualisierte Dokument im angegebenen Speicherformat in einem Ausgabestream. Gibt eine Liste der entfernten Seitenzahlen zurück.

```csharp
public static List<int> RemoveBlankPages(Stream inputStream, Stream outputStream, 
    SaveFormat saveFormat)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputStream | Stream | Der Eingabestream. |
| outputStream | Stream | Der Ausgabestream. |
| saveFormat | SaveFormat | Das Speicherformat. |

### Rückgabewert

Die Liste der Seitenzahlen wurde als leer betrachtet und entfernt.

## Beispiele

Zeigt, wie leere Seiten aus dem Dokument aus dem Stream entfernt werden.

```csharp
using (FileStream streamIn = new FileStream(MyDir + "Blank pages.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.RemoveBlankPagesStream.docx", FileMode.Create, FileAccess.ReadWrite))
        Splitter.RemoveBlankPages(streamIn, streamOut, SaveFormat.Docx);
}
```

### Siehe auch

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [Splitter](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)

---

## RemoveBlankPages(*Stream, Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/)*) {#removeblankpages_1}

Entfernt leere Seiten aus einem Dokument, das in einem Eingabestream bereitgestellt wird, und speichert das aktualisierte Dokument im angegebenen Speicherformat in einem Ausgabestream. Gibt eine Liste der entfernten Seitenzahlen zurück.

```csharp
public static List<int> RemoveBlankPages(Stream inputStream, Stream outputStream, 
    SaveOptions saveOptions)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputStream | Stream | Der Eingabestream. |
| outputStream | Stream | Der Ausgabestream. |
| saveOptions | SaveOptions | Die Speicheroptionen. |

### Rückgabewert

Die Liste der Seitenzahlen wurde als leer betrachtet und entfernt.

### Siehe auch

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Splitter](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)
