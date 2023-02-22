---
title: Body.ParentSection
second_title: Aspose.Words per .NET API Reference
description: Body proprietà. Ottiene la sezione padre di questa storia.
type: docs
weight: 30
url: /it/net/aspose.words/body/parentsection/
---
## Body.ParentSection property

Ottiene la sezione padre di questa storia.

```csharp
public Section ParentSection { get; }
```

### Osservazioni

**Sezione Genitori** è equivalente a`(Sezione) ParentNode`.

### Esempi

Mostra come memorizzare le note di chiusura alla fine di ogni sezione e modificarne le posizioni.

```csharp
{
    Document doc = new Document();
    doc.RemoveAllChildren();

     // Per impostazione predefinita, un documento compila tutte le note di chiusura alla fine.
    Assert.AreEqual(EndnotePosition.EndOfDocument, doc.EndnoteOptions.Position);

    // Utilizziamo la proprietà "Position" dell'oggetto "EndnoteOptions" del documento
     // per raccogliere invece le note di chiusura alla fine di ogni sezione.
    doc.EndnoteOptions.Position = EndnotePosition.EndOfSection;

    InsertSectionWithEndnote(doc, "Section 1", "Endnote 1, will stay in section 1");
    InsertSectionWithEndnote(doc, "Section 2", "Endnote 2, will be pushed down to section 3");
    InsertSectionWithEndnote(doc, "Section 3", "Endnote 3, will stay in section 3");

    // Mentre riceviamo sezioni per visualizzare le rispettive note di chiusura, possiamo impostare il flag "SuppressEndnotes".
    // dell'oggetto "PageSetup" di una sezione su "true" per ripristinare il comportamento predefinito e passare le note di chiusura
    // alla prossima sezione.
    PageSetup pageSetup = doc.Sections[1].PageSetup;
    pageSetup.SuppressEndnotes = true;

    doc.Save(ArtifactsDir + "PageSetup.SuppressEndnotes.docx");

/// <summary>
/// Aggiunge una sezione con testo e una nota di chiusura a un documento.
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
* spazio dei nomi [Aspose.Words](../../body/)
* assemblea [Aspose.Words](../../../)


