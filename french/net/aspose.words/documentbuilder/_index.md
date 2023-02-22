---
title: Class DocumentBuilder
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.DocumentBuilder classe. Fournit des méthodes pour insérer du texte des images et dautres contenus spécifier la mise en forme de la police des paragraphes et des sections.
type: docs
weight: 440
url: /fr/net/aspose.words/documentbuilder/
---
## DocumentBuilder class

Fournit des méthodes pour insérer du texte, des images et d'autres contenus, spécifier la mise en forme de la police, des paragraphes et des sections.

```csharp
public class DocumentBuilder
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [DocumentBuilder](documentbuilder/#constructor)() | Initialise une nouvelle instance de cette classe. |
| [DocumentBuilder](documentbuilder/#constructor_1)(Document) | Initialise une nouvelle instance de cette classe. |

## Propriétés

| Nom | La description |
| --- | --- |
| [Bold](../../aspose.words/documentbuilder/bold/) { get; set; } | Vrai si la police est formatée en gras. |
| [CellFormat](../../aspose.words/documentbuilder/cellformat/) { get; } | Renvoie un objet qui représente les propriétés de formatage des cellules de tableau actuelles. |
| [CurrentNode](../../aspose.words/documentbuilder/currentnode/) { get; } | Obtient le nœud actuellement sélectionné dans ce DocumentBuilder. |
| [CurrentParagraph](../../aspose.words/documentbuilder/currentparagraph/) { get; } | Obtient le paragraphe actuellement sélectionné dans ce DocumentBuilder. |
| [CurrentSection](../../aspose.words/documentbuilder/currentsection/) { get; } | Obtient la section actuellement sélectionnée dans ce DocumentBuilder. |
| [CurrentStory](../../aspose.words/documentbuilder/currentstory/) { get; } | Obtient l'histoire actuellement sélectionnée dans ce DocumentBuilder. |
| [Document](../../aspose.words/documentbuilder/document/) { get; set; } | Obtient ou définit le[`Document`](./document/) objet auquel cet objet est attaché. |
| [Font](../../aspose.words/documentbuilder/font/) { get; } | Renvoie un objet qui représente les propriétés de formatage de police actuelles. |
| [IsAtEndOfParagraph](../../aspose.words/documentbuilder/isatendofparagraph/) { get; } | Renvoie true si le curseur est à la fin du paragraphe courant. |
| [IsAtStartOfParagraph](../../aspose.words/documentbuilder/isatstartofparagraph/) { get; } | Renvoie true si le curseur est au début du paragraphe courant (pas de texte avant le curseur). |
| [Italic](../../aspose.words/documentbuilder/italic/) { get; set; } | Vrai si la police est formatée en italique. |
| [ListFormat](../../aspose.words/documentbuilder/listformat/) { get; } | Renvoie un objet qui représente les propriétés de formatage de la liste actuelle. |
| [PageSetup](../../aspose.words/documentbuilder/pagesetup/) { get; } | Renvoie un objet qui représente la configuration de page actuelle et les propriétés de section. |
| [ParagraphFormat](../../aspose.words/documentbuilder/paragraphformat/) { get; } | Renvoie un objet qui représente les propriétés de formatage de paragraphe actuelles. |
| [RowFormat](../../aspose.words/documentbuilder/rowformat/) { get; } | Renvoie un objet qui représente les propriétés de formatage des lignes de tableau actuelles. |
| [Underline](../../aspose.words/documentbuilder/underline/) { get; set; } | Obtient/définit le type de soulignement pour la police actuelle. |

## Méthodes

| Nom | La description |
| --- | --- |
| [DeleteRow](../../aspose.words/documentbuilder/deleterow/)(int, int) | Supprime une ligne d'une table. |
| [EndBookmark](../../aspose.words/documentbuilder/endbookmark/)(string) | Marque la position actuelle dans le document comme fin de signet. |
| [EndColumnBookmark](../../aspose.words/documentbuilder/endcolumnbookmark/)(string) | Marque la position actuelle dans le document en tant que fin de signet de colonne. La position doit être dans une cellule du tableau. |
| [EndEditableRange](../../aspose.words/documentbuilder/endeditablerange/#endeditablerange)() | Marque la position actuelle dans le document comme une fin de plage modifiable. |
| [EndEditableRange](../../aspose.words/documentbuilder/endeditablerange/#endeditablerange_1)(EditableRangeStart) | Marque la position actuelle dans le document comme une fin de plage modifiable. |
| [EndRow](../../aspose.words/documentbuilder/endrow/)() | Termine une ligne de tableau dans le document. |
| [EndTable](../../aspose.words/documentbuilder/endtable/)() | Termine un tableau dans le document. |
| [InsertBreak](../../aspose.words/documentbuilder/insertbreak/)(BreakType) | Insère une rupture du type spécifié dans le document. |
| [InsertCell](../../aspose.words/documentbuilder/insertcell/)() | Insère une cellule de tableau dans le document. |
| [InsertChart](../../aspose.words/documentbuilder/insertchart/#insertchart_1)(ChartType, double, double) | Insère un objet graphique dans le document et le met à l'échelle à la taille spécifiée. |
| [InsertChart](../../aspose.words/documentbuilder/insertchart/#insertchart)(ChartType, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) | Insère un objet graphique dans le document et le met à l'échelle à la taille spécifiée. |
| [InsertCheckBox](../../aspose.words/documentbuilder/insertcheckbox/#insertcheckbox_1)(string, bool, int) | Insère un champ de formulaire de case à cocher à la position actuelle. |
| [InsertCheckBox](../../aspose.words/documentbuilder/insertcheckbox/#insertcheckbox)(string, bool, bool, int) | Insère un champ de formulaire de case à cocher à la position actuelle. |
| [InsertComboBox](../../aspose.words/documentbuilder/insertcombobox/)(string, string[], int) | Insère un champ de formulaire combobox à la position actuelle. |
| [InsertDocument](../../aspose.words/documentbuilder/insertdocument/#insertdocument)(Document, ImportFormatMode) | Insère un document à la position du curseur. |
| [InsertDocument](../../aspose.words/documentbuilder/insertdocument/#insertdocument_1)(Document, ImportFormatMode, ImportFormatOptions) | Insère un document à la position du curseur. |
| [InsertField](../../aspose.words/documentbuilder/insertfield/#insertfield_1)(string) | Insère un champ Word dans un document et met à jour le résultat du champ. |
| [InsertField](../../aspose.words/documentbuilder/insertfield/#insertfield)(FieldType, bool) | Insère un champ Word dans un document et met éventuellement à jour le résultat du champ. |
| [InsertField](../../aspose.words/documentbuilder/insertfield/#insertfield_2)(string, string) | Insère un champ Word dans un document sans mettre à jour le résultat du champ. |
| [InsertFootnote](../../aspose.words/documentbuilder/insertfootnote/#insertfootnote)(FootnoteType, string) | Insère une note de bas de page ou une note de fin dans le document. |
| [InsertFootnote](../../aspose.words/documentbuilder/insertfootnote/#insertfootnote_1)(FootnoteType, string, string) | Insère une note de bas de page ou une note de fin dans le document. |
| [InsertHorizontalRule](../../aspose.words/documentbuilder/inserthorizontalrule/)() | Insère une forme de règle horizontale dans le document. |
| [InsertHtml](../../aspose.words/documentbuilder/inserthtml/#inserthtml)(string) | Insère une chaîne HTML dans le document. |
| [InsertHtml](../../aspose.words/documentbuilder/inserthtml/#inserthtml_2)(string, bool) | Insère une chaîne HTML dans le document. |
| [InsertHtml](../../aspose.words/documentbuilder/inserthtml/#inserthtml_1)(string, HtmlInsertOptions) | Insère une chaîne HTML dans le document. Permet de spécifier des options supplémentaires. |
| [InsertHyperlink](../../aspose.words/documentbuilder/inserthyperlink/)(string, string, bool) | Insère un lien hypertexte dans le document. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage)(byte[]) | Insère une image d'un tableau d'octets dans le document. L'image est insérée en ligne et à l'échelle 100 %. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_3)(Image) | Insère une image à partir d'un .NETImage objet dans le document. L'image est insérée en ligne et à l'échelle 100 %. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_6)(Stream) | Insère une image d'un flux dans le document. L'image est insérée en ligne et à l'échelle 100 %. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_9)(string) | Insère une image à partir d'un fichier ou d'une URL dans le document. L'image est insérée en ligne et à l'échelle 100 %. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_2)(byte[], double, double) | Insère une image en ligne à partir d'un tableau d'octets dans le document et la met à l'échelle à la taille spécifiée. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_5)(Image, double, double) | Insère une image en ligne à partir d'un .NETImage objet dans le document et le redimensionne à la taille spécifiée. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_8)(Stream, double, double) | Insère une image en ligne à partir d'un flux dans le document et la redimensionne à la taille spécifiée. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_11)(string, double, double) | Insère une image en ligne à partir d'un fichier ou d'une URL dans le document et la redimensionne à la taille spécifiée. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_1)(byte[], RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) | Insère une image à partir d'un tableau d'octets à la position et à la taille spécifiées. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_4)(Image, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) | Insère une image à partir d'un .NETImage objet à la position et à la taille spécifiées. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_7)(Stream, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) | Insère une image à partir d'un flux à la position et à la taille spécifiées. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_10)(string, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) | Insère une image à partir d'un fichier ou d'une URL à la position et à la taille spécifiées. |
| [InsertNode](../../aspose.words/documentbuilder/insertnode/)(Node) | Insère un nœud de niveau de texte à l'intérieur du paragraphe actuel avant le curseur. |
| [InsertOleObject](../../aspose.words/documentbuilder/insertoleobject/#insertoleobject)(Stream, string, bool, Stream) | Insère un objet OLE incorporé à partir d'un flux dans le document. |
| [InsertOleObject](../../aspose.words/documentbuilder/insertoleobject/#insertoleobject_1)(string, bool, bool, Stream) | Insère un objet OLE incorporé ou lié à partir d'un fichier dans le document. Détecte le type d'objet OLE à l'aide de l'extension de fichier. |
| [InsertOleObject](../../aspose.words/documentbuilder/insertoleobject/#insertoleobject_2)(string, string, bool, bool, Stream) | Insère un objet OLE incorporé ou lié à partir d'un fichier dans le document. Détecte le type d'objet OLE à l'aide du paramètre progID donné. |
| [InsertOleObjectAsIcon](../../aspose.words/documentbuilder/insertoleobjectasicon/#insertoleobjectasicon)(Stream, string, string, string) | Insère un objet OLE intégré en tant qu'icône d'un flux dans le document. Permet de spécifier le fichier d'icône et la légende. Détecte le type d'objet OLE à l'aide du paramètre progID donné. |
| [InsertOleObjectAsIcon](../../aspose.words/documentbuilder/insertoleobjectasicon/#insertoleobjectasicon_1)(string, bool, string, string) | Insère un objet OLE intégré ou lié en tant qu'icône dans le document. Permet de spécifier le fichier d'icône et la légende. Détecte le type d'objet OLE à l'aide de l'extension de fichier. |
| [InsertOleObjectAsIcon](../../aspose.words/documentbuilder/insertoleobjectasicon/#insertoleobjectasicon_2)(string, string, bool, string, string) | Insère un objet OLE intégré ou lié en tant qu'icône dans le document. Permet de spécifier le fichier d'icône et la légende. Détecte le type d'objet OLE à l'aide du paramètre progID donné. |
| [InsertOnlineVideo](../../aspose.words/documentbuilder/insertonlinevideo/#insertonlinevideo_1)(string, double, double) | Insère un objet vidéo en ligne dans le document et le redimensionne à la taille spécifiée. |
| [InsertOnlineVideo](../../aspose.words/documentbuilder/insertonlinevideo/#insertonlinevideo_3)(string, string, byte[], double, double) | Insère un objet vidéo en ligne dans le document et le redimensionne à la taille spécifiée. |
| [InsertOnlineVideo](../../aspose.words/documentbuilder/insertonlinevideo/#insertonlinevideo)(string, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) | Insère un objet vidéo en ligne dans le document et le redimensionne à la taille spécifiée. |
| [InsertOnlineVideo](../../aspose.words/documentbuilder/insertonlinevideo/#insertonlinevideo_2)(string, string, byte[], RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) | Insère un objet vidéo en ligne dans le document et le redimensionne à la taille spécifiée. |
| [InsertParagraph](../../aspose.words/documentbuilder/insertparagraph/)() | Insère un saut de paragraphe dans le document. |
| [InsertShape](../../aspose.words/documentbuilder/insertshape/#insertshape_1)(ShapeType, double, double) | Insère une forme en ligne avec le type et la taille spécifiés. |
| [InsertShape](../../aspose.words/documentbuilder/insertshape/#insertshape)(ShapeType, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) | Insère une forme flottante avec une position, une taille et un type d'habillage de texte spécifiés. |
| [InsertSignatureLine](../../aspose.words/documentbuilder/insertsignatureline/#insertsignatureline)(SignatureLineOptions) | Insère une ligne de signature à la position actuelle. |
| [InsertSignatureLine](../../aspose.words/documentbuilder/insertsignatureline/#insertsignatureline_1)(SignatureLineOptions, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, WrapType) | Insère une ligne de signature à la position spécifiée. |
| [InsertStyleSeparator](../../aspose.words/documentbuilder/insertstyleseparator/)() | Insère un séparateur de style dans le document. |
| [InsertTableOfContents](../../aspose.words/documentbuilder/inserttableofcontents/)(string) | Insère un champ TOC (table des matières) dans le document. |
| [InsertTextInput](../../aspose.words/documentbuilder/inserttextinput/)(string, TextFormFieldType, string, string, int) | Insère un champ de formulaire de texte à la position actuelle. |
| [MoveTo](../../aspose.words/documentbuilder/moveto/)(Node) | Déplace le curseur vers un nœud en ligne ou à la fin d'un paragraphe. |
| [MoveToBookmark](../../aspose.words/documentbuilder/movetobookmark/#movetobookmark)(string) | Déplace le curseur vers un signet. |
| [MoveToBookmark](../../aspose.words/documentbuilder/movetobookmark/#movetobookmark_1)(string, bool, bool) | Déplace le curseur vers un signet avec une plus grande précision. |
| [MoveToCell](../../aspose.words/documentbuilder/movetocell/)(int, int, int, int) | Déplace le curseur vers une cellule du tableau dans la section actuelle. |
| [MoveToDocumentEnd](../../aspose.words/documentbuilder/movetodocumentend/)() | Déplace le curseur à la fin du document. |
| [MoveToDocumentStart](../../aspose.words/documentbuilder/movetodocumentstart/)() | Déplace le curseur au début du document. |
| [MoveToField](../../aspose.words/documentbuilder/movetofield/)(Field, bool) | Déplace le curseur vers un champ du document. |
| [MoveToHeaderFooter](../../aspose.words/documentbuilder/movetoheaderfooter/)(HeaderFooterType) | Déplace le curseur au début d'un en-tête ou d'un pied de page dans la section actuelle. |
| [MoveToMergeField](../../aspose.words/documentbuilder/movetomergefield/#movetomergefield)(string) | Déplace le curseur vers une position juste au-delà du champ de fusion spécifié et supprime le champ de fusion. |
| [MoveToMergeField](../../aspose.words/documentbuilder/movetomergefield/#movetomergefield_1)(string, bool, bool) | Déplace le champ de fusion vers le champ de fusion spécifié. |
| [MoveToParagraph](../../aspose.words/documentbuilder/movetoparagraph/)(int, int) | Déplace le curseur vers un paragraphe de la section actuelle. |
| [MoveToSection](../../aspose.words/documentbuilder/movetosection/)(int) | Déplace le curseur au début du corps dans une section spécifiée. |
| [PopFont](../../aspose.words/documentbuilder/popfont/)() | Récupère la mise en forme des caractères précédemment enregistrée sur la pile. |
| [PushFont](../../aspose.words/documentbuilder/pushfont/)() | Enregistre la mise en forme actuelle des caractères sur la pile. |
| [StartBookmark](../../aspose.words/documentbuilder/startbookmark/)(string) | Marque la position actuelle dans le document comme début de signet. |
| [StartColumnBookmark](../../aspose.words/documentbuilder/startcolumnbookmark/)(string) | Marque la position actuelle dans le document comme début de signet de colonne. La position doit être dans une cellule du tableau. |
| [StartEditableRange](../../aspose.words/documentbuilder/starteditablerange/)() | Marque la position actuelle dans le document comme début de plage modifiable. |
| [StartTable](../../aspose.words/documentbuilder/starttable/)() | Démarre un tableau dans le document. |
| [Write](../../aspose.words/documentbuilder/write/)(string) | Insère une chaîne dans le document à la position d'insertion actuelle. |
| [Writeln](../../aspose.words/documentbuilder/writeln/#writeln)() | Insère un saut de paragraphe dans le document. |
| [Writeln](../../aspose.words/documentbuilder/writeln/#writeln_1)(string) | Insère une chaîne et un saut de paragraphe dans le document. |

### Remarques

**Générateur de documents** rend le processus de construction d'un **Document** plus facile.  **Document**est un objet composite constitué d'un arbre de nœuds et bien qu'il soit possible d'insérer des nœuds content directement dans l'arbre, cela nécessite une bonne compréhension de la structure de l'arbre.  **Générateur de documents** est une "façade" pour la structure complexe de **Document** et permet d'insérer rapidement et facilement du contenu et une mise en forme.

Créer un **Générateur de documents** et l'associer à un[`Document`](./document/).

La **Générateur de documents** a un curseur interne où le texte sera inséré lorsque vous appelez[`Write`](./write/) ,[`Writeln`](./writeln/) ,[`InsertBreak`](./insertbreak/) et d'autres méthodes. Vous pouvez naviguer dans le **Générateur de documents** curseur vers un autre emplacement dans un document à l'aide de diverses méthodes MoveToXXX.

Utilisez le[`Font`](./font/) propriété pour spécifier le formatage des caractères qui s'appliquera à tout le texte inséré à partir de la position actuelle dans le document.

Utilisez le[`ParagraphFormat`](./paragraphformat/) propriété pour spécifier le formatage des paragraphes pour le current et tous les paragraphes qui seront insérés.

Utilisez le[`PageSetup`](./pagesetup/)propriété pour spécifier les propriétés de page et de section pour la section current et toutes les sections qui seront insérées.

Utilisez le[`CellFormat`](./cellformat/) et[`RowFormat`](./rowformat/) properties pour spécifier les propriétés de formatage pour les cellules et les lignes du tableau. Utilisateur le[`InsertCell`](./insertcell/) et [`EndRow`](./endrow/) Méthodes pour construire une table.

Notez que **Police de caractère** , **FormatParagraphe** et **Mise en page** les propriétés sont mises à jour chaque fois que vous naviguez vers un endroit différent dans le document pour refléter les propriétés de mise en forme disponibles au nouvel emplacement.

### Exemples

Montre comment utiliser un générateur de document pour créer un tableau.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Démarre le tableau, puis remplit la première ligne avec deux cellules.
builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, Cell 1.");
builder.InsertCell();
builder.Write("Row 1, Cell 2.");

// Appelez la méthode "EndRow" du générateur pour démarrer une nouvelle ligne.
builder.EndRow();
builder.InsertCell();
builder.Write("Row 2, Cell 1.");
builder.InsertCell();
builder.Write("Row 2, Cell 2.");
builder.EndTable();

doc.Save(ArtifactsDir + "DocumentBuilder.CreateTable.docx");
```

