---
title: EndnoteOptions.Position
linktitle: Position
articleTitle: Position
second_title: Aspose.Words pour .NET
description: Découvrez comment la propriété Position d'EndnoteOptions améliore la mise en page de votre document en spécifiant l'emplacement idéal des notes de fin. Optimisez votre rédaction dès aujourd'hui !
type: docs
weight: 20
url: /fr/net/aspose.words.notes/endnoteoptions/position/
---
## EndnoteOptions.Position property

Spécifie la position des notes de fin.

```csharp
public EndnotePosition Position { get; set; }
```

## Exemples

Montre comment sélectionner un emplacement différent où le document collecte et affiche ses notes de fin.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Une note de fin est un moyen d'attacher une référence ou un commentaire latéral au texte
 // qui n'interfère pas avec le flux du texte principal.
// L'insertion d'une note de fin ajoute un petit symbole de référence en exposant
// dans le corps du texte principal où nous insérons la note de fin.
// Chaque note de fin crée également une entrée à la fin du document, composée d'un symbole
// qui correspond au symbole de référence dans le corps du texte principal.
// Le texte de référence que nous transmettons à la méthode « InsertEndnote » du générateur de documents.
builder.Write("Hello world!");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote contents.");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("This is the second section.");

// Nous pouvons utiliser la propriété « Position » pour déterminer où le document placera toutes ses notes de fin.
// Si nous définissons la valeur de la propriété "Position" sur "EndnotePosition.EndOfDocument",
// Chaque note de bas de page apparaîtra dans une collection à la fin du document. Il s'agit de la valeur par défaut.
// Si nous définissons la valeur de la propriété « Position » sur « EndnotePosition.EndOfSection »,
// chaque note de bas de page apparaîtra dans une collection à la fin de la section dont le texte contient la marque de référence de la note de fin.
doc.EndnoteOptions.Position = endnotePosition;

doc.Save(ArtifactsDir + "InlineStory.PositionEndnote.docx");
```

### Voir également

* enum [EndnotePosition](../../endnoteposition/)
* class [EndnoteOptions](../)
* espace de noms [Aspose.Words.Notes](../../../aspose.words.notes/)
* Assemblée [Aspose.Words](../../../)
