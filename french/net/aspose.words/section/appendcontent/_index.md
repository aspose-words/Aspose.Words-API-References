---
title: Section.AppendContent
linktitle: AppendContent
articleTitle: AppendContent
second_title: Aspose.Words pour .NET
description: Section AppendContent méthode. Insère une copie du contenu de la section source à la fin de cette section en C#.
type: docs
weight: 80
url: /fr/net/aspose.words/section/appendcontent/
---
## Section.AppendContent method

Insère une copie du contenu de la section source à la fin de cette section.

```csharp
public void AppendContent(Section sourceSection)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| sourceSection | Section | Section à partir de laquelle copier le contenu. |

## Remarques

Seul le contenu de[`Body`](../body/) de la section source est copiée, la mise en page, les en-têtes et pieds de page ne sont pas copiés.

Les nœuds sont automatiquement importés si la section source appartient à un autre document.

Aucune nouvelle section n'est créée dans le document de destination.

## Exemples

Montre comment ajouter le contenu d’une section à une autre section.

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

// Insère le contenu de la première section au début de la troisième section.
Section sectionToPrepend = doc.Sections[0];
section.PrependContent(sectionToPrepend);

// Insère le contenu de la deuxième section à la fin de la troisième section.
Section sectionToAppend = doc.Sections[1];
section.AppendContent(sectionToAppend);

// Les méthodes "PrependContent" et "AppendContent" n'ont créé aucune nouvelle section.
Assert.AreEqual(3, doc.Sections.Count);
Assert.AreEqual("Section 1" + ControlChar.ParagraphBreak +
                "Section 3" + ControlChar.ParagraphBreak +
                "Section 2" + ControlChar.SectionBreak, section.GetText());
```

### Voir également

* class [Section](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
