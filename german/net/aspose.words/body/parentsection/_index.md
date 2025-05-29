---
title: Body.ParentSection
linktitle: ParentSection
articleTitle: ParentSection
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „Body ParentSection“, um einfach auf den übergeordneten Abschnitt einer Story zuzugreifen und die Effizienz Ihres Content-Managements zu verbessern.
type: docs
weight: 30
url: /de/net/aspose.words/body/parentsection/
---
## Body.ParentSection property

Ruft den übergeordneten Abschnitt dieser Story ab.

```csharp
public Section ParentSection { get; }
```

## Bemerkungen

`ParentSection` ist gleichbedeutend mit[`ParentNode`](../../node/parentnode/) gegossen zu[`Section`](../../section/).

## Beispiele

Zeigt, wie Endnoten am Ende jedes Abschnitts gespeichert und ihre Positionen geändert werden.

```csharp
public void SuppressEndnotes()
{
    Document doc = new Document();
    doc.RemoveAllChildren();

        // Standardmäßig kompiliert ein Dokument alle Endnoten an seinem Ende.
    Assert.AreEqual(EndnotePosition.EndOfDocument, doc.EndnoteOptions.Position);

    // Wir verwenden die Eigenschaft "Position" des Objekts "EndnoteOptions" des Dokuments
        // stattdessen am Ende jedes Abschnitts Endnoten zu sammeln.
    doc.EndnoteOptions.Position = EndnotePosition.EndOfSection;

    InsertSectionWithEndnote(doc, "Section 1", "Endnote 1, will stay in section 1");
    InsertSectionWithEndnote(doc, "Section 2", "Endnote 2, will be pushed down to section 3");
    InsertSectionWithEndnote(doc, "Section 3", "Endnote 3, will stay in section 3");

    // Während wir Abschnitte dazu bringen, ihre jeweiligen Endnoten anzuzeigen, können wir das Flag "SuppressEndnotes" setzen
    // des "PageSetup"-Objekts eines Abschnitts auf "true", um zum Standardverhalten zurückzukehren und seine Endnoten zu übergeben
    // weiter zum nächsten Abschnitt.
    PageSetup pageSetup = doc.Sections[1].PageSetup;
    pageSetup.SuppressEndnotes = true;

    doc.Save(ArtifactsDir + "PageSetup.SuppressEndnotes.docx");
}

/// <summary>
/// Fügen Sie einem Dokument einen Abschnitt mit Text und einer Endnote hinzu.
/// </summary>
private static void InsertSectionWithEndnote(Document doc, string sectionBodyText, string endnoteText)
{
    Section section = new Section(doc);

    doc.AppendChild(section);

    Body body = new Body(doc);
    section.AppendChild(body);

    Assert.AreEqual(section, body.ParentNode);

    Paragraph para = new Paragraph(doc);
    body.AppendChild(para);

    Assert.AreEqual(body, para.ParentNode);

    DocumentBuilder builder = new DocumentBuilder(doc);
    builder.MoveTo(para);
    builder.Write(sectionBodyText);
    builder.InsertFootnote(FootnoteType.Endnote, endnoteText);
}
```

### Siehe auch

* class [Section](../../section/)
* class [Body](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
