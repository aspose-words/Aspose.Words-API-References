---
title: PageVerticalAlignment Enum
linktitle: PageVerticalAlignment
articleTitle: PageVerticalAlignment
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words.PageVerticalAlignment pour un alignement optimal du texte sur les pages. Améliorez la mise en page de votre document grâce à une justification verticale précise !
type: docs
weight: 5100
url: /fr/net/aspose.words/pageverticalalignment/
---
## PageVerticalAlignment enumeration

Spécifie la justification verticale du texte sur chaque page.

```csharp
public enum PageVerticalAlignment
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| Bottom | `3` | Le texte est aligné au bas de la page. |
| Center | `1` | Le texte est aligné au milieu de la page. |
| Justify | `2` | Le texte est étalé pour remplir la page. |
| Top | `0` | Le texte est aligné en haut de la page. |

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

* class [PageSetup](../pagesetup/)
* property [VerticalAlignment](../pagesetup/verticalalignment/)
* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)
