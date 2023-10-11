---
title: Document.LastSection
second_title: Référence de l'API Aspose.Words pour .NET
description: Document propriété. Obtient la dernière section du document.
type: docs
weight: 240
url: /fr/net/aspose.words/document/lastsection/
---
## Document.LastSection property

Obtient la dernière section du document.

```csharp
public Section LastSection { get; }
```

### Remarques

Retours`nul` s'il n'y a pas de sections.

### Exemples

Montre comment créer une nouvelle section avec un générateur de documents.

```csharp
Document doc = new Document();

// Un document vierge contient une section par défaut,
// qui contient des nœuds enfants que nous pouvons modifier.
Assert.AreEqual(1, doc.Sections.Count);

// Utilisez un générateur de documents pour ajouter du texte à la première section.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Créez une deuxième section en insérant un saut de section.
builder.InsertBreak(BreakType.SectionBreakNewPage);

Assert.AreEqual(2, doc.Sections.Count);

// Chaque section a ses propres paramètres de mise en page.
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
* espace de noms [Aspose.Words](../../document/)
* Assemblée [Aspose.Words](../../../)


