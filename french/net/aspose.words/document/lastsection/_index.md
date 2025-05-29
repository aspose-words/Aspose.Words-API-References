---
title: Document.LastSection
linktitle: LastSection
articleTitle: LastSection
second_title: Aspose.Words pour .NET
description: Découvrez la propriété LastSection pour accéder facilement à la section finale de votre document, améliorant ainsi l'efficacité de la navigation et de la gestion du contenu.
type: docs
weight: 250
url: /fr/net/aspose.words/document/lastsection/
---
## Document.LastSection property

Obtient la dernière section du document.

```csharp
public Section LastSection { get; }
```

## Remarques

Retours`nul`s'il n'y a pas de sections.

## Exemples

Montre comment créer une nouvelle section avec un générateur de documents.

```csharp
Document doc = new Document();

// Un document vierge contient une section par défaut,
// qui contient des nœuds enfants que nous pouvons éditer.
Assert.AreEqual(1, doc.Sections.Count);

// Utilisez un générateur de documents pour ajouter du texte à la première section.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Créez une deuxième section en insérant un saut de section.
builder.InsertBreak(BreakType.SectionBreakNewPage);

Assert.AreEqual(2, doc.Sections.Count);

// Chaque section a ses propres paramètres de configuration de page.
// Nous pouvons diviser le texte de la deuxième section en deux colonnes.
// Cela n'affectera pas le texte de la première section.
doc.LastSection.PageSetup.TextColumns.SetCount(2);
builder.Writeln("Column 1.");
builder.InsertBreak(BreakType.ColumnBreak);
builder.Writeln("Column 2.");

Assert.AreEqual(1, doc.FirstSection.PageSetup.TextColumns.Count);
Assert.AreEqual(2, doc.LastSection.PageSetup.TextColumns.Count);

doc.Save(ArtifactsDir + "Section.Create.docx");
```

### Voir également

* class [Section](../../section/)
* class [Document](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
