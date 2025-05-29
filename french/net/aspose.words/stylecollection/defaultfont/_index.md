---
title: StyleCollection.DefaultFont
linktitle: DefaultFont
articleTitle: DefaultFont
second_title: Aspose.Words pour .NET
description: Découvrez la propriété StyleCollection DefaultFont pour une mise en forme fluide du texte de vos documents. Améliorez vos documents avec un style cohérent et professionnel.
type: docs
weight: 20
url: /fr/net/aspose.words/stylecollection/defaultfont/
---
## StyleCollection.DefaultFont property

Obtient la mise en forme du texte par défaut du document.

```csharp
public Font DefaultFont { get; }
```

## Remarques

Notez que les valeurs par défaut à l'échelle du document ont été introduites dans Microsoft Word 2007 et sont entièrement prises en charge dans les formats OOXML (Docx) uniquement. Les formats de document antérieurs ont une prise en charge limitée de cette fonctionnalité et seuls les noms de polices peuvent être stockés.

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

* class [Font](../../font/)
* class [StyleCollection](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