Montre comment créer des en-têtes et des pieds de page dans un document à l'aide de DocumentBuilder.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Spécifiez que nous voulons des en-têtes et des pieds de page différents pour les premières pages, paires et impaires.
builder.PageSetup.DifferentFirstPageHeaderFooter = true;
builder.PageSetup.OddAndEvenPagesHeaderFooter = true;

// Crée les en-têtes, puis ajoute trois pages au document pour afficher chaque type d'en-tête.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderFirst);
builder.Write("Header for the first page");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderEven);
builder.Write("Header for even pages");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Write("Header for all other pages");

builder.MoveToSection(0);
builder.Writeln("Page1");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page2");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page3");

doc.Save(ArtifactsDir + "DocumentBuilder.HeadersAndFooters.docx");
```

Montre comment créer un tableau avec des bordures personnalisées.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartTable();

// Définition des options de formatage de tableau pour un générateur de document
// les appliquera à chaque ligne et cellule que nous ajouterons avec.
builder.ParagraphFormat.Alignment = ParagraphAlignment.Center;

builder.CellFormat.ClearFormatting();
builder.CellFormat.Width = 150;
builder.CellFormat.VerticalAlignment = CellVerticalAlignment.Center;
builder.CellFormat.Shading.BackgroundPatternColor = Color.GreenYellow;
builder.CellFormat.WrapText = false;
builder.CellFormat.FitText = true;

builder.RowFormat.ClearFormatting();
builder.RowFormat.HeightRule = HeightRule.Exactly;
builder.RowFormat.Height = 50;
builder.RowFormat.Borders.LineStyle = LineStyle.Engrave3D;
builder.RowFormat.Borders.Color = Color.Orange;

builder.InsertCell();
builder.Write("Row 1, Col 1");

builder.InsertCell();
builder.Write("Row 1, Col 2");
builder.EndRow();

// Changer la mise en forme l'appliquera à la cellule courante,
// et toutes les nouvelles cellules que nous créons avec le constructeur par la suite.
// Cela n'affectera pas les cellules que nous avons ajoutées précédemment.
builder.CellFormat.Shading.ClearFormatting();

builder.InsertCell();
builder.Write("Row 2, Col 1");

builder.InsertCell();
builder.Write("Row 2, Col 2");

builder.EndRow();

// Augmente la hauteur de ligne pour s'adapter au texte vertical.
builder.InsertCell();
builder.RowFormat.Height = 150;
builder.CellFormat.Orientation = TextOrientation.Upward;
builder.Write("Row 3, Col 1");

builder.InsertCell();
builder.CellFormat.Orientation = TextOrientation.Downward;
builder.Write("Row 3, Col 2");

builder.EndRow();
builder.EndTable();

doc.Save(ArtifactsDir + "DocumentBuilder.InsertTable.docx");
```

### Voir également

* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)


