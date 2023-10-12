---
title: StructuredDocumentTag.Clear
second_title: Référence de l'API Aspose.Words pour .NET
description: StructuredDocumentTag méthode. Efface le contenu de cette balise de document structuré et affiche un espace réservé sil est défini.
type: docs
weight: 360
url: /fr/net/aspose.words.markup/structureddocumenttag/clear/
---
## StructuredDocumentTag.Clear method

Efface le contenu de cette balise de document structuré et affiche un espace réservé s'il est défini.

```csharp
public void Clear()
```

### Remarques

Il n'est pas possible d'effacer le contenu d'une balise de document structuré si elle comporte des révisions.

Si cette balise de document structuré est mappée sur du XML personnalisé (en utilisant le[`XmlMapping`](../xmlmapping/) ), le nœud XML référencé est effacé.

### Exemples

Montre comment supprimer le contenu des éléments de balise de document structuré.

```csharp
Document doc = new Document();

// Créez une balise de document structuré en texte brut, puis ajoutez-la au document.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Block);
doc.FirstSection.Body.AppendChild(tag);

// Cette balise de document structuré, qui se présente sous la forme d'une zone de texte, affiche déjà du texte d'espace réservé.
Assert.AreEqual("Click here to enter text.", tag.GetText().Trim());
Assert.True(tag.IsShowingPlaceholderText);

// Crée un bloc de construction avec du contenu textuel.
GlossaryDocument glossaryDoc = doc.GlossaryDocument;
BuildingBlock substituteBlock = new BuildingBlock(glossaryDoc);
substituteBlock.Name = "My placeholder";
substituteBlock.AppendChild(new Section(glossaryDoc));
substituteBlock.FirstSection.EnsureMinimum();
substituteBlock.FirstSection.Body.FirstParagraph.AppendChild(new Run(glossaryDoc, "Custom placeholder text."));
glossaryDoc.AppendChild(substituteBlock);

// Définissez la propriété "PlaceholderName" de la balise du document structuré sur le nom de notre bloc de construction pour obtenir
// la balise du document structuré pour afficher le contenu du bloc de construction à la place du texte original par défaut.
tag.PlaceholderName = "My placeholder";

Assert.AreEqual("Custom placeholder text.", tag.GetText().Trim());
Assert.True(tag.IsShowingPlaceholderText);

// Modifie le texte de la balise du document structuré et masque le texte de l'espace réservé.
Run run = (Run)tag.GetChild(NodeType.Run, 0, true);
run.Text = "New text.";
tag.IsShowingPlaceholderText = false;

Assert.AreEqual("New text.", tag.GetText().Trim());

// Utilisez la méthode "Clear" pour effacer le contenu de cette balise de document structuré et afficher à nouveau l'espace réservé.
tag.Clear();

Assert.True(tag.IsShowingPlaceholderText);
Assert.AreEqual("Custom placeholder text.", tag.GetText().Trim());
```

### Voir également

* class [StructuredDocumentTag](../)
* espace de noms [Aspose.Words.Markup](../../structureddocumenttag/)
* Assemblée [Aspose.Words](../../../)


