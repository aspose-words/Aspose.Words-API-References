---
title: StructuredDocumentTag.Appearance
second_title: Référence de l'API Aspose.Words pour .NET
description: StructuredDocumentTag propriété. Obtient/définit lapparence dune balise de document structuré.
type: docs
weight: 20
url: /fr/net/aspose.words.markup/structureddocumenttag/appearance/
---
## StructuredDocumentTag.Appearance property

Obtient/définit l'apparence d'une balise de document structuré.

```csharp
public SdtAppearance Appearance { get; set; }
```

### Exemples

Montre comment créer une balise de document structuré dans une zone de texte brut et modifier son apparence.

```csharp
Document doc = new Document();

// Créez une balise de document structuré qui contiendra du texte brut.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline);

// Définissez le titre et la couleur du cadre qui apparaît lorsque vous passez la souris sur la balise du document structuré dans Microsoft Word.
tag.Title = "My plain text";
tag.Color = Color.Magenta;

// Définit une balise pour cette balise de document structuré, qui peut être obtenue
// en tant qu'élément XML nommé "tag", avec la chaîne ci-dessous dans son attribut "@val".
tag.Tag = "MyPlainTextSDT";

// Chaque balise de document structuré a un identifiant unique aléatoire.
Assert.That(tag.Id, Is.Positive);

// Définit la police du texte à l'intérieur de la balise du document structuré.
tag.ContentsFont.Name = "Arial";

// Définit la police du texte à la fin de la balise du document structuré.
// Tout texte que nous tapons dans le corps du document après avoir quitté la balise avec les touches fléchées utilisera cette police.
tag.EndCharacterFont.Name = "Arial Black";

// Par défaut, c'est faux et appuyer sur Entrée à l'intérieur d'une balise de document structuré ne fait rien.
// Lorsqu'elle est définie sur true, notre balise de document structuré peut avoir plusieurs lignes.

// Définit la propriété "Multiline" sur "false" pour autoriser uniquement le contenu
// de cette balise de document structuré pour s'étendre sur une seule ligne.
// Définissez la propriété "Multiline" sur "true" pour permettre à la balise de contenir plusieurs lignes de contenu.
tag.Multiline = true;

// Définissez la propriété "Appearance" sur "SdtAppearance.Tags" pour afficher les balises autour du contenu.
 // Par défaut, la balise du document structuré s'affiche sous la forme BoundingBox.
tag.Appearance = SdtAppearance.Tags;

DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertNode(tag);

// Insère un clone de notre balise de document structuré dans un nouveau paragraphe.
StructuredDocumentTag tagClone = (StructuredDocumentTag)tag.Clone(true);
builder.InsertParagraph();
builder.InsertNode(tagClone);

// Utilisez la méthode "RemoveSelfOnly" pour supprimer une balise de document structuré, tout en conservant son contenu dans le document.
tagClone.RemoveSelfOnly();

doc.Save(ArtifactsDir + "StructuredDocumentTag.PlainText.docx");
```

### Voir également

* enum [SdtAppearance](../../sdtappearance/)
* class [StructuredDocumentTag](../)
* espace de noms [Aspose.Words.Markup](../../structureddocumenttag/)
* Assemblée [Aspose.Words](../../../)


