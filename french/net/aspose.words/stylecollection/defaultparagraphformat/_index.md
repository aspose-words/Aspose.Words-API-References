---
title: StyleCollection.DefaultParagraphFormat
linktitle: DefaultParagraphFormat
articleTitle: DefaultParagraphFormat
second_title: Aspose.Words pour .NET
description: Découvrez la propriété StyleCollection DefaultParagraphFormat pour accéder et personnaliser facilement la mise en forme de paragraphe par défaut de votre document pour une meilleure lisibilité.
type: docs
weight: 30
url: /fr/net/aspose.words/stylecollection/defaultparagraphformat/
---
## StyleCollection.DefaultParagraphFormat property

Obtient la mise en forme de paragraphe par défaut du document.

```csharp
public ParagraphFormat DefaultParagraphFormat { get; }
```

## Remarques

Notez que les valeurs par défaut à l'échelle du document ont été introduites dans Microsoft Word 2007 et sont entièrement prises en charge dans les formats OOXML (Docx) uniquement. Les formats de document antérieurs ne prennent pas en charge le formatage de paragraphe par défaut du document.

## Exemples

Montre comment ajouter un style à la collection de styles d'un document.

```csharp
Document doc = new Document();

StyleCollection styles = doc.Styles;
// Définissez les paramètres par défaut pour les nouveaux styles que nous pourrons ajouter ultérieurement à cette collection.
styles.DefaultFont.Name = "Courier New";
// Si nous ajoutons un style de type "StyleType.Paragraph", la collection appliquera les valeurs de
// sa propriété « DefaultParagraphFormat » à la propriété « ParagraphFormat » du style.
styles.DefaultParagraphFormat.FirstLineIndent = 15.0;
// Ajoutez un style, puis vérifiez qu'il possède les paramètres par défaut.
styles.Add(StyleType.Paragraph, "MyStyle");

Assert.AreEqual("Courier New", styles[4].Font.Name);
Assert.AreEqual(15.0, styles["MyStyle"].ParagraphFormat.FirstLineIndent);
```

### Voir également

* class [ParagraphFormat](../../paragraphformat/)
* class [StyleCollection](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
