---
title: BuiltInDocumentProperties.Paragraphs
linktitle: Paragraphs
articleTitle: Paragraphs
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „BuiltInDocumentProperties Paragraphs“, die eine genaue Schätzung der Absatzanzahl in Ihrem Dokument für eine bessere Inhaltsverwaltung bietet.
type: docs
weight: 240
url: /de/net/aspose.words.properties/builtindocumentproperties/paragraphs/
---
## BuiltInDocumentProperties.Paragraphs property

Stellt eine Schätzung der Anzahl der Absätze im Dokument dar.

```csharp
public int Paragraphs { get; set; }
```

## Bemerkungen

Aspose.Words aktualisiert diese Eigenschaft, wenn Sie aufrufen[`UpdateWordCount`](../../../aspose.words/document/updatewordcount/).

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

Zeigt, wie mit Dokumenteigenschaften in der Kategorie „Inhalt“ gearbeitet wird.

```csharp
public void Content()
{
    Document doc = new Document(MyDir + "Paragraphs.docx");
    BuiltInDocumentProperties properties = doc.BuiltInDocumentProperties;

    // Durch die Verwendung integrierter Eigenschaften,
    // Wir können Dokumentstatistiken wie die Anzahl von Wörtern/Seiten/Zeichen als Metadaten behandeln, die man sich ansehen kann, ohne das Dokument zu öffnen
    // Auf diese Eigenschaften kann zugegriffen werden, indem Sie im Windows Explorer mit der rechten Maustaste auf die Datei klicken und zu Eigenschaften > Details > Inhalt navigieren.
    // Wenn wir diese Daten im Dokument anzeigen möchten, können wir Felder wie NUMPAGES, NUMWORDS, NUMCHARS usw. verwenden.
    // Diese Werte können auch in Microsoft Word angezeigt werden, indem Sie zu Datei > Eigenschaften > Erweiterte Eigenschaften > Statistik navigieren.
    // Seitenanzahl: Die Eigenschaft PageCount zeigt die Seitenanzahl in Echtzeit an und ihr Wert kann der Eigenschaft Pages zugewiesen werden

        // Die Eigenschaft „Seiten“ speichert die Seitenanzahl des Dokuments.
    Assert.AreEqual(6, properties.Pages);

    // Die integrierten Eigenschaften „Wörter“, „Zeichen“ und „Zeichen mit Leerzeichen“ zeigen auch verschiedene Dokumentstatistiken an.
    // aber wir müssen die Methode „UpdateWordCount“ für das gesamte Dokument aufrufen, bevor wir erwarten können, dass sie genaue Werte enthalten.
    doc.UpdateWordCount();

    Assert.AreEqual(1035, properties.Words);
    Assert.AreEqual(6026, properties.Characters);
    Assert.AreEqual(7041, properties.CharactersWithSpaces);

    // Zählen Sie die Anzahl der Zeilen im Dokument und weisen Sie das Ergebnis dann der integrierten Eigenschaft „Lines“ zu.
    LineCounter lineCounter = new LineCounter(doc);
    properties.Lines = lineCounter.GetLineCount();

    Assert.AreEqual(142, properties.Lines);

    // Weisen Sie der integrierten Eigenschaft „Paragraphs“ die Anzahl der Absatzknoten im Dokument zu.
    properties.Paragraphs = doc.GetChildNodes(NodeType.Paragraph, true).Count;
    Assert.AreEqual(29, properties.Paragraphs);

    // Erhalten Sie eine Schätzung der Dateigröße unseres Dokuments über die integrierte Eigenschaft „Bytes“.
    Assert.AreEqual(20310, properties.Bytes);

    // Legen Sie eine andere Vorlage für unser Dokument fest und aktualisieren Sie dann die integrierte Eigenschaft „Vorlage“ manuell, um diese Änderung widerzuspiegeln.
    doc.AttachedTemplate = MyDir + "Business brochure.dotx";

    Assert.AreEqual("Normal", properties.Template);

    properties.Template = doc.AttachedTemplate;

    // „ContentStatus“ ist eine beschreibende integrierte Eigenschaft.
    properties.ContentStatus = "Draft";

    // Beim Speichern enthält die integrierte Eigenschaft „ContentType“ den MIME-Typ des Ausgabespeicherformats.
    Assert.AreEqual(string.Empty, properties.ContentType);

    // Wenn das Dokument Links enthält und diese alle auf dem neuesten Stand sind, können wir die Eigenschaft „LinksUpToDate“ auf „true“ setzen.
    Assert.False(properties.LinksUpToDate);

    doc.Save(ArtifactsDir + "DocumentProperties.Content.docx");
}

/// <summary>
/// Zählt die Zeilen in einem Dokument.
/// Durchläuft den Layout-Entitätenbaum des Dokuments bei der Erstellung,
/// Zählen von Entitäten des Typs „Zeile“, die auch echten Text enthalten.
/// </summary>
private class LineCounter
{
    public LineCounter(Document doc)
    {
        mLayoutEnumerator = new LayoutEnumerator(doc);

        CountLines();
    }

    public int GetLineCount()
    {
        return mLineCount;
    }

    private void CountLines()
    {
        do
        {
            if (mLayoutEnumerator.Type == LayoutEntityType.Line)
            {
                mScanningLineForRealText = true;
            }

            if (mLayoutEnumerator.MoveFirstChild())
            {
                if (mScanningLineForRealText && mLayoutEnumerator.Kind.StartsWith("TEXT"))
                {
                    mLineCount++;
                    mScanningLineForRealText = false;
                }
                CountLines();
                mLayoutEnumerator.MoveParent();
            }
        } while (mLayoutEnumerator.MoveNext());
    }

    private readonly LayoutEnumerator mLayoutEnumerator;
    private int mLineCount;
    private bool mScanningLineForRealText;
}
```

### Siehe auch

* class [BuiltInDocumentProperties](../)
* namensraum [Aspose.Words.Properties](../../../aspose.words.properties/)
* Montage [Aspose.Words](../../../)
