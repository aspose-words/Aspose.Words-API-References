---
title: PageSetup.SuppressEndnotes
linktitle: SuppressEndnotes
articleTitle: SuppressEndnotes
second_title: Aspose.Words per .NET
description: Scopri come la proprietà PageSetup SuppressEndnotes migliora il layout del tuo documento controllando il posizionamento delle note di chiusura per sezioni più chiare e organizzate.
type: docs
weight: 410
url: /it/net/aspose.words/pagesetup/suppressendnotes/
---
## PageSetup.SuppressEndnotes property

Vero se le note di chiusura vengono stampate alla fine della sezione successiva che non le sopprime. Le note di chiusura soppresse vengono stampate prima delle note di chiusura in quella sezione.

```csharp
public bool SuppressEndnotes { get; set; }
```

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

* class [PageSetup](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
