---
title: Enum PageVerticalAlignment
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.PageVerticalAlignment énumération. Spécifie la justification verticale du texte sur chaque page.
type: docs
weight: 4130
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
| Bottom | `3` | Le texte est aligné en bas de la page. |
| Center | `1` | Le texte est aligné au milieu de la page. |
| Justify | `2` | Le texte est étalé pour remplir la page. |
| Top | `0` | Le texte est aligné en haut de la page. |

### Exemples

Montre comment appliquer et rétablir les paramètres de mise en page aux sections d'un document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Modifie les propriétés de mise en page pour la section actuelle du générateur et ajoute du texte.
builder.PageSetup.Orientation = Orientation.Landscape;
builder.PageSetup.VerticalAlignment = PageVerticalAlignment.Center;
builder.Writeln("This is the first section, which landscape oriented with vertically centered text.");

// Si nous commençons une nouvelle section en utilisant un générateur de document,
// il héritera des propriétés de configuration de page actuelles du générateur.
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

* class [PageSetup](../pagesetup/)
* property [VerticalAlignment](../pagesetup/verticalalignment/)
* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)


