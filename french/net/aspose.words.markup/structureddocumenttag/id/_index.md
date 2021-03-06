---
title: Id
second_title: Référence de l'API Aspose.Words pour .NET
description: Spécifie un identifiant numérique persistant unique en lecture seule pour ce TDS.
type: docs
weight: 140
url: /fr/net/aspose.words.markup/structureddocumenttag/id/
---
## StructuredDocumentTag.Id property

Spécifie un identifiant numérique persistant unique en lecture seule pour ce **TDS**.

```csharp
public int Id { get; }
```

### Remarques

L'attribut d'identifiant doit suivre ces règles :

* Le document ne conservera les identifiants SDT que si l'intégralité du document est clonée[`Clone`](../../../aspose.words/document/clone).
* Durant[`ImportNode`](../../../aspose.words/documentbase/importnode) L'identifiant doit être conservé si l'importation ne provoque pas de conflits avec d'autres identifiants SDT dans le document cible.
* Si plusieurs nœuds SDT spécifient la même valeur décimale pour l'attribut Id, , le premier SDT du document doit conserver cet identifiant d'origine, et tous les nœuds SDT suivants doivent se voir attribuer de nouveaux identifiants lors du chargement du document.
* Pendant SDT autonomeINodeCloningListener) opération un nouvel ID unique sera généré pour le nœud SDT cloné.
* Si Id n'est pas spécifié dans le document source, le nœud SDT doit se voir attribuer un nouvel identifiant unique lors du chargement du document.

### Exemples

Montre comment créer une balise de document structurée dans une zone de texte brut et modifier son apparence.

```csharp
Document doc = new Document();

// Crée une balise de document structurée qui contiendra du texte brut.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline);

// Définissez le titre et la couleur du cadre qui apparaît lorsque vous passez la souris sur la balise de document structuré dans Microsoft Word.
tag.Title = "My plain text";
tag.Color = Color.Magenta;

// Définissez une balise pour cette balise de document structuré, qui peut être obtenue
// sous la forme d'un élément XML nommé "tag", avec la chaîne ci-dessous dans son attribut "@val".
tag.Tag = "MyPlainTextSDT";

// Chaque balise de document structuré a un ID unique aléatoire.
Assert.That(tag.Id, Is.Positive);

// Définit la police du texte à l'intérieur de la balise de document structuré.
tag.ContentsFont.Name = "Arial";

// Définit la police du texte à la fin de la balise de document structuré.
// Tout texte que nous tapons dans le corps du document après être sorti de la balise avec les touches fléchées utilisera cette police.
tag.EndCharacterFont.Name = "Arial Black";

// Par défaut, c'est faux et appuyer sur Entrée à l'intérieur d'une balise de document structuré ne fait rien.
// Lorsqu'il est défini sur true, notre balise de document structuré peut avoir plusieurs lignes.

// Définissez la propriété "Multiline" sur "false" pour n'autoriser que le contenu
// de cette balise de document structuré pour s'étendre sur une seule ligne.
// Définissez la propriété "Multiline" sur "true" pour permettre à la balise de contenir plusieurs lignes de contenu.
tag.Multiline = true;

// Définissez la propriété "Apparence" sur "SdtAppearance.Tags" pour afficher les balises autour du contenu.
 // Par défaut, la balise de document structuré s'affiche en tant que BoundingBox.
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

* class [StructuredDocumentTag](../../structureddocumenttag)
* espace de noms [Aspose.Words.Markup](../../structureddocumenttag)
* Assemblée [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
