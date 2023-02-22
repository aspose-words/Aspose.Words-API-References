---
title: Class FieldToc
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.Fields.FieldToc classe. Implémente le champ TOC.
type: docs
weight: 2380
url: /fr/net/aspose.words.fields/fieldtoc/
---
## FieldToc class

Implémente le champ TOC.

```csharp
public class FieldToc : Field
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [FieldToc](fieldtoc/)() | Default_Constructor |

## Propriétés

| Nom | La description |
| --- | --- |
| [BookmarkName](../../aspose.words.fields/fieldtoc/bookmarkname/) { get; set; } | Obtient ou définit le nom du signet qui marque la partie du document utilisée pour créer le tableau. |
| [CaptionlessTableOfFiguresLabel](../../aspose.words.fields/fieldtoc/captionlesstableoffigureslabel/) { get; set; } | Obtient ou définit le nom de l'identificateur de séquence utilisé lors de la création d'un tableau de figures qui n'inclut pas l'étiquette et le numéro de la légende . |
| [CustomStyles](../../aspose.words.fields/fieldtoc/customstyles/) { get; set; } | Obtient ou définit une liste de styles autres que les styles de titre intégrés à inclure dans la table des matières. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Obtient le texte qui représente le résultat du champ affiché. |
| [End](../../aspose.words.fields/field/end/) { get; } | Obtient le nœud qui représente la fin du champ. |
| [EntryIdentifier](../../aspose.words.fields/fieldtoc/entryidentifier/) { get; set; } | Obtient ou définit une chaîne qui doit correspondre aux identificateurs de type des champs TC inclus. |
| [EntryLevelRange](../../aspose.words.fields/fieldtoc/entrylevelrange/) { get; set; } | Obtient ou définit une plage de niveaux des entrées de la table des matières à inclure. |
| [EntrySeparator](../../aspose.words.fields/fieldtoc/entryseparator/) { get; set; } | Obtient ou définit une séquence de caractères qui séparent une entrée et son numéro de page. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Obtient un[`FieldFormat`](../fieldformat/) objet qui fournit un accès typé au formatage du champ. |
| [HeadingLevelRange](../../aspose.words.fields/fieldtoc/headinglevelrange/) { get; set; } | Obtient ou définit une plage de niveaux de titre à inclure. |
| [HideInWebLayout](../../aspose.words.fields/fieldtoc/hideinweblayout/) { get; set; } | Obtient ou définit s'il faut masquer l'amorce de tabulation et les numéros de page en mode Mise en page Web. |
| [InsertHyperlinks](../../aspose.words.fields/fieldtoc/inserthyperlinks/) { get; set; } | Obtient ou définit s'il faut créer des liens hypertexte entre les entrées de la table des matières. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Obtient ou définit si le résultat actuel du champ n'est plus correct (périmé) en raison d'autres modifications apportées au document. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Obtient ou définit si le champ est verrouillé (ne doit pas recalculer son résultat). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Obtient ou définit le LCID du champ. |
| [PageNumberOmittingLevelRange](../../aspose.words.fields/fieldtoc/pagenumberomittinglevelrange/) { get; set; } | Obtient ou définit une plage de niveaux des entrées de la table des matières à partir de laquelle omettre les numéros de page. |
| [PrefixedSequenceIdentifier](../../aspose.words.fields/fieldtoc/prefixedsequenceidentifier/) { get; set; } | Obtient ou définit l'identifiant d'une séquence pour laquelle un préfixe doit être ajouté au numéro de page de l'entrée. |
| [PreserveLineBreaks](../../aspose.words.fields/fieldtoc/preservelinebreaks/) { get; set; } | Obtient ou définit s'il faut conserver les caractères de nouvelle ligne dans les entrées de table. |
| [PreserveTabs](../../aspose.words.fields/fieldtoc/preservetabs/) { get; set; } | Obtient ou définit s'il faut conserver les entrées de tabulation dans les entrées de table. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Obtient ou définit le texte qui se trouve entre le séparateur de champ et la fin du champ. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Obtient le nœud qui représente le séparateur de champs. Peut être null. |
| [SequenceSeparator](../../aspose.words.fields/fieldtoc/sequenceseparator/) { get; set; } | Obtient ou définit la séquence de caractères utilisée pour séparer les numéros de séquence et les numéros de page. |
| [Start](../../aspose.words.fields/field/start/) { get; } | Obtient le nœud qui représente le début du champ. |
| [TableOfFiguresLabel](../../aspose.words.fields/fieldtoc/tableoffigureslabel/) { get; set; } | Obtient ou définit le nom de l'identificateur de séquence utilisé lors de la création d'un tableau des illustrations. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Obtient le type de champ Microsoft Word. |
| [UseParagraphOutlineLevel](../../aspose.words.fields/fieldtoc/useparagraphoutlinelevel/) { get; set; } | Obtient ou définit s'il faut utiliser le niveau de plan de paragraphe appliqué. |

## Méthodes

| Nom | La description |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Renvoie le texte entre le début du champ et le séparateur de champ (ou la fin du champ s'il n'y a pas de séparateur). Le code de champ et le résultat du champ des champs enfants sont inclus. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(bool) | Renvoie le texte entre le début du champ et le séparateur de champ (ou la fin du champ s'il n'y a pas de séparateur). |
| [Remove](../../aspose.words.fields/field/remove/)() | Supprime le champ du document. Renvoie un nœud juste après le champ. Si la fin du champ est le dernier enfant de son nœud parent, renvoie son paragraphe parent. Si le champ est déjà supprimé, renvoie **nul** . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Effectue la dissociation du champ. |
| [Update](../../aspose.words.fields/field/update/)() | Effectue la mise à jour du champ. Lance si le champ est déjà mis à jour. |
| [Update](../../aspose.words.fields/field/update/)(bool) | Effectue une mise à jour du champ. Lance si le champ est déjà mis à jour. |
| [UpdatePageNumbers](../../aspose.words.fields/fieldtoc/updatepagenumbers/)() | Met à jour les numéros de page des éléments de cette table des matières. |

### Remarques

Construit une table des matières (qui peut également être une table des figures) en utilisant les entrées spécifiées par les champs TC, leurs niveaux de titre et les styles spécifiés, et insère cette table à cet endroit dans le document.

### Exemples

Montre comment insérer une table des matières et la remplir avec des entrées basées sur les styles de titre.

```csharp
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.StartBookmark("MyBookmark");

    // Insère un champ TOC, qui compilera tous les titres dans une table des matières.
    // Pour chaque en-tête, ce champ créera une ligne avec le texte dans ce style d'en-tête à gauche,
    // et la page sur laquelle le titre apparaît à droite.
    FieldToc field = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

    // Utilisez la propriété BookmarkName pour ne lister que les en-têtes
    // qui apparaissent dans les limites d'un signet avec le nom "MyBookmark".
    field.BookmarkName = "MyBookmark";

    // Le texte avec un style de titre intégré, tel que "Titre 1", qui lui est appliqué comptera comme un titre.
    // Nous pouvons nommer des styles supplémentaires à sélectionner comme en-têtes par la table des matières dans cette propriété et leurs niveaux de table des matières.
    field.CustomStyles = "Quote; 6; Intense Quote; 7";

    // Par défaut, les niveaux Styles/TOC sont séparés dans la propriété CustomStyles par une virgule,
    // mais nous pouvons définir un délimiteur personnalisé dans cette propriété.
    doc.FieldOptions.CustomTocStyleSeparator = ";";

    // Configurez le champ pour exclure tous les titres qui ont des niveaux de table des matières en dehors de cette plage.
    field.HeadingLevelRange = "1-3";

    // La table des matières n'affichera pas les numéros de page des titres dont les niveaux de table des matières se situent dans cette plage.
    field.PageNumberOmittingLevelRange = "2-5";

     // Définissez une chaîne personnalisée qui séparera chaque en-tête de son numéro de page.
    field.EntrySeparator = "-";
    field.InsertHyperlinks = true;
    field.HideInWebLayout = false;
    field.PreserveLineBreaks = true;
    field.PreserveTabs = true;
    field.UseParagraphOutlineLevel = false;

    InsertNewPageWithHeading(builder, "First entry", "Heading 1");
    builder.Writeln("Paragraph text.");
    InsertNewPageWithHeading(builder, "Second entry", "Heading 1");
    InsertNewPageWithHeading(builder, "Third entry", "Quote");
    InsertNewPageWithHeading(builder, "Fourth entry", "Intense Quote");

    // Ces deux en-têtes auront les numéros de page omis car ils se situent dans la plage "2-5".
    InsertNewPageWithHeading(builder, "Fifth entry", "Heading 2");
    InsertNewPageWithHeading(builder, "Sixth entry", "Heading 3");

    // Cette entrée n'apparaît pas car "Heading 4" est en dehors de la plage "1-3" que nous avons définie précédemment.
    InsertNewPageWithHeading(builder, "Seventh entry", "Heading 4");

    builder.EndBookmark("MyBookmark");
    builder.Writeln("Paragraph text.");

    // Cette entrée n'apparaît pas car elle se trouve en dehors du signet spécifié par la table des matières.
    InsertNewPageWithHeading(builder, "Eighth entry", "Heading 1");

    Assert.AreEqual(" TOC  \\b MyBookmark \\t \"Quote; 6; Intense Quote; 7\" \\o 1-3 \\n 2-5 \\p - \\h \\x \\w", field.GetFieldCode());

    field.UpdatePageNumbers();
    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.TOC.docx");

