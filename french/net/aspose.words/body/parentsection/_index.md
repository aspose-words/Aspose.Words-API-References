---
title: Body.ParentSection
linktitle: ParentSection
articleTitle: ParentSection
second_title: Aspose.Words pour .NET
description: Découvrez la propriété Body ParentSection pour accéder facilement à la section parent d'une histoire et améliorer l'efficacité de votre gestion de contenu.
type: docs
weight: 30
url: /fr/net/aspose.words/body/parentsection/
---
## Body.ParentSection property

Obtient la section parent de cette histoire.

```csharp
public Section ParentSection { get; }
```

## Remarques

`ParentSection` est équivalent à[`ParentNode`](../../node/parentnode/) jeté à[`Section`](../../section/).

## Exemples

Montre comment stocker les notes de fin à la fin de chaque section et modifier leurs positions.

```csharp
public void SuppressEndnotes()
{
    Document doc = new Document();
    doc.RemoveAllChildren();

     // Par défaut, un document compile toutes les notes de fin à sa fin.
    Assert.AreEqual(EndnotePosition.EndOfDocument, doc.EndnoteOptions.Position);

    // Nous utilisons la propriété « Position » de l'objet « EndnoteOptions » du document
     // pour collecter les notes de fin à la fin de chaque section à la place.
    doc.EndnoteOptions.Position = EndnotePosition.EndOfSection;

    InsertSectionWithEndnote(doc, "Section 1", "Endnote 1, will stay in section 1");
    InsertSectionWithEndnote(doc, "Section 2", "Endnote 2, will be pushed down to section 3");
    InsertSectionWithEndnote(doc, "Section 3", "Endnote 3, will stay in section 3");

    // Lors de l'affichage des notes de fin respectives dans les sections, nous pouvons définir l'indicateur « SuppressEndnotes »
    // de l'objet « PageSetup » d'une section sur « true » pour revenir au comportement par défaut et transmettre ses notes de fin
    // passons à la section suivante.
    PageSetup pageSetup = doc.Sections[1].PageSetup;
    pageSetup.SuppressEndnotes = true;

    doc.Save(ArtifactsDir + "PageSetup.SuppressEndnotes.docx");
}

/// <summary>
/// Ajouter une section avec du texte et une note de fin à un document.
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

### Voir également

* class [Section](../../section/)
* class [Body](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
