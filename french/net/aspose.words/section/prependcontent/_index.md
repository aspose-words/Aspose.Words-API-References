---
title: Section.PrependContent
linktitle: PrependContent
articleTitle: PrependContent
second_title: Aspose.Words pour .NET
description: Améliorez votre contenu avec la méthode Section PrependContent, en insérant sans effort le texte de la section source au début pour une meilleure organisation et clarté.
type: docs
weight: 160
url: /fr/net/aspose.words/section/prependcontent/
---
## Section.PrependContent method

Insère une copie du contenu de la section source au début de cette section.

```csharp
public void PrependContent(Section sourceSection)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| sourceSection | Section | La section à partir de laquelle copier le contenu. |

## Remarques

Seul le contenu de[`Body`](../body/) de la section source est copiée, la mise en page, les en-têtes et pieds de page ne sont pas copiés.

Les nœuds sont automatiquement importés si la section source appartient à un document différent.

Aucune nouvelle section n'est créée dans le document de destination.

## Exemples

Montre comment ajouter le contenu d'une section à une autre section.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Section 1");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("Section 2");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("Section 3");

Section section = doc.Sections[2];

Assert.AreEqual("Section 3" + ControlChar.SectionBreak, section.GetText());

// Insérer le contenu de la première section au début de la troisième section.
Section sectionToPrepend = doc.Sections[0];
section.PrependContent(sectionToPrepend);

// Insérer le contenu de la deuxième section à la fin de la troisième section.
Section sectionToAppend = doc.Sections[1];
section.AppendContent(sectionToAppend);

// Les méthodes « PrependContent » et « AppendContent » n'ont créé aucune nouvelle section.
Assert.AreEqual(3, doc.Sections.Count);
Assert.AreEqual("Section 1" + ControlChar.ParagraphBreak +
                "Section 3" + ControlChar.ParagraphBreak +
                "Section 2" + ControlChar.SectionBreak, section.GetText());
```

### Voir également

* class [Section](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
