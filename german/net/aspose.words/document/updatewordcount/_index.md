---
title: UpdateWordCount
second_title: Aspose.Words für .NET-API-Referenz
description: Aktualisiert die Eigenschaften der Wortanzahl des Dokuments.
type: docs
weight: 770
url: /de/net/aspose.words/document/updatewordcount/
---
## UpdateWordCount() {#updatewordcount}

Aktualisiert die Eigenschaften der Wortanzahl des Dokuments.

```csharp
public void UpdateWordCount()
```

### Bemerkungen

**WordCount aktualisieren** berechnet und aktualisiert die Eigenschaften Characters, Words und Paragraphs in der[`BuiltInDocumentProperties`](../builtindocumentproperties) Sammlung der **Dokumentieren**.

Beachten Sie, dass **WordCount aktualisieren** aktualisiert die Zeilenanzahl und Seiteneigenschaften nicht. Verwenden Sie die`UpdateWordCount` überladen und True-Wert als Parameter übergeben, um dies zu tun.

Wenn Sie eine Evaluierungsversion verwenden, wird das Evaluierungswasserzeichen auch in die Wortzählung aufgenommen.

### Beispiele

Zeigt, wie alle Listenbezeichnungen in einem Dokument aktualisiert werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
builder.Write("Ut enim ad minim veniam, " +
                "quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

// Aspose.Words verfolgt Dokumentmetriken wie diese nicht in Echtzeit.
Assert.AreEqual(0, doc.BuiltInDocumentProperties.Characters);
Assert.AreEqual(0, doc.BuiltInDocumentProperties.Words);
Assert.AreEqual(1, doc.BuiltInDocumentProperties.Paragraphs);
Assert.AreEqual(1, doc.BuiltInDocumentProperties.Lines);

// Um genaue Werte für drei dieser Eigenschaften zu erhalten, müssen wir sie manuell aktualisieren.
doc.UpdateWordCount();

Assert.AreEqual(196, doc.BuiltInDocumentProperties.Characters);
Assert.AreEqual(36, doc.BuiltInDocumentProperties.Words);
Assert.AreEqual(2, doc.BuiltInDocumentProperties.Paragraphs);

// Für die Zeilenanzahl müssen wir eine bestimmte Überladung der Aktualisierungsmethode aufrufen.
Assert.AreEqual(1, doc.BuiltInDocumentProperties.Lines);

doc.UpdateWordCount(true);

Assert.AreEqual(4, doc.BuiltInDocumentProperties.Lines);
```

### Siehe auch

* class [Document](../../document)
* namensraum [Aspose.Words](../../document)
* Montage [Aspose.Words](../../../)

---

## UpdateWordCount(bool) {#updatewordcount_1}

Aktualisiert die Wortzähleigenschaften des Dokuments, optional aktualisiert[`Lines`](../../../aspose.words.properties/builtindocumentproperties/lines) Eigentum.

```csharp
public void UpdateWordCount(bool updateLinesCount)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| updateLinesCount | Boolean | True, wenn die Anzahl der Zeilen im Dokument berechnet werden soll. |

### Bemerkungen

Diese Methode baut das Seitenlayout des Dokuments neu auf.

### Beispiele

Zeigt, wie alle Listenbezeichnungen in einem Dokument aktualisiert werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
builder.Write("Ut enim ad minim veniam, " +
                "quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

// Aspose.Words verfolgt Dokumentmetriken wie diese nicht in Echtzeit.
Assert.AreEqual(0, doc.BuiltInDocumentProperties.Characters);
Assert.AreEqual(0, doc.BuiltInDocumentProperties.Words);
Assert.AreEqual(1, doc.BuiltInDocumentProperties.Paragraphs);
Assert.AreEqual(1, doc.BuiltInDocumentProperties.Lines);

// Um genaue Werte für drei dieser Eigenschaften zu erhalten, müssen wir sie manuell aktualisieren.
doc.UpdateWordCount();

Assert.AreEqual(196, doc.BuiltInDocumentProperties.Characters);
Assert.AreEqual(36, doc.BuiltInDocumentProperties.Words);
Assert.AreEqual(2, doc.BuiltInDocumentProperties.Paragraphs);

// Für die Zeilenanzahl müssen wir eine bestimmte Überladung der Aktualisierungsmethode aufrufen.
Assert.AreEqual(1, doc.BuiltInDocumentProperties.Lines);

doc.UpdateWordCount(true);

Assert.AreEqual(4, doc.BuiltInDocumentProperties.Lines);
```

### Siehe auch

* class [Document](../../document)
* namensraum [Aspose.Words](../../document)
* Montage [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->