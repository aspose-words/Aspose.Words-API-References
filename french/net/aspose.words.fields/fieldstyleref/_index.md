---
title: Class FieldStyleRef
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.Fields.FieldStyleRef classe. Implémente le champ STYLEREF.
type: docs
weight: 2290
url: /fr/net/aspose.words.fields/fieldstyleref/
---
## FieldStyleRef class

Implémente le champ STYLEREF.

```csharp
public class FieldStyleRef : Field
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [FieldStyleRef](fieldstyleref/)() | Default_Constructor |

## Propriétés

| Nom | La description |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Obtient le texte qui représente le résultat du champ affiché. |
| [End](../../aspose.words.fields/field/end/) { get; } | Obtient le nœud qui représente la fin du champ. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Obtient un[`FieldFormat`](../fieldformat/) objet qui fournit un accès typé au formatage du champ. |
| [InsertParagraphNumber](../../aspose.words.fields/fieldstyleref/insertparagraphnumber/) { get; set; } | Obtient ou définit s'il faut insérer le numéro de paragraphe du paragraphe référencé exactement tel qu'il apparaît dans le document. |
| [InsertParagraphNumberInFullContext](../../aspose.words.fields/fieldstyleref/insertparagraphnumberinfullcontext/) { get; set; } | Obtient ou définit s'il faut insérer le numéro de paragraphe du paragraphe référencé dans son contexte complet. |
| [InsertParagraphNumberInRelativeContext](../../aspose.words.fields/fieldstyleref/insertparagraphnumberinrelativecontext/) { get; set; } | Obtient ou définit s'il faut insérer le numéro de paragraphe du paragraphe référencé dans un contexte relatif. |
| [InsertRelativePosition](../../aspose.words.fields/fieldstyleref/insertrelativeposition/) { get; set; } | Obtient ou définit s'il faut insérer la position relative du paragraphe référencé. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Obtient ou définit si le résultat actuel du champ n'est plus correct (périmé) en raison d'autres modifications apportées au document. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Obtient ou définit si le champ est verrouillé (ne doit pas recalculer son résultat). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Obtient ou définit le LCID du champ. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Obtient ou définit le texte qui se trouve entre le séparateur de champ et la fin du champ. |
| [SearchFromBottom](../../aspose.words.fields/fieldstyleref/searchfrombottom/) { get; set; } | Obtient ou définit s'il faut rechercher à partir du bas de la page actuelle, plutôt qu'à partir du haut. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Obtient le nœud qui représente le séparateur de champs. Peut être null. |
| [Start](../../aspose.words.fields/field/start/) { get; } | Obtient le nœud qui représente le début du champ. |
| [StyleName](../../aspose.words.fields/fieldstyleref/stylename/) { get; set; } | Obtient ou définit le nom du style par lequel le texte à rechercher est formaté. |
| [SuppressNonDelimiters](../../aspose.words.fields/fieldstyleref/suppressnondelimiters/) { get; set; } | Obtient ou définit s'il faut supprimer les caractères non délimiteurs. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Obtient le type de champ Microsoft Word. |

## Méthodes

| Nom | La description |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Renvoie le texte entre le début du champ et le séparateur de champ (ou la fin du champ s'il n'y a pas de séparateur). Le code de champ et le résultat du champ des champs enfants sont inclus. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(bool) | Renvoie le texte entre le début du champ et le séparateur de champ (ou la fin du champ s'il n'y a pas de séparateur). |
| [Remove](../../aspose.words.fields/field/remove/)() | Supprime le champ du document. Renvoie un nœud juste après le champ. Si la fin du champ est le dernier enfant de son nœud parent, renvoie son paragraphe parent. Si le champ est déjà supprimé, renvoie **nul** . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Effectue la dissociation du champ. |
| [Update](../../aspose.words.fields/field/update/)() | Effectue la mise à jour du champ. Lance si le champ est déjà mis à jour. |
| [Update](../../aspose.words.fields/field/update/)(bool) | Effectue une mise à jour du champ. Lance si le champ est déjà mis à jour. |

### Remarques

Le STYLEREF est utilisé pour référencer un fragment de texte dans le document qui est formaté avec le style spécifié.

### Exemples

Montre comment utiliser les champs STYLEREF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Crée une liste basée sur un modèle de liste Microsoft Word.
Aspose.Words.Lists.List list = doc.Lists.Add(Aspose.Words.Lists.ListTemplate.NumberDefault);

// Cette liste générée affichera "1.a )".
 // L'espace avant le crochet est un caractère non délimiteur, que nous pouvons supprimer.
list.ListLevels[0].NumberFormat = "\x0000.";
list.ListLevels[1].NumberFormat = "\x0001 )";

// Ajoute du texte et applique des styles de paragraphe auxquels les champs STYLEREF feront référence.
builder.ListFormat.List = list;
builder.ListFormat.ListIndent();
builder.ParagraphFormat.Style = doc.Styles["List Paragraph"];
builder.Writeln("Item 1");
builder.ParagraphFormat.Style = doc.Styles["Quote"];
builder.Writeln("Item 2");
builder.ParagraphFormat.Style = doc.Styles["List Paragraph"];
builder.Writeln("Item 3");
builder.ListFormat.RemoveNumbers();
builder.ParagraphFormat.Style = doc.Styles["Normal"];

// Place un champ STYLEREF dans l'en-tête et affiche le premier texte de style "List Paragraph" dans le document.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
FieldStyleRef field = (FieldStyleRef)builder.InsertField(FieldType.FieldStyleRef, true);
field.StyleName = "List Paragraph";

// Place un champ STYLEREF dans le pied de page et affiche le dernier texte.
builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
field = (FieldStyleRef)builder.InsertField(FieldType.FieldStyleRef, true);
field.StyleName = "List Paragraph";
field.SearchFromBottom = true;

builder.MoveToDocumentEnd();

// Nous pouvons également utiliser les champs STYLEREF pour référencer les numéros de liste des listes.
builder.Write("\nParagraph number: ");
field = (FieldStyleRef)builder.InsertField(FieldType.FieldStyleRef, true);
field.StyleName = "Quote";
field.InsertParagraphNumber = true;

builder.Write("\nParagraph number, relative context: ");
field = (FieldStyleRef)builder.InsertField(FieldType.FieldStyleRef, true);
field.StyleName = "Quote";
field.InsertParagraphNumberInRelativeContext = true;

builder.Write("\nParagraph number, full context: ");
field = (FieldStyleRef)builder.InsertField(FieldType.FieldStyleRef, true);
field.StyleName = "Quote";
field.InsertParagraphNumberInFullContext = true;

builder.Write("\nParagraph number, full context, non-delimiter chars suppressed: ");
field = (FieldStyleRef)builder.InsertField(FieldType.FieldStyleRef, true);
field.StyleName = "Quote";
field.InsertParagraphNumberInFullContext = true;
field.SuppressNonDelimiters = true;

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.STYLEREF.docx");
```

### Voir également

* class [Field](../field/)
* espace de noms [Aspose.Words.Fields](../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../)


