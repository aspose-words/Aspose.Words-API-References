---
title: StyleCollection.DefaultFont
second_title: Référence de l'API Aspose.Words pour .NET
description: StyleCollection propriété. Obtient le formatage du texte par défaut du document.
type: docs
weight: 20
url: /fr/net/aspose.words/stylecollection/defaultfont/
---
## StyleCollection.DefaultFont property

Obtient le formatage du texte par défaut du document.

```csharp
public Font DefaultFont { get; }
```

### Remarques

Notez que les valeurs par défaut à l'échelle du document ont été introduites dans Microsoft Word 2007 et sont entièrement prises en charge dans les formats OOXML (Docx) uniquement. Les formats de documents antérieurs ont une prise en charge limitée pour cette fonctionnalité et seuls les noms de polices peuvent être stockés.

### Exemples

Montre comment ajouter un style à la collection de styles d’un document.

```csharp
Document doc = new Document();

StyleCollection styles = doc.Styles;
// Définissez les paramètres par défaut pour les nouveaux styles que nous pourrons ajouter ultérieurement à cette collection.
styles.DefaultFont.Name = "Courier New";
// Si on ajoute un style du "StyleType.Paragraph", la collection appliquera les valeurs de
// sa propriété "DefaultParagraphFormat" à la propriété "ParagraphFormat" du style.
styles.DefaultParagraphFormat.FirstLineIndent = 15.0;
// Ajoutez un style, puis vérifiez qu'il possède les paramètres par défaut.
styles.Add(StyleType.Paragraph, "MyStyle");

Assert.AreEqual("Courier New", styles[4].Font.Name);
Assert.AreEqual(15.0, styles["MyStyle"].ParagraphFormat.FirstLineIndent);
```

### Voir également

* class [Font](../../font/)
* class [StyleCollection](../)
* espace de noms [Aspose.Words](../../stylecollection/)
* Assemblée [Aspose.Words](../../../)


