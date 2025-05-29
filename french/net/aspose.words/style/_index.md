---
title: Style Class
linktitle: Style
articleTitle: Style
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.Style pour gérer facilement les styles personnalisés et intégrés. Améliorez la mise en forme de vos documents avec facilité et précision.
type: docs
weight: 6980
url: /fr/net/aspose.words/style/
---
## Style class

Représente un seul style intégré ou défini par l'utilisateur.

Pour en savoir plus, visitez le[Travailler avec des styles et des thèmes](https://docs.aspose.com/words/net/working-with-styles-and-themes/) article de documentation.

```csharp
public class Style
```

## Propriétés

| Nom | La description |
| --- | --- |
| [Aliases](../../aspose.words/style/aliases/) { get; } | Récupère tous les alias de ce style. Si le style n'a pas d'alias, un tableau vide de chaînes est renvoyé. |
| [AutomaticallyUpdate](../../aspose.words/style/automaticallyupdate/) { get; set; } | Spécifie si ce style est automatiquement redéfini en fonction de la valeur appropriée. |
| [BaseStyleName](../../aspose.words/style/basestylename/) { get; set; } | Obtient/définit le nom du style sur lequel ce style est basé. |
| [BuiltIn](../../aspose.words/style/builtin/) { get; } | Vrai si ce style est l'un des styles intégrés dans MS Word. |
| [Document](../../aspose.words/style/document/) { get; } | Obtient le document propriétaire. |
| [Font](../../aspose.words/style/font/) { get; } | Obtient la mise en forme des caractères du style. |
| [IsHeading](../../aspose.words/style/isheading/) { get; } | Vrai lorsque le style est l'un des styles de titre intégrés. |
| [IsQuickStyle](../../aspose.words/style/isquickstyle/) { get; set; } | Spécifie si ce style est affiché dans la galerie de styles rapides dans l'interface utilisateur de MS Word. |
| [LinkedStyleName](../../aspose.words/style/linkedstylename/) { get; set; } | Obtient/définit le nom du`Style` Lié à celui-ci. Renvoie une chaîne vide si aucun style n'est lié. |
| [List](../../aspose.words/style/list/) { get; } | Obtient la liste qui définit la mise en forme de ce style de liste. |
| [ListFormat](../../aspose.words/style/listformat/) { get; } | Donne accès aux propriétés de formatage de liste d'un style de paragraphe. |
| [Locked](../../aspose.words/style/locked/) { get; set; } | Spécifie si ce style est verrouillé. |
| [Name](../../aspose.words/style/name/) { get; set; } | Obtient ou définit le nom du style. |
| [NextParagraphStyleName](../../aspose.words/style/nextparagraphstylename/) { get; set; } | Obtient/définit le nom du style à appliquer automatiquement à un nouveau paragraphe inséré après un paragraphe formaté avec le style spécifié. |
| [ParagraphFormat](../../aspose.words/style/paragraphformat/) { get; } | Obtient la mise en forme du paragraphe du style. |
| [Priority](../../aspose.words/style/priority/) { get; set; } | Obtient/définit la valeur entière qui représente la priorité de tri des styles dans le volet Office Styles. |
| [SemiHidden](../../aspose.words/style/semihidden/) { get; set; } | Obtient/définit si le style est masqué dans la galerie Styles et dans le volet Office Styles. |
| [StyleIdentifier](../../aspose.words/style/styleidentifier/) { get; } | Obtient l'identifiant de style indépendant des paramètres régionaux pour un style intégré. |
| [Styles](../../aspose.words/style/styles/) { get; } | Obtient la collection de styles à laquelle appartient ce style. |
| [Type](../../aspose.words/style/type/) { get; } | Obtient le type de style (paragraphe ou caractère). |
| [UnhideWhenUsed](../../aspose.words/style/unhidewhenused/) { get; set; } | Obtient/définit si le style utilisé dans le document actuel est affiché dans la galerie Styles et dans le volet Office Styles. Vrai lorsque le style utilisé doit être affiché dans la galerie Styles. |

## Méthodes

| Nom | La description |
| --- | --- |
| [Equals](../../aspose.words/style/equals/#equals)(*Style*) | Compare avec le style spécifié. Les styles Istds sont comparés uniquement pour les styles intégrés. Les valeurs par défaut des styles ne sont pas incluses dans la comparaison. Le style de base, le style lié et le style du paragraphe suivant sont comparés de manière récursive. |
| [Remove](../../aspose.words/style/remove/)() | Supprime le style spécifié du document. |

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

Montre comment créer et appliquer un style personnalisé.

```csharp
Document doc = new Document();

Style style = doc.Styles.Add(StyleType.Paragraph, "MyStyle");
style.Font.Name = "Times New Roman";
style.Font.Size = 16;
style.Font.Color = Color.Navy;
// Redéfinir automatiquement le style.
style.AutomaticallyUpdate = true;

DocumentBuilder builder = new DocumentBuilder(doc);

// Appliquez l’un des styles du document au paragraphe que le générateur de documents est en train de créer.
builder.ParagraphFormat.Style = doc.Styles["MyStyle"];
builder.Writeln("Hello world!");

Style firstParagraphStyle = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Style;

Assert.AreEqual(style, firstParagraphStyle);

// Supprimez notre style personnalisé de la collection de styles du document.
doc.Styles["MyStyle"].Remove();

firstParagraphStyle = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Style;

// Tout texte qui utilise un style supprimé revient à la mise en forme par défaut.
Assert.False(doc.Styles.Any(s => s.Name == "MyStyle"));
Assert.AreEqual("Times New Roman", firstParagraphStyle.Font.Name);
Assert.AreEqual(12.0d, firstParagraphStyle.Font.Size);
Assert.AreEqual(Color.Empty.ToArgb(), firstParagraphStyle.Font.Color.ToArgb());
```

### Voir également

* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)
