---
title: IStructuredDocumentTag.IsShowingPlaceholderText
linktitle: IsShowingPlaceholderText
articleTitle: IsShowingPlaceholderText
second_title: Aspose.Words pour .NET
description: Découvrez la propriété IStructuredDocumentTag IsShowingPlaceholderText pour identifier facilement le texte d'espace réservé dans votre SDT, améliorant ainsi la clarté et la gestion du contenu.
type: docs
weight: 50
url: /fr/net/aspose.words.markup/istructureddocumenttag/isshowingplaceholdertext/
---
## IStructuredDocumentTag.IsShowingPlaceholderText property

Spécifie si le contenu de ce**SDT** doit être interprété comme contenant du texte d'espace réservé text (par opposition au contenu de texte normal dans le SDT).

si défini sur vrai, cet état sera repris (affichant le texte d'espace réservé) à l'ouverture de ce document.

```csharp
public bool IsShowingPlaceholderText { get; set; }
```

## Exemples

Montre comment utiliser le contenu d'un bloc de construction comme texte d'espace réservé personnalisé pour une balise de document structurée.

```csharp
Document doc = new Document();

// Insérer une balise de document structurée en texte brut de type « PlainText », qui fonctionnera comme une zone de texte.
// Le contenu qu'il affichera par défaut est une invite « Cliquez ici pour saisir du texte ».
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline);

// Nous pouvons faire en sorte que la balise affiche le contenu d'un bloc de construction au lieu du texte par défaut.
// Tout d’abord, ajoutez un bloc de construction avec du contenu au document de glossaire.
GlossaryDocument glossaryDoc = doc.GlossaryDocument;

BuildingBlock substituteBlock = new BuildingBlock(glossaryDoc);
substituteBlock.Name = "Custom Placeholder";
substituteBlock.AppendChild(new Section(glossaryDoc));
substituteBlock.FirstSection.AppendChild(new Body(glossaryDoc));
substituteBlock.FirstSection.Body.AppendParagraph("Custom placeholder text.");

glossaryDoc.AppendChild(substituteBlock);

// Ensuite, utilisez la propriété « PlaceholderName » de la balise de document structuré pour référencer ce bloc de construction par son nom.
tag.PlaceholderName = "Custom Placeholder";

// Si « PlaceholderName » fait référence à un bloc existant dans le document de glossaire du document parent,
// nous pourrons vérifier le bloc de construction via la propriété "Placeholder".
Assert.AreEqual(substituteBlock, tag.Placeholder);

// Définissez la propriété « IsShowingPlaceholderText » sur « true » pour traiter le
// contenu actuel de la balise de document structuré sous forme de texte d'espace réservé.
// Cela signifie que cliquer sur la zone de texte dans Microsoft Word mettra immédiatement en surbrillance tout le contenu de la balise.
// Définissez la propriété « IsShowingPlaceholderText » sur « false » pour obtenir le
// balise de document structurée pour traiter son contenu comme du texte qu'un utilisateur a déjà saisi.
// Cliquer sur ce texte dans Microsoft Word placera le curseur clignotant à l'emplacement cliqué.
tag.IsShowingPlaceholderText = isShowingPlaceholderText;

DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertNode(tag);

doc.Save(ArtifactsDir + "StructuredDocumentTag.PlaceholderBuildingBlock.docx");
```

### Voir également

* interface [IStructuredDocumentTag](../)
* espace de noms [Aspose.Words.Markup](../../../aspose.words.markup/)
* Assemblée [Aspose.Words](../../../)
