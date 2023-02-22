---
title: Class StyleCollection
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.StyleCollection classe. Une collection dobjets Style qui représentent à la fois les styles intégrés et définis par lutilisateur dans un document.
type: docs
weight: 5840
url: /fr/net/aspose.words/stylecollection/
---
## StyleCollection class

Une collection d'objets Style qui représentent à la fois les styles intégrés et définis par l'utilisateur dans un document.

```csharp
public class StyleCollection : IEnumerable<Style>
```

## Propriétés

| Nom | La description |
| --- | --- |
| [Count](../../aspose.words/stylecollection/count/) { get; } | Obtient le nombre de styles dans la collection. |
| [DefaultFont](../../aspose.words/stylecollection/defaultfont/) { get; } | Récupère la mise en forme du texte par défaut du document. |
| [DefaultParagraphFormat](../../aspose.words/stylecollection/defaultparagraphformat/) { get; } | Obtient le formatage de paragraphe par défaut du document. |
| [Document](../../aspose.words/stylecollection/document/) { get; } | Obtient le document propriétaire. |
| [Item](../../aspose.words/stylecollection/item/) { get; } | Obtient un style par nom ou alias. (3 indexers) |

## Méthodes

| Nom | La description |
| --- | --- |
| [Add](../../aspose.words/stylecollection/add/)(StyleType, string) | Crée un nouveau style défini par l'utilisateur et l'ajoute à la collection. |
| [AddCopy](../../aspose.words/stylecollection/addcopy/)(Style) | Copie un style dans cette collection. |
| [ClearQuickStyleGallery](../../aspose.words/stylecollection/clearquickstylegallery/)() | Supprime tous les styles du panneau Galerie de styles rapides. |
| [GetEnumerator](../../aspose.words/stylecollection/getenumerator/)() | Obtient un objet énumérateur qui énumérera les styles dans l'ordre alphabétique de leurs noms. |

### Exemples

Montre comment créer et utiliser un style de paragraphe avec une mise en forme de liste.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Crée un style de paragraphe personnalisé.
Style style = doc.Styles.Add(StyleType.Paragraph, "MyStyle1");
style.Font.Size = 24;
style.Font.Name = "Verdana";
style.ParagraphFormat.SpaceAfter = 12;

// Créez une liste et assurez-vous que les paragraphes qui utilisent ce style utiliseront cette liste.
style.ListFormat.List = doc.Lists.Add(ListTemplate.BulletDefault);
style.ListFormat.ListLevelNumber = 0;

// Appliquez le style de paragraphe au paragraphe actuel du générateur de document, puis ajoutez du texte.
builder.ParagraphFormat.Style = style;
builder.Writeln("Hello World: MyStyle1, bulleted list.");

// Modifiez le style du générateur de document en un style qui n'a pas de formatage de liste et écrivez un autre paragraphe.
builder.ParagraphFormat.Style = doc.Styles["Normal"];
builder.Writeln("Hello World: Normal.");

builder.Document.Save(ArtifactsDir + "Styles.ParagraphStyleBulletedList.docx");
```

### Voir également

* class [Style](../style/)
* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)


