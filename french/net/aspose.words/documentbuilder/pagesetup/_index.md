---
title: DocumentBuilder.PageSetup
linktitle: PageSetup
articleTitle: PageSetup
second_title: Aspose.Words pour .NET
description: Explorez la propriété PageSetup de DocumentBuilder pour accéder aux paramètres de page et de section actuels, améliorant ainsi l'efficacité du formatage et de la mise en page de votre document.
type: docs
weight: 160
url: /fr/net/aspose.words/documentbuilder/pagesetup/
---
## DocumentBuilder.PageSetup property

Renvoie un objet qui représente la configuration de la page actuelle et les propriétés de la section.

```csharp
public PageSetup PageSetup { get; }
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

* class [PageSetup](../../pagesetup/)
* class [DocumentBuilder](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
