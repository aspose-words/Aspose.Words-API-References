---
title: FieldSeq Class
linktitle: FieldSeq
articleTitle: FieldSeq
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.Fields.FieldSeq pour une implémentation fluide des champs SEQ. Optimisez l'automatisation de vos documents grâce à des fonctionnalités puissantes et flexibles.
type: docs
weight: 2800
url: /fr/net/aspose.words.fields/fieldseq/
---
## FieldSeq class

Implémente le champ SEQ.

Pour en savoir plus, visitez le[Travailler avec les champs](https://docs.aspose.com/words/net/working-with-fields/) article de documentation.

```csharp
public class FieldSeq : Field
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [FieldSeq](fieldseq/)() | Default_Constructor |

## Propriétés

| Nom | La description |
| --- | --- |
| [BookmarkName](../../aspose.words.fields/fieldseq/bookmarkname/) { get; set; } | Obtient ou définit un nom de signet qui fait référence à un élément ailleurs dans le document plutôt qu'à l'emplacement actuel. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Obtient le texte qui représente le résultat du champ affiché. |
| [End](../../aspose.words.fields/field/end/) { get; } | Obtient le nœud qui représente la fin du champ. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Obtient un[`FieldFormat`](../fieldformat/)objet qui fournit un accès typé au formatage du champ. |
| [InsertNextNumber](../../aspose.words.fields/fieldseq/insertnextnumber/) { get; set; } | Obtient ou définit s'il faut insérer le numéro de séquence suivant pour l'élément spécifié. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Obtient ou définit si le résultat actuel du champ n'est plus correct (obsolète) en raison d'autres modifications apportées au document. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Obtient ou définit si le champ est verrouillé (ne doit pas recalculer son résultat). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Obtient ou définit le LCID du champ. |
| [ResetHeadingLevel](../../aspose.words.fields/fieldseq/resetheadinglevel/) { get; set; } | Obtient ou définit un nombre entier représentant un niveau de titre sur lequel réinitialiser le numéro de séquence. Renvoie -1 si le numéro est absent. |
| [ResetNumber](../../aspose.words.fields/fieldseq/resetnumber/) { get; set; } | Obtient ou définit un nombre entier pour réinitialiser le numéro de séquence. Renvoie -1 si le numéro est absent. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Obtient ou définit le texte qui se trouve entre le séparateur de champ et la fin du champ. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Récupère le nœud représentant le séparateur de champ. Peut être`nul` . |
| [SequenceIdentifier](../../aspose.words.fields/fieldseq/sequenceidentifier/) { get; set; } | Obtient ou définit le nom attribué à la série d'éléments à numéroter. |
| [Start](../../aspose.words.fields/field/start/) { get; } | Obtient le nœud qui représente le début du champ. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Obtient le type de champ Microsoft Word. |

## Méthodes

| Nom | La description |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Renvoie le texte entre le début du champ et le séparateur de champ (ou la fin du champ s'il n'y a pas de séparateur). Le code du champ et le résultat du champ des champs enfants sont inclus. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | Renvoie le texte entre le début du champ et le séparateur de champ (ou la fin du champ s'il n'y a pas de séparateur). |
| [Remove](../../aspose.words.fields/field/remove/)() | Supprime le champ du document. Renvoie un nœud immédiatement après le champ. Si la fin du champ est le dernier child de son nœud parent, renvoie son paragraphe parent. Si le champ est déjà supprimé, renvoie`nul` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Effectue la dissociation du champ. |
| [Update](../../aspose.words.fields/field/update/)() | Effectue la mise à jour du champ. Lève une requête si le champ est déjà en cours de mise à jour. |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | Effectue une mise à jour du champ. L'erreur est générée si le champ est déjà en cours de mise à jour. |

## Remarques

Numérote séquentiellement les chapitres, les tableaux, les figures et d'autres listes d'éléments définies par l'utilisateur dans un document.

## Exemples

Les émissions créent une numérotation à l'aide de champs SEQ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Les champs SEQ affichent un nombre qui augmente à chaque champ SEQ.
// Ces champs conservent également des comptes distincts pour chaque séquence nommée unique
// identifié par la propriété « SequenceIdentifier » du champ SEQ.
// Insérer un champ SEQ qui affichera la valeur de comptage actuelle de « MySequence »,
// après avoir utilisé la propriété "ResetNumber" pour la définir à 100.
builder.Write("#");
FieldSeq fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
fieldSeq.ResetNumber = "100";
fieldSeq.Update();

Assert.AreEqual(" SEQ  MySequence \\r 100", fieldSeq.GetFieldCode());
Assert.AreEqual("100", fieldSeq.Result);

// Affichez le numéro suivant dans cette séquence avec un autre champ SEQ.
builder.Write(", #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
fieldSeq.Update();

Assert.AreEqual("101", fieldSeq.Result);

// Insérer un titre de niveau 1.
builder.InsertBreak(BreakType.ParagraphBreak);
builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("This level 1 heading will reset MySequence to 1");
builder.ParagraphFormat.Style = doc.Styles["Normal"];

// Insérez un autre champ SEQ de la même séquence et configurez-le pour réinitialiser le compte à chaque en-tête avec 1.
builder.Write("\n#");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
fieldSeq.ResetHeadingLevel = "1";
fieldSeq.Update();

// Le titre ci-dessus est un titre de niveau 1, donc le nombre de cette séquence est réinitialisé à 1.
Assert.AreEqual(" SEQ  MySequence \\s 1", fieldSeq.GetFieldCode());
Assert.AreEqual("1", fieldSeq.Result);

// Passer au numéro suivant de cette séquence.
builder.Write(", #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
fieldSeq.InsertNextNumber = true;
fieldSeq.Update();

Assert.AreEqual(" SEQ  MySequence \\n", fieldSeq.GetFieldCode());
Assert.AreEqual("2", fieldSeq.Result);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.SEQ.ResetNumbering.docx");
```

Montre comment combiner les champs de table des matières et de séquence.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Un champ TOC peut créer une entrée dans sa table des matières pour chaque champ SEQ trouvé dans le document.
// Chaque entrée contient le paragraphe qui contient le champ SEQ,
// et le numéro de la page sur laquelle le champ apparaît.
FieldToc fieldToc = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

// Configurez ce champ TOC pour avoir une propriété SequenceIdentifier avec une valeur de « MySequence ».
fieldToc.TableOfFiguresLabel = "MySequence";

// Configurez ce champ TOC pour récupérer uniquement les champs SEQ qui se trouvent dans les limites d'un signet
// nommé "TOCBookmark".
fieldToc.BookmarkName = "TOCBookmark";
builder.InsertBreak(BreakType.PageBreak);

Assert.AreEqual(" TOC  \\c MySequence \\b TOCBookmark", fieldToc.GetFieldCode());

// Les champs SEQ affichent un nombre qui augmente à chaque champ SEQ.
// Ces champs conservent également des comptes distincts pour chaque séquence nommée unique
// identifié par la propriété « SequenceIdentifier » du champ SEQ.
// Insérer un champ SEQ qui a un identifiant de séquence qui correspond à la table des matières
// Propriété TableOfFiguresLabel. Ce champ ne crée pas d'entrée dans la table des matières, car il est extérieur.
// les limites du signet désignées par « BookmarkName ».
builder.Write("MySequence #");
FieldSeq fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
builder.Writeln(", will not show up in the TOC because it is outside of the bookmark.");

builder.StartBookmark("TOCBookmark");

// La séquence de ce champ SEQ correspond à la propriété « TableOfFiguresLabel » de la table des matières et se situe dans les limites du signet.
// Le paragraphe qui contient ce champ apparaîtra dans la table des matières sous forme d'entrée.
builder.Write("MySequence #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
builder.Writeln(", will show up in the TOC next to the entry for the above caption.");

// La séquence de ce champ SEQ ne correspond pas à la propriété « TableOfFiguresLabel » de la table des matières,
// et se trouve dans les limites du signet. Son paragraphe n'apparaîtra pas dans la table des matières comme une entrée.
builder.Write("MySequence #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "OtherSequence";
builder.Writeln(", will not show up in the TOC because it's from a different sequence identifier.");

// La séquence de ce champ SEQ correspond à la propriété « TableOfFiguresLabel » de la table des matières et se situe dans les limites du signet.
// Ce champ fait également référence à un autre signet. Le contenu de ce signet apparaîtra dans la table des matières de ce champ SEQ.
// Le champ SEQ lui-même n'affichera pas le contenu de ce signet.
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
fieldSeq.BookmarkName = "SEQBookmark";
Assert.AreEqual(" SEQ  MySequence SEQBookmark", fieldSeq.GetFieldCode());

// Créez un signet avec un contenu qui apparaîtra dans l'entrée TOC en raison du champ SEQ ci-dessus qui y fait référence.
builder.InsertBreak(BreakType.PageBreak);
builder.StartBookmark("SEQBookmark");
builder.Write("MySequence #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
builder.Writeln(", text from inside SEQBookmark.");
builder.EndBookmark("SEQBookmark");

builder.EndBookmark("TOCBookmark");

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.SEQ.Bookmark.docx");
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
