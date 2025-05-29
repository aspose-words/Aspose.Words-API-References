---
title: StructuredDocumentTag.ContentsFont
linktitle: ContentsFont
articleTitle: ContentsFont
second_title: Aspose.Words pour .NET
description: Découvrez la propriété StructuredDocumentTag ContentsFont pour une mise en forme fluide du texte dans SDT. Améliorez vos documents grâce à des options de police personnalisables !
type: docs
weight: 80
url: /fr/net/aspose.words.markup/structureddocumenttag/contentsfont/
---
## StructuredDocumentTag.ContentsFont property

Formatage de police qui sera appliqué au texte saisi dans**SDT** .

```csharp
public Font ContentsFont { get; }
```

## Exemples

Montre comment créer une balise de document structurée dans une zone de texte brut et modifier son apparence.

```csharp
Document doc = new Document();

// Créez une balise de document structurée qui contiendra du texte brut.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline);

// Définissez le titre et la couleur du cadre qui apparaît lorsque vous passez la souris sur la balise de document structuré dans Microsoft Word.
tag.Title = "My plain text";
tag.Color = Color.Magenta;

// Définir une balise pour cette balise de document structuré, qui est accessible
// comme un élément XML nommé "tag", avec la chaîne ci-dessous dans son attribut "@val".
tag.Tag = "MyPlainTextSDT";

// Chaque balise de document structuré possède un identifiant unique aléatoire.
Assert.IsTrue(tag.Id > 0);

// Définissez la police du texte à l'intérieur de la balise de document structuré.
tag.ContentsFont.Name = "Arial";

// Définissez la police du texte à la fin de la balise de document structuré.
// Tout texte que nous tapons dans le corps du document après avoir quitté la balise avec les touches fléchées utilisera cette police.
tag.EndCharacterFont.Name = "Arial Black";

// Par défaut, c'est faux et appuyer sur Entrée à l'intérieur d'une balise de document structuré ne fait rien.
// Lorsqu'il est défini sur true, notre balise de document structuré peut avoir plusieurs lignes.

// Définissez la propriété « Multiline » sur « false » pour autoriser uniquement le contenu
// de cette balise de document structuré pour s'étendre sur une seule ligne.
// Définissez la propriété « Multiline » sur « true » pour permettre à la balise de contenir plusieurs lignes de contenu.
tag.Multiline = true;

// Définissez la propriété « Apparence » sur « SdtAppearance.Tags » pour afficher les balises autour du contenu.
 // Par défaut, la balise de document structuré s'affiche sous la forme BoundingBox.
tag.Appearance = SdtAppearance.Tags;

DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertNode(tag);

// Insérer un clone de notre balise de document structuré dans un nouveau paragraphe.
StructuredDocumentTag tagClone = (StructuredDocumentTag)tag.Clone(true);
builder.InsertParagraph();
builder.InsertNode(tagClone);

// Utilisez la méthode « RemoveSelfOnly » pour supprimer une balise de document structurée, tout en conservant son contenu dans le document.
tagClone.RemoveSelfOnly();

doc.Save(ArtifactsDir + "StructuredDocumentTag.PlainText.docx");
```

### Voir également

* class [Font](../../../aspose.words/font/)
* class [StructuredDocumentTag](../)
* espace de noms [Aspose.Words.Markup](../../../aspose.words.markup/)
* Assemblée [Aspose.Words](../../../)
