---
title: StyleCollection Class
linktitle: StyleCollection
articleTitle: StyleCollection
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.StyleCollection, dotée d'une riche gamme d'objets de style intégrés et personnalisés pour améliorer la mise en forme et la conception de votre document.
type: docs
weight: 6990
url: /fr/net/aspose.words/stylecollection/
---
## StyleCollection class

Une collection de[`Style`](../style/)objets qui représentent à la fois les styles intégrés et définis par l'utilisateur dans un document.

Pour en savoir plus, visitez le[Travailler avec des styles et des thèmes](https://docs.aspose.com/words/net/working-with-styles-and-themes/) article de documentation.

```csharp
public class StyleCollection : IEnumerable<Style>
```

## Propriétés

| Nom | La description |
| --- | --- |
| [Count](../../aspose.words/stylecollection/count/) { get; } | Obtient le nombre de styles dans la collection. |
| [DefaultFont](../../aspose.words/stylecollection/defaultfont/) { get; } | Obtient la mise en forme du texte par défaut du document. |
| [DefaultParagraphFormat](../../aspose.words/stylecollection/defaultparagraphformat/) { get; } | Obtient la mise en forme de paragraphe par défaut du document. |
| [Document](../../aspose.words/stylecollection/document/) { get; } | Obtient le document propriétaire. |
| [Item](../../aspose.words/stylecollection/item/) { get; } | Obtient un style par nom ou alias. (3 indexers) |

## Méthodes

| Nom | La description |
| --- | --- |
| [Add](../../aspose.words/stylecollection/add/)(*[StyleType](../styletype/), string*) | Crée un nouveau style défini par l'utilisateur et l'ajoute à la collection. |
| [AddCopy](../../aspose.words/stylecollection/addcopy/)(*[Style](../style/)*) | Copie un style dans cette collection. |
| [ClearQuickStyleGallery](../../aspose.words/stylecollection/clearquickstylegallery/)() | Supprime tous les styles du panneau Galerie de styles rapides. |
| [GetEnumerator](../../aspose.words/stylecollection/getenumerator/)() | Obtient un objet énumérateur qui énumérera les styles dans l'ordre alphabétique de leurs noms. |

## Exemples

Montre comment créer et utiliser un style de paragraphe avec formatage de liste.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Créez un style de paragraphe personnalisé.
Style style = doc.Styles.Add(StyleType.Paragraph, "MyStyle1");
style.Font.Size = 24;
style.Font.Name = "Verdana";
style.ParagraphFormat.SpaceAfter = 12;

// Créez une liste et assurez-vous que les paragraphes qui utilisent ce style utiliseront cette liste.
style.ListFormat.List = doc.Lists.Add(ListTemplate.BulletDefault);
style.ListFormat.ListLevelNumber = 0;

// Appliquez le style de paragraphe au paragraphe actuel du générateur de documents, puis ajoutez du texte.
builder.ParagraphFormat.Style = style;
builder.Writeln("Hello World: MyStyle1, bulleted list.");

// Modifiez le style du générateur de documents en un style sans formatage de liste et écrivez un autre paragraphe.
builder.ParagraphFormat.Style = doc.Styles["Normal"];
builder.Writeln("Hello World: Normal.");

builder.Document.Save(ArtifactsDir + "Styles.ParagraphStyleBulletedList.docx");
```

### Voir également

* class [Style](../style/)
* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)
