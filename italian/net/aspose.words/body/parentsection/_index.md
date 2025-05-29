---
title: Body.ParentSection
linktitle: ParentSection
articleTitle: ParentSection
second_title: Aspose.Words per .NET
description: Scopri la proprietà Body ParentSection per accedere facilmente alla sezione padre di un articolo e migliorare l'efficienza della gestione dei contenuti.
type: docs
weight: 30
url: /it/net/aspose.words/body/parentsection/
---
## Body.ParentSection property

Ottiene la sezione padre di questa storia.

```csharp
public Section ParentSection { get; }
```

## Osservazioni

`ParentSection` è equivalente a[`ParentNode`](../../node/parentnode/) lanciato a[`Section`](../../section/).

## Esempi

Mostra come memorizzare le note di chiusura alla fine di ogni sezione e modificarne la posizione.

```csharp
public void SuppressEndnotes()
{
    Document doc = new Document();
    doc.RemoveAllChildren();

     // Per impostazione predefinita, un documento compila tutte le note di chiusura alla fine.
    Assert.AreEqual(EndnotePosition.EndOfDocument, doc.EndnoteOptions.Position);

    // Utilizziamo la proprietà "Position" dell'oggetto "EndnoteOptions" del documento
     // per raccogliere invece le note finali alla fine di ogni sezione.
    doc.EndnoteOptions.Position = EndnotePosition.EndOfSection;

    InsertSectionWithEndnote(doc, "Section 1", "Endnote 1, will stay in section 1");
    InsertSectionWithEndnote(doc, "Section 2", "Endnote 2, will be pushed down to section 3");
    InsertSectionWithEndnote(doc, "Section 3", "Endnote 3, will stay in section 3");

    // Mentre otteniamo che le sezioni visualizzino le rispettive note di chiusura, possiamo impostare il flag "SuppressEndnotes"
    // dell'oggetto "PageSetup" di una sezione su "true" per ripristinare il comportamento predefinito e passare le sue note di chiusura
    // passiamo alla sezione successiva.
    PageSetup pageSetup = doc.Sections[1].PageSetup;
    pageSetup.SuppressEndnotes = true;

    doc.Save(ArtifactsDir + "PageSetup.SuppressEndnotes.docx");
}

/// <summary>
/// Aggiungere una sezione con testo e una nota di chiusura a un documento.
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

### Guarda anche

* class [Section](../../section/)
* class [Body](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
