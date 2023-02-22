---
title: BuiltInDocumentProperties.ContentType
second_title: Aspose.Words für .NET-API-Referenz
description: BuiltInDocumentProperties eigendom. Ruft den ContentStatus des Dokuments ab oder legt ihn fest.
type: docs
weight: 90
url: /de/net/aspose.words.properties/builtindocumentproperties/contenttype/
---
## BuiltInDocumentProperties.ContentType property

Ruft den ContentStatus des Dokuments ab oder legt ihn fest.

```csharp
public string ContentType { get; set; }
```

### Beispiele

Zeigt, wie Sie mit Dokumenteigenschaften in der Kategorie "Inhalt" arbeiten.

```csharp
public void Content()
{
    Document doc = new Document(MyDir + "Paragraphs.docx");
    BuiltInDocumentProperties properties = doc.BuiltInDocumentProperties;

    // Durch die Verwendung eingebauter Eigenschaften,
    // Wir können Dokumentstatistiken wie Wort-/Seiten-/Zeichenanzahl als Metadaten behandeln, die eingesehen werden können, ohne das Dokument zu öffnen
    // Auf diese Eigenschaften greifen Sie zu, indem Sie im Windows Explorer mit der rechten Maustaste auf die Datei klicken und zu Eigenschaften > Einzelheiten > Inhalt
    // Wenn wir diese Daten innerhalb des Dokuments anzeigen möchten, können wir Felder wie NUMPAGES, NUMWORDS, NUMCHARS usw. verwenden.
    // Diese Werte können auch in Microsoft Word angezeigt werden, indem Sie zu Datei > Eigenschaften > Erweiterte Eigenschaften > Statistiken
    // Seitenzahl: Die Eigenschaft PageCount zeigt die Seitenzahl in Echtzeit an und ihr Wert kann der Eigenschaft Pages zugewiesen werden

    // Die Eigenschaft "Pages" speichert die Seitenanzahl des Dokuments. 
    Assert.AreEqual(6, properties.Pages);

    // Die integrierten Eigenschaften "Wörter", "Zeichen" und "ZeichenMitLeerzeichen" zeigen auch verschiedene Dokumentstatistiken an,
    // aber wir müssen die "UpdateWordCount"-Methode für das gesamte Dokument aufrufen, bevor wir erwarten können, dass sie genaue Werte enthalten.
    doc.UpdateWordCount();

    Assert.AreEqual(1035, properties.Words);
    Assert.AreEqual(6026, properties.Characters);
    Assert.AreEqual(7041, properties.CharactersWithSpaces);

    // Zählen Sie die Anzahl der Zeilen im Dokument und weisen Sie das Ergebnis dann der integrierten Eigenschaft "Lines" zu.
    LineCounter lineCounter = new LineCounter(doc);
    properties.Lines = lineCounter.GetLineCount();

    Assert.AreEqual(142, properties.Lines);

    // Weisen Sie der eingebauten Eigenschaft "Paragraphs" die Anzahl der Paragraph-Knoten im Dokument zu.
    properties.Paragraphs = doc.GetChildNodes(NodeType.Paragraph, true).Count;
    Assert.AreEqual(29, properties.Paragraphs);

    // Erhalten Sie eine Schätzung der Dateigröße unseres Dokuments über die eingebaute Eigenschaft "Bytes".
    Assert.AreEqual(20310, properties.Bytes);

    // Legen Sie eine andere Vorlage für unser Dokument fest und aktualisieren Sie dann die integrierte Eigenschaft "Vorlage" manuell, um diese Änderung widerzuspiegeln.
    doc.AttachedTemplate = MyDir + "Business brochure.dotx";

    Assert.AreEqual("Normal", properties.Template);    

    properties.Template = doc.AttachedTemplate;

    // "ContentStatus" ist eine beschreibende eingebaute Eigenschaft.
    properties.ContentStatus = "Draft";

    // Beim Speichern enthält die integrierte Eigenschaft "ContentType" den MIME-Typ des Ausgabespeicherformats.
    Assert.AreEqual(string.Empty, properties.ContentType);

    // Wenn das Dokument Links enthält und alle aktuell sind, können wir die Eigenschaft "LinksUpToDate" auf "true" setzen.
    Assert.False(properties.LinksUpToDate);

    doc.Save(ArtifactsDir + "DocumentProperties.Content.docx");
}

/// <summary>
/// Zählt die Zeilen in einem Dokument.
/// Durchläuft den Layoutentitätsbaum des Dokuments bei der Konstruktion,
/// Zählen von Entitäten des Typs "Zeile", die auch echten Text enthalten.
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
* namensraum [Aspose.Words.Properties](../../builtindocumentproperties/)
* Montage [Aspose.Words](../../../)


