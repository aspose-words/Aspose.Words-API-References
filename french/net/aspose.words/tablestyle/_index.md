---
title: Class TableStyle
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.TableStyle classe. Représente un style de tableau.
type: docs
weight: 6220
url: /fr/net/aspose.words/tablestyle/
---
## TableStyle class

Représente un style de tableau.

Pour en savoir plus, visitez le[Travailler avec des tableaux](https://docs.aspose.com/words/net/working-with-tables/) article documentaire.

```csharp
public class TableStyle : Style
```

## Propriétés

| Nom | La description |
| --- | --- |
| [Aliases](../../aspose.words/style/aliases/) { get; } | Obtient tous les alias de ce style. Si le style n'a pas d'alias, un tableau de chaînes vide est renvoyé. |
| [Alignment](../../aspose.words/tablestyle/alignment/) { get; set; } | Spécifie l'alignement du style de tableau. |
| [AllowBreakAcrossPages](../../aspose.words/tablestyle/allowbreakacrosspages/) { get; set; } | Obtient ou définit un indicateur indiquant si le texte d'une ligne de tableau est autorisé à être divisé sur un saut de page. |
| [AutomaticallyUpdate](../../aspose.words/style/automaticallyupdate/) { get; set; } | Spécifie si ce style est automatiquement redéfini en fonction de la valeur appropriée. |
| [BaseStyleName](../../aspose.words/style/basestylename/) { get; set; } | Obtient/définit le nom du style sur lequel ce style est basé. |
| [Bidi](../../aspose.words/tablestyle/bidi/) { get; set; } | Obtient ou définit s'il s'agit d'un style pour un tableau de droite à gauche. |
| [Borders](../../aspose.words/tablestyle/borders/) { get; } | Obtient la collection de bordures de cellules par défaut pour le style. |
| [BottomPadding](../../aspose.words/tablestyle/bottompadding/) { get; set; } | Obtient ou définit la quantité d'espace (en points) à ajouter sous le contenu des cellules du tableau. |
| [BuiltIn](../../aspose.words/style/builtin/) { get; } | True si ce style est l'un des styles intégrés dans MS Word. |
| [CellSpacing](../../aspose.words/tablestyle/cellspacing/) { get; set; } | Obtient ou définit la quantité d'espace (en points) entre les cellules. |
| [ColumnStripe](../../aspose.words/tablestyle/columnstripe/) { get; set; } | Obtient ou définit un certain nombre de colonnes à inclure dans la bande lorsque le style spécifie une bande de colonnes paires/impaires. |
| [ConditionalStyles](../../aspose.words/tablestyle/conditionalstyles/) { get; } | Collection de styles conditionnels pouvant être définis pour ce style de tableau. |
| [Document](../../aspose.words/style/document/) { get; } | Obtient le document propriétaire. |
| [Font](../../aspose.words/style/font/) { get; } | Obtient le formatage des caractères du style. |
| [IsHeading](../../aspose.words/style/isheading/) { get; } | Vrai lorsque le style est l'un des styles de titre intégrés. |
| [IsQuickStyle](../../aspose.words/style/isquickstyle/) { get; set; } | Spécifie si ce style est affiché dans la galerie de styles rapides dans l'interface utilisateur de MS Word. |
| [LeftIndent](../../aspose.words/tablestyle/leftindent/) { get; set; } | Obtient ou définit la valeur qui représente le retrait gauche d'une table. |
| [LeftPadding](../../aspose.words/tablestyle/leftpadding/) { get; set; } | Obtient ou définit la quantité d'espace (en points) à ajouter à gauche du contenu des cellules du tableau. |
| [LinkedStyleName](../../aspose.words/style/linkedstylename/) { get; } | Obtient le nom du[`Style`](../style/) lié à celui-ci. Renvoie une chaîne vide si aucun style n'est lié. |
| [List](../../aspose.words/style/list/) { get; } | Obtient la liste qui définit le formatage de ce style de liste. |
| [ListFormat](../../aspose.words/style/listformat/) { get; } | Permet d'accéder aux propriétés de formatage de liste d'un style de paragraphe. |
| [Locked](../../aspose.words/style/locked/) { get; set; } |  |
| [Name](../../aspose.words/style/name/) { get; set; } | Obtient ou définit le nom du style. |
| [NextParagraphStyleName](../../aspose.words/style/nextparagraphstylename/) { get; set; } | Obtient/définit le nom du style à appliquer automatiquement à un nouveau paragraphe inséré après un paragraphe formaté avec le style spécifié. |
| [ParagraphFormat](../../aspose.words/style/paragraphformat/) { get; } | Obtient la mise en forme du paragraphe du style. |
| [RightPadding](../../aspose.words/tablestyle/rightpadding/) { get; set; } | Obtient ou définit la quantité d'espace (en points) à ajouter à droite du contenu des cellules du tableau. |
| [RowStripe](../../aspose.words/tablestyle/rowstripe/) { get; set; } | Obtient ou définit un nombre de lignes à inclure dans la bande lorsque le style spécifie une bande de ligne paire/impaire. |
| [Shading](../../aspose.words/tablestyle/shading/) { get; } | Obtient un[`Shading`](../shading/) objet qui fait référence au formatage d'ombrage des cellules du tableau. |
| [StyleIdentifier](../../aspose.words/style/styleidentifier/) { get; } | Obtient l'identifiant de style indépendant des paramètres régionaux pour un style intégré. |
| [Styles](../../aspose.words/style/styles/) { get; } | Obtient la collection de styles à laquelle appartient ce style. |
| [TopPadding](../../aspose.words/tablestyle/toppadding/) { get; set; } | Obtient ou définit la quantité d'espace (en points) à ajouter au-dessus du contenu des cellules du tableau. |
| [Type](../../aspose.words/style/type/) { get; } | Obtient le type de style (paragraphe ou caractère). |
| [VerticalAlignment](../../aspose.words/tablestyle/verticalalignment/) { get; set; } | Spécifie l'alignement vertical des cellules. |

## Méthodes

| Nom | La description |
| --- | --- |
| [Equals](../../aspose.words/style/equals/)(Style) | Se compare au style spécifié. Les styles Istds sont comparés uniquement pour les styles intégrés. Les styles par défaut ne sont pas inclus dans la comparaison. Le style de base, le style lié et le style du paragraphe suivant sont comparés de manière récursive. |
| [Remove](../../aspose.words/style/remove/)() | Supprime le style spécifié du document. |

### Exemples

Montre comment créer des paramètres de style personnalisés pour le tableau.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Name");
builder.InsertCell();
builder.Write("مرحبًا");
builder.EndRow();
builder.InsertCell();
builder.InsertCell();
builder.EndTable();

TableStyle tableStyle = (TableStyle)doc.Styles.Add(StyleType.Table, "MyTableStyle1");
tableStyle.AllowBreakAcrossPages = true;
tableStyle.Bidi = true;
tableStyle.CellSpacing = 5;
tableStyle.BottomPadding = 20;
tableStyle.LeftPadding = 5;
tableStyle.RightPadding = 10;
tableStyle.TopPadding = 20;
tableStyle.Shading.BackgroundPatternColor = Color.AntiqueWhite;
tableStyle.Borders.Color = Color.Blue;
tableStyle.Borders.LineStyle = LineStyle.DotDash;
tableStyle.VerticalAlignment = CellVerticalAlignment.Center;

table.Style = tableStyle;

// La définition des propriétés de style d'un tableau peut affecter les propriétés du tableau lui-même.
Assert.True(table.Bidi);
Assert.AreEqual(5.0d, table.CellSpacing);
Assert.AreEqual("MyTableStyle1", table.StyleName);

doc.Save(ArtifactsDir + "Table.TableStyleCreation.docx");
```

### Voir également

* class [Style](../style/)
* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)


