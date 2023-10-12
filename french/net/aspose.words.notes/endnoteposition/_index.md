---
title: Enum EndnotePosition
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.Notes.EndnotePosition énumération. Définit la position de la note de fin.
type: docs
weight: 4250
url: /fr/net/aspose.words.notes/endnoteposition/
---
## EndnotePosition enumeration

Définit la position de la note de fin.

```csharp
public enum EndnotePosition
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| EndOfSection | `0` | Les notes de fin sont affichées à la fin de la section. |
| EndOfDocument | `3` | Les notes de fin sont affichées à la fin du document. |

### Exemples

Montre comment sélectionner un autre emplacement où le document collecte et affiche ses notes de fin.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Une note de fin est un moyen d'attacher une référence ou un commentaire secondaire au texte
 // cela n'interfère pas avec le flux du corps principal du texte.
// L'insertion d'une note de fin ajoute un petit symbole de référence en exposant
// au corps du texte principal où nous insérons la note de fin.
// Chaque note de fin crée également une entrée à la fin du document, constituée d'un symbole
// qui correspond au symbole de référence dans le corps du texte principal.
// Le texte de référence que nous transmettons à la méthode "InsertEndnote" du générateur de documents.
builder.Write("Hello world!");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote contents.");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("This is the second section.");

// Nous pouvons utiliser la propriété "Position" pour déterminer où le document placera toutes ses notes de fin.
// Si on fixe la valeur de la propriété "Position" à "EndnotePosition.EndOfDocument",
// chaque note de bas de page apparaîtra dans une collection à la fin du document. Ceci est la valeur par défault.
// Si on fixe la valeur de la propriété "Position" à "EndnotePosition.EndOfSection",
// chaque note de bas de page apparaîtra dans une collection à la fin de la section dont le texte contient la marque de référence de la note de fin.
doc.EndnoteOptions.Position = endnotePosition;

doc.Save(ArtifactsDir + "InlineStory.PositionEndnote.docx");
```

### Voir également

* class [EndnoteOptions](../endnoteoptions/)
* espace de noms [Aspose.Words.Notes](../../aspose.words.notes/)
* Assemblée [Aspose.Words](../../)