/// <summary>
/// Commence une nouvelle page et insère un paragraphe d'un style spécifié.
/// </summary>
public void InsertNewPageWithHeading(DocumentBuilder builder, string captionText, string styleName)
{
    builder.InsertBreak(BreakType.PageBreak);
    string originalStyle = builder.ParagraphFormat.StyleName;
    builder.ParagraphFormat.Style = builder.Document.Styles[styleName];
    builder.Writeln(captionText);
    builder.ParagraphFormat.Style = builder.Document.Styles[originalStyle];
}
```

Montre comment remplir un champ TOC avec des entrées à l'aide des champs SEQ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Un champ TOC peut créer une entrée dans sa table des matières pour chaque champ SEQ présent dans le document.
// Chaque entrée contient le paragraphe qui inclut le champ SEQ et le numéro de page sur lequel le champ apparaît.
FieldToc fieldToc = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

// Les champs SEQ affichent un décompte qui s'incrémente à chaque champ SEQ.
// Ces champs conservent également des décomptes séparés pour chaque séquence nommée unique
// identifié par la propriété "SequenceIdentifier" du champ SEQ.
// Utilisez la propriété "TableOfFiguresLabel" pour nommer une séquence principale pour la table des matières.
// Désormais, cette table des matières créera uniquement des entrées à partir des champs SEQ avec leur "SequenceIdentifier" défini sur "MySequence".
fieldToc.TableOfFiguresLabel = "MySequence";

// Nous pouvons nommer une autre séquence de champs SEQ dans la propriété "PrefixedSequenceIdentifier".
 // Les champs SEQ de cette séquence de préfixes ne créeront pas d'entrées TOC.
// Chaque entrée de table des matières créée à partir d'un champ SEQ de séquence principale affichera désormais également le nombre qui
// la séquence de préfixe est actuellement activée dans le champ SEQ de séquence primaire qui a effectué l'entrée.
fieldToc.PrefixedSequenceIdentifier = "PrefixSequence";

// Chaque entrée TOC affichera le nombre de séquences de préfixes immédiatement à gauche
// du numéro de page sur lequel apparaît le champ SEQ de la séquence principale.
// Nous pouvons spécifier un séparateur personnalisé qui apparaîtra entre ces deux nombres.
fieldToc.SequenceSeparator = ">";

Assert.AreEqual(" TOC  \\c MySequence \\s PrefixSequence \\d >", fieldToc.GetFieldCode());

builder.InsertBreak(BreakType.PageBreak);

// Il existe deux manières d'utiliser les champs SEQ pour remplir cette table des matières.
// 1 - Insertion d'un champ SEQ appartenant à la séquence de préfixe de la TOC :
// Ce champ incrémentera le nombre de séquences SEQ pour la "PrefixSequence" de 1.
// Comme ce champ n'appartient pas à la séquence principale identifiée
// par la propriété "TableOfFiguresLabel" de la table des matières, elle n'apparaîtra pas comme une entrée.
FieldSeq fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "PrefixSequence";
builder.InsertParagraph();

Assert.AreEqual(" SEQ  PrefixSequence", fieldSeq.GetFieldCode());

// 2 - Insertion d'un champ SEQ appartenant à la séquence principale de la TOC :
// Ce champ SEQ créera une entrée dans la table des matières.
// L'entrée TOC contiendra le paragraphe dans lequel se trouve le champ SEQ et le numéro de la page sur laquelle il apparaît.
// Cette entrée affichera également le décompte auquel se trouve actuellement la séquence de préfixes,
// séparé du numéro de page par la valeur de la propriété SeqenceSeparator de la table des matières.
// Le décompte "PrefixSequence" est à 1, ce champ SEQ de la séquence principale est en page 2,
// et le séparateur est ">", donc l'entrée affichera "1>2".
builder.Write("First TOC entry, MySequence #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";

Assert.AreEqual(" SEQ  MySequence", fieldSeq.GetFieldCode());

// Insérez une page, avancez la séquence de préfixes de 2 et insérez un champ SEQ pour créer une entrée TOC par la suite.
// La séquence du préfixe est maintenant à 2, et le champ SEQ de la séquence principale est à la page 3,
// donc l'entrée TOC affichera "2>3" à son nombre de pages.
builder.InsertBreak(BreakType.PageBreak);
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "PrefixSequence";
builder.InsertParagraph();
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
builder.Write("Second TOC entry, MySequence #");
fieldSeq.SequenceIdentifier = "MySequence";

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.TOC.SEQ.docx");
```

### Voir également

* class [Field](../field/)
* espace de noms [Aspose.Words.Fields](../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../)


