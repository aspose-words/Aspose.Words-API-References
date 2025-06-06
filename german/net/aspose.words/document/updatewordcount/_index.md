---
title: Document.UpdateWordCount
linktitle: UpdateWordCount
articleTitle: UpdateWordCount
second_title: Aspose.Words für .NET
description: Verbessern Sie die Effizienz Ihres Dokuments mit der Methode UpdateWordCount und stellen Sie genaue Wortanzahleigenschaften für eine bessere Bearbeitung und Überprüfung sicher.
type: docs
weight: 850
url: /de/net/aspose.words/document/updatewordcount/
---
## UpdateWordCount() {#updatewordcount}

Aktualisiert die Wortanzahleigenschaften des Dokuments.

```csharp
public void UpdateWordCount()
```

## Bemerkungen

`UpdateWordCount` berechnet und aktualisiert die Eigenschaften „Characters“, „Words“ und „Paradix“ in der[`BuiltInDocumentProperties`](../builtindocumentproperties/) Sammlung der[`Document`](../).

Beachten Sie, dass`UpdateWordCount` aktualisiert die Eigenschaften für Zeilenanzahl und Seiten nicht. Verwenden Sie die`UpdateWordCount` Überlastung und Pass`WAHR` Wert als Parameter, um dies zu tun.

Wenn Sie eine Testversion verwenden, wird das Testwasserzeichen ebenfalls in die Wortanzahl einbezogen .

## Beispiele

Zeigt, wie alle Listenbeschriftungen in einem Dokument aktualisiert werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
builder.Write("Ut enim ad minim veniam, " +
                "quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

// Aspose.Words verfolgt solche Dokumentmetriken nicht in Echtzeit.
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

* class [Document](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)

---

## UpdateWordCount(*bool*) {#updatewordcount_1}

Aktualisiert die Wortanzahleigenschaften des Dokuments, aktualisiert optional[`Lines`](../../../aspose.words.properties/builtindocumentproperties/lines/) Eigenschaft.

```csharp
public void UpdateWordCount(bool updateLinesCount)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| updateLinesCount | Boolean | `WAHR` wenn die Zeilenanzahl im Dokument berechnet werden soll. |

## Bemerkungen

Diese Methode erstellt das Seitenlayout des Dokuments neu.

## Beispiele

Zeigt, wie alle Listenbeschriftungen in einem Dokument aktualisiert werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
builder.Write("Ut enim ad minim veniam, " +
                "quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

// Aspose.Words verfolgt solche Dokumentmetriken nicht in Echtzeit.
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

* class [Document](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
