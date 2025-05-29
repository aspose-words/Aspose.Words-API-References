---
title: Orientation Enum
linktitle: Orientation
articleTitle: Orientation
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words.Orientation pour un contrôle transparent de l'orientation des pages. Améliorez la mise en forme de vos documents avec facilité et précision !
type: docs
weight: 5050
url: /fr/net/aspose.words/orientation/
---
## Orientation enumeration

Spécifie l'orientation de la page.

```csharp
public enum Orientation
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| Portrait | `1` | Orientation de la page portrait (étroite et haute). |
| Landscape | `2` | Orientation de la page paysage (large et courte). |

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

* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)
