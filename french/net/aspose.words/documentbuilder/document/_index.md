---
title: DocumentBuilder.Document
linktitle: Document
articleTitle: Document
second_title: Aspose.Words pour .NET
description: Gérez facilement les propriétés de vos documents avec DocumentBuilder. Obtenez ou configurez facilement votre objet Document pour une gestion documentaire simplifiée.
type: docs
weight: 90
url: /fr/net/aspose.words/documentbuilder/document/
---
## DocumentBuilder.Document property

Obtient ou définit le`Document` objet auquel cet objet est attaché.

```csharp
public Document Document { get; set; }
```

## Exemples

Montre comment appliquer et rétablir les paramètres de mise en page aux sections d'un document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Modifiez les propriétés de configuration de la page pour la section actuelle du générateur et ajoutez du texte.
builder.PageSetup.Orientation = Orientation.Landscape;
builder.PageSetup.VerticalAlignment = PageVerticalAlignment.Center;
builder.Writeln("This is the first section, which landscape oriented with vertically centered text.");

// Si nous commençons une nouvelle section en utilisant un générateur de documents,
// il héritera des propriétés de configuration de page actuelles du constructeur.
builder.InsertBreak(BreakType.SectionBreakNewPage);

Assert.AreEqual(Orientation.Landscape, doc.Sections[1].PageSetup.Orientation);
Assert.AreEqual(PageVerticalAlignment.Center, doc.Sections[1].PageSetup.VerticalAlignment);

// Nous pouvons rétablir ses propriétés de configuration de page à leurs valeurs par défaut en utilisant la méthode « ClearFormatting ».
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
