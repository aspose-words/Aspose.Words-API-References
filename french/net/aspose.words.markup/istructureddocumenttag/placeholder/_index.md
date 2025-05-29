---
title: IStructuredDocumentTag.Placeholder
linktitle: Placeholder
articleTitle: Placeholder
second_title: Aspose.Words pour .NET
description: Découvrez la propriété d'espace réservé IStructuredDocumentTag. Gérez facilement le texte d'espace réservé pour le contenu SDT vide et améliorez la convivialité de votre document.
type: docs
weight: 100
url: /fr/net/aspose.words.markup/istructureddocumenttag/placeholder/
---
## IStructuredDocumentTag.Placeholder property

Obtient le[`BuildingBlock`](../../../aspose.words.buildingblocks/buildingblock/) contenant un texte d'espace réservé qui doit être affiché lorsque le contenu de cette exécution SDT est vide, l'élément XML mappé associé est vide comme spécifié via le[`XmlMapping`](../xmlmapping/) élément ou le[`IsShowingPlaceholderText`](../isshowingplaceholdertext/) l'élément est vrai.

```csharp
public BuildingBlock Placeholder { get; }
```

## Remarques

Peut être nul, ce qui signifie que l'espace réservé n'est pas applicable pour ce Sdt.

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

* class [BuildingBlock](../../../aspose.words.buildingblocks/buildingblock/)
* interface [IStructuredDocumentTag](../)
* espace de noms [Aspose.Words.Markup](../../../aspose.words.markup/)
* Assemblée [Aspose.Words](../../../)
