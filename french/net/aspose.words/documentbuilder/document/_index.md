---
title: DocumentBuilder.Document
linktitle: Document
articleTitle: Document
second_title: Aspose.Words pour .NET
description: DocumentBuilder Document propriété. Obtient ou définit leDocumentobjet auquel cet objet est attaché en C#.
type: docs
weight: 90
url: /fr/net/aspose.words/documentbuilder/document/
---
## DocumentBuilder.Document property

Obtient ou définit le`Document`objet auquel cet objet est attaché.

```csharp
public Document Document { get; set; }
```

## Exemples

Montre comment appliquer et rétablir les paramètres de mise en page aux sections d’un document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Modifie les propriétés de mise en page de la section actuelle du générateur et ajoute du texte.
builder.PageSetup.Orientation = Orientation.Landscape;
builder.PageSetup.VerticalAlignment = PageVerticalAlignment.Center;
builder.Writeln("This is the first section, which landscape oriented with vertically centered text.");

// Si on démarre une nouvelle section en utilisant un générateur de documents,
// il héritera des propriétés de mise en page actuelles du constructeur.
builder.InsertBreak(BreakType.SectionBreakNewPage);

Assert.AreEqual(Orientation.Landscape, doc.Sections[1].PageSetup.Orientation);
Assert.AreEqual(PageVerticalAlignment.Center, doc.Sections[1].PageSetup.VerticalAlignment);

// Nous pouvons rétablir ses propriétés de mise en page à leurs valeurs par défaut en utilisant la méthode "ClearFormatting".
builder.PageSetup.ClearFormatting();

Assert.AreEqual(Orientation.Portrait, doc.Sections[1].PageSetup.Orientation);
Assert.AreEqual(PageVerticalAlignment.Top, doc.Sections[1].PageSetup.VerticalAlignment);

builder.Writeln("This is the second section, which is in default Letter paper size, portrait orientation and top alignment.");

doc.Save(ArtifactsDir + "PageSetup.ClearFormatting.docx");
```

### Voir également

* class [Document](../../document/)
* class [DocumentBuilder](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
