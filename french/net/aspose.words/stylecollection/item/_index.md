---
title: StyleCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words pour .NET
description: Découvrez la puissante propriété Item de StyleCollection pour récupérer sans effort des styles par nom ou alias, améliorant ainsi votre expérience de conception en toute simplicité !
type: docs
weight: 50
url: /fr/net/aspose.words/stylecollection/item/
---
## StyleCollection indexer (1 of 3)

Obtient un style par nom ou alias.

```csharp
public Style this[string name] { get; }
```

## Remarques

Sensible à la casse, renvoie`nul` si le style avec le nom donné n'est pas trouvé.

S'il s'agit d'un nom anglais d'un style intégré qui n'existe pas encore, il est automatiquement créé.

## Exemples

Indique quand recalculer la mise en page du document.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// L'enregistrement d'un document au format PDF, dans une image ou l'impression pour la première fois sera automatiquement
// mettre en cache la mise en page du document dans ses pages.
doc.Save(ArtifactsDir + "Document.UpdatePageLayout.1.pdf");

// Modifier le document d'une manière ou d'une autre.
doc.Styles["Normal"].Font.Size = 6;
doc.Sections[0].PageSetup.Orientation = Aspose.Words.Orientation.Landscape;
doc.Sections[0].PageSetup.Margins = Margins.Mirrored;

// Dans la version actuelle d'Aspose.Words, la modification du document ne le reconstruit pas automatiquement
// la mise en page en cache. Si nous souhaitons la mise en page en cache
// pour rester à jour, nous devrons le mettre à jour manuellement.
doc.UpdatePageLayout();

doc.Save(ArtifactsDir + "Document.UpdatePageLayout.2.pdf");
```

### Voir également

* class [Style](../../style/)
* class [StyleCollection](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)

---

## StyleCollection indexer (2 of 3)

Obtient un style intégré par son identifiant indépendant des paramètres régionaux.

```csharp
public Style this[StyleIdentifier sti] { get; }
```

| Paramètre | La description |
| --- | --- |
| sti | UN[`StyleIdentifier`](../../styleidentifier/) valeur qui spécifie le style intégré à récupérer. |

## Remarques

Lors de l'accès à un style qui n'existe pas encore, il est automatiquement créé.

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

* class [Style](../../style/)
* enum [StyleIdentifier](../../styleidentifier/)
* class [StyleCollection](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)

---

## StyleCollection indexer (3 of 3)

Obtient un style par index.

```csharp
public Style this[int index] { get; }
```

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

* class [Style](../../style/)
* class [StyleCollection](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
