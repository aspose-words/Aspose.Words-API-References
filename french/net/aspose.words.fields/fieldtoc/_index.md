---
title: FieldToc Class
linktitle: FieldToc
articleTitle: FieldToc
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.Fields.FieldToc pour créer facilement des tables des matières dans vos documents. Améliorez votre flux de travail grâce à de puissantes fonctionnalités !
type: docs
weight: 2940
url: /fr/net/aspose.words.fields/fieldtoc/
---
## FieldToc class

Implémente le champ TOC.

Pour en savoir plus, visitez le[Travailler avec les champs](https://docs.aspose.com/words/net/working-with-fields/) article de documentation.

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
| [CaptionlessTableOfFiguresLabel](../../aspose.words.fields/fieldtoc/captionlesstableoffigureslabel/) { get; set; } | Obtient ou définit le nom de l'identifiant de séquence utilisé lors de la création d'un tableau de figures qui n'inclut pas l'étiquette et le numéro de la légende . |
| [CustomStyles](../../aspose.words.fields/fieldtoc/customstyles/) { get; set; } | Obtient ou définit une liste de styles autres que les styles de titre intégrés à inclure dans la table des matières. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Obtient le texte qui représente le résultat du champ affiché. |
| [End](../../aspose.words.fields/field/end/) { get; } | Obtient le nœud qui représente la fin du champ. |
| [EntryIdentifier](../../aspose.words.fields/fieldtoc/entryidentifier/) { get; set; } | Obtient ou définit une chaîne qui doit correspondre aux identifiants de type des champs TC inclus. |
| [EntryLevelRange](../../aspose.words.fields/fieldtoc/entrylevelrange/) { get; set; } | Obtient ou définit une plage de niveaux des entrées de la table des matières à inclure. |
| [EntrySeparator](../../aspose.words.fields/fieldtoc/entryseparator/) { get; set; } | Obtient ou définit une séquence de caractères qui sépare une entrée et son numéro de page. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Obtient un[`FieldFormat`](../fieldformat/)objet qui fournit un accès typé au formatage du champ. |
| [HeadingLevelRange](../../aspose.words.fields/fieldtoc/headinglevelrange/) { get; set; } | Obtient ou définit une plage de niveaux de titre à inclure. |
| [HideInWebLayout](../../aspose.words.fields/fieldtoc/hideinweblayout/) { get; set; } | Obtient ou définit s'il faut masquer le leader des tabulations et les numéros de page dans la vue de mise en page Web. |
| [InsertHyperlinks](../../aspose.words.fields/fieldtoc/inserthyperlinks/) { get; set; } | Obtient ou définit s'il faut transformer les entrées de la table des matières en hyperliens. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Obtient ou définit si le résultat actuel du champ n'est plus correct (obsolète) en raison d'autres modifications apportées au document. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Obtient ou définit si le champ est verrouillé (ne doit pas recalculer son résultat). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Obtient ou définit le LCID du champ. |
| [PageNumberOmittingLevelRange](../../aspose.words.fields/fieldtoc/pagenumberomittinglevelrange/) { get; set; } | Obtient ou définit une plage de niveaux d'entrées de table des matières à partir de laquelle omettre les numéros de page. |
| [PrefixedSequenceIdentifier](../../aspose.words.fields/fieldtoc/prefixedsequenceidentifier/) { get; set; } | Obtient ou définit l'identifiant d'une séquence pour laquelle un préfixe doit être ajouté au numéro de page de l'entrée. |
| [PreserveLineBreaks](../../aspose.words.fields/fieldtoc/preservelinebreaks/) { get; set; } | Obtient ou définit s'il faut conserver les caractères de nouvelle ligne dans les entrées de table. |
| [PreserveTabs](../../aspose.words.fields/fieldtoc/preservetabs/) { get; set; } | Obtient ou définit s'il faut conserver les entrées d'onglet dans les entrées de table. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Obtient ou définit le texte qui se trouve entre le séparateur de champ et la fin du champ. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Récupère le nœud représentant le séparateur de champ. Peut être`nul` . |
| [SequenceSeparator](../../aspose.words.fields/fieldtoc/sequenceseparator/) { get; set; } | Obtient ou définit la séquence de caractères utilisée pour séparer les numéros de séquence et les numéros de page. |
| [Start](../../aspose.words.fields/field/start/) { get; } | Obtient le nœud qui représente le début du champ. |
| [TableOfFiguresLabel](../../aspose.words.fields/fieldtoc/tableoffigureslabel/) { get; set; } | Obtient ou définit le nom de l'identifiant de séquence utilisé lors de la création d'un tableau des figures. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Obtient le type de champ Microsoft Word. |
| [UseParagraphOutlineLevel](../../aspose.words.fields/fieldtoc/useparagraphoutlinelevel/) { get; set; } | Obtient ou définit s'il faut utiliser le niveau de plan de paragraphe appliqué. |

## Méthodes

| Nom | La description |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Renvoie le texte entre le début du champ et le séparateur de champ (ou la fin du champ s'il n'y a pas de séparateur). Le code du champ et le résultat du champ des champs enfants sont inclus. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | Renvoie le texte entre le début du champ et le séparateur de champ (ou la fin du champ s'il n'y a pas de séparateur). |
| [Remove](../../aspose.words.fields/field/remove/)() | Supprime le champ du document. Renvoie un nœud immédiatement après le champ. Si la fin du champ est le dernier child de son nœud parent, renvoie son paragraphe parent. Si le champ est déjà supprimé, renvoie`nul` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Effectue la dissociation du champ. |
| [Update](../../aspose.words.fields/field/update/)() | Effectue la mise à jour du champ. Lève une requête si le champ est déjà en cours de mise à jour. |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | Effectue une mise à jour du champ. L'erreur est générée si le champ est déjà en cours de mise à jour. |
| [UpdatePageNumbers](../../aspose.words.fields/fieldtoc/updatepagenumbers/)() | Met à jour les numéros de page des éléments de cette table des matières. |

## Remarques

Crée une table des matières (qui peut également être une table des figures) en utilisant les entrées spécifiées par les champs TC, leurs niveaux de titre et les styles spécifiés, et insère cette table à cet endroit dans le document.

## Exemples

Montre comment insérer une table des matières et la remplir avec des entrées basées sur des styles de titre.

```csharp
public void FieldToc()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.StartBookmark("MyBookmark");

    // Insérez un champ TOC, qui compilera tous les titres dans une table des matières.
    // Pour chaque titre, ce champ créera une ligne avec le texte dans ce style de titre à gauche,
    // et la page sur laquelle le titre apparaît à droite.
    FieldToc field = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

    // Utilisez la propriété BookmarkName pour répertorier uniquement les titres
    // qui apparaissent dans les limites d'un signet portant le nom « MyBookmark ».
    field.BookmarkName = "MyBookmark";

    // Le texte avec un style de titre intégré, tel que « Titre 1 », qui lui est appliqué sera considéré comme un titre.
    // Nous pouvons nommer des styles supplémentaires à récupérer comme titres par la table des matières dans cette propriété et leurs niveaux de table des matières.
    field.CustomStyles = "Quote; 6; Intense Quote; 7";

    // Par défaut, les niveaux Styles/TOC sont séparés dans la propriété CustomStyles par une virgule,
    // mais nous pouvons définir un délimiteur personnalisé dans cette propriété.
    doc.FieldOptions.CustomTocStyleSeparator = ";";

    // Configurez le champ pour exclure tous les titres dont les niveaux de table des matières sont en dehors de cette plage.
    field.HeadingLevelRange = "1-3";

    // La table des matières n'affichera pas les numéros de page des titres dont les niveaux de table des matières se situent dans cette plage.
    field.PageNumberOmittingLevelRange = "2-5";

     // Définissez une chaîne personnalisée qui séparera chaque titre de son numéro de page.
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

    // Ces deux titres auront les numéros de page omis car ils sont compris dans la plage « 2-5 ».
    InsertNewPageWithHeading(builder, "Fifth entry", "Heading 2");
    InsertNewPageWithHeading(builder, "Sixth entry", "Heading 3");

    // Cette entrée n'apparaît pas car « Titre 4 » est en dehors de la plage « 1-3 » que nous avons définie précédemment.
    InsertNewPageWithHeading(builder, "Seventh entry", "Heading 4");

    builder.EndBookmark("MyBookmark");
    builder.Writeln("Paragraph text.");

    // Cette entrée n'apparaît pas car elle se trouve en dehors du signet spécifié par la table des matières.
    InsertNewPageWithHeading(builder, "Eighth entry", "Heading 1");

    Assert.AreEqual(" TOC  \\b MyBookmark \\t \"Quote; 6; Intense Quote; 7\" \\o 1-3 \\n 2-5 \\p - \\h \\x \\w", field.GetFieldCode());

    field.UpdatePageNumbers();
    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.TOC.docx");
}

/// <summary>
/// Démarrez une nouvelle page et insérez un paragraphe d'un style spécifié.
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

Montre comment remplir un champ TOC avec des entrées à l'aide de champs SEQ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Un champ TOC peut créer une entrée dans sa table des matières pour chaque champ SEQ trouvé dans le document.
// Chaque entrée contient le paragraphe qui inclut le champ SEQ et le numéro de page sur lequel le champ apparaît.
FieldToc fieldToc = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

// Les champs SEQ affichent un nombre qui augmente à chaque champ SEQ.
// Ces champs conservent également des comptes distincts pour chaque séquence nommée unique
// identifié par la propriété « SequenceIdentifier » du champ SEQ.
// Utilisez la propriété « TableOfFiguresLabel » pour nommer une séquence principale pour la table des matières.
// Désormais, cette table des matières créera uniquement des entrées à partir de champs SEQ avec leur « SequenceIdentifier » défini sur « MySequence ».
fieldToc.TableOfFiguresLabel = "MySequence";

// Nous pouvons nommer une autre séquence de champs SEQ dans la propriété « PrefixedSequenceIdentifier ».
 // Les champs SEQ de cette séquence de préfixes ne créeront pas d'entrées TOC.
// Chaque entrée de table des matières créée à partir d'un champ SEQ de séquence principale affichera désormais également le nombre de
// la séquence de préfixe est actuellement activée dans le champ SEQ de la séquence principale qui a effectué l'entrée.
fieldToc.PrefixedSequenceIdentifier = "PrefixSequence";

// Chaque entrée de la table des matières affichera le nombre de séquences de préfixes immédiatement à gauche
// du numéro de page sur lequel le champ SEQ de la séquence principale apparaît.
// Nous pouvons spécifier un séparateur personnalisé qui apparaîtra entre ces deux nombres.
fieldToc.SequenceSeparator = ">";

Assert.AreEqual(" TOC  \\c MySequence \\s PrefixSequence \\d >", fieldToc.GetFieldCode());

builder.InsertBreak(BreakType.PageBreak);

// Il existe deux manières d'utiliser les champs SEQ pour remplir cette table des matières.
// 1 - Insertion d'un champ SEQ appartenant à la séquence de préfixe de la table des matières :
// Ce champ incrémentera le nombre de séquences SEQ pour la « PrefixSequence » de 1.
// Étant donné que ce champ n'appartient pas à la séquence principale identifiée
// par la propriété "TableOfFiguresLabel" de la table des matières, elle n'apparaîtra pas comme une entrée.
FieldSeq fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "PrefixSequence";
builder.InsertParagraph();

Assert.AreEqual(" SEQ  PrefixSequence", fieldSeq.GetFieldCode());

// 2 - Insertion d'un champ SEQ appartenant à la séquence principale de la table des matières :
// Ce champ SEQ créera une entrée dans la table des matières.
// L'entrée TOC contiendra le paragraphe dans lequel se trouve le champ SEQ et le numéro de la page sur laquelle il apparaît.
// Cette entrée affichera également le nombre actuel de séquences de préfixes,
// séparé du numéro de page par la valeur de la propriété SequenceSeparator de la table des matières.
// Le nombre de « PrefixSequence » est à 1, ce champ SEQ de séquence principale est à la page 2,
// et le séparateur est « > », donc l'entrée affichera « 1>2 ».
builder.Write("First TOC entry, MySequence #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";

Assert.AreEqual(" SEQ  MySequence", fieldSeq.GetFieldCode());

// Insérez une page, avancez la séquence de préfixes de 2 et insérez un champ SEQ pour créer une entrée TOC par la suite.
// La séquence de préfixe est maintenant à 2, et le champ SEQ de la séquence principale est à la page 3,
// donc l'entrée TOC affichera « 2 > 3 » à son nombre de pages.
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
