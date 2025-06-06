---
title: FootnotePosition Enum
linktitle: FootnotePosition
articleTitle: FootnotePosition
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words.Notes.FootnotePosition pour un placement personnalisable des notes de bas de page, améliorant ainsi la mise en forme et la lisibilité du document.
type: docs
weight: 4980
url: /fr/net/aspose.words.notes/footnoteposition/
---
## FootnotePosition enumeration

Définit la position de la note de bas de page.

```csharp
public enum FootnotePosition
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| BottomOfPage | `1` | Les notes de bas de page sont affichées au bas de chaque page. |
| BeneathText | `2` | Les notes de bas de page sont affichées sous le texte sur chaque page. |

## Exemples

Montre comment sélectionner un emplacement différent où le document collecte et affiche ses notes de bas de page.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Une note de bas de page est un moyen d'attacher une référence ou un commentaire latéral au texte
 // qui n'interfère pas avec le flux du texte principal.
// L'insertion d'une note de bas de page ajoute un petit symbole de référence en exposant
// dans le corps du texte principal où nous insérons la note de bas de page.
// Chaque note de bas de page crée également une entrée au bas de la page, composée d'un symbole
// qui correspond au symbole de référence dans le corps du texte principal.
// Le texte de référence que nous transmettons à la méthode « InsertFootnote » du générateur de documents.
builder.Write("Hello world!");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote contents.");

// Nous pouvons utiliser la propriété « Position » pour déterminer où le document placera toutes ses notes de bas de page.
// Si nous définissons la valeur de la propriété "Position" sur "FootnotePosition.BottomOfPage",
// Chaque note de bas de page apparaîtra au bas de la page contenant sa marque de référence. Il s'agit de la valeur par défaut.
// Si nous définissons la valeur de la propriété « Position » sur « FootnotePosition.BeneathText »,
// chaque note de bas de page apparaîtra à la fin du texte de la page qui contient sa marque de référence.
doc.FootnoteOptions.Position = footnotePosition;

doc.Save(ArtifactsDir + "InlineStory.PositionFootnote.docx");
```

### Voir également

* class [FootnoteOptions](../footnoteoptions/)
* espace de noms [Aspose.Words.Notes](../../aspose.words.notes/)
* Assemblée [Aspose.Words](../../)
