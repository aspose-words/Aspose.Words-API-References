---
title: FieldOptions Class
linktitle: FieldOptions
articleTitle: FieldOptions
second_title: Aspose.Words pour .NET
description: Aspose.Words.Fields.FieldOptions classe. Représente les options permettant de contrôler la gestion des champs dans un document en C#.
type: docs
weight: 2250
url: /fr/net/aspose.words.fields/fieldoptions/
---
## FieldOptions class

Représente les options permettant de contrôler la gestion des champs dans un document.

Pour en savoir plus, visitez le[Travailler avec des champs](https://docs.aspose.com/words/net/working-with-fields/) article documentaire.

```csharp
public sealed class FieldOptions
```

## Propriétés

| Nom | La description |
| --- | --- |
| [BarcodeGenerator](../../aspose.words.fields/fieldoptions/barcodegenerator/) { get; set; } | Obtient ou définit un générateur de codes-barres personnalisé. |
| [BibliographyStylesProvider](../../aspose.words.fields/fieldoptions/bibliographystylesprovider/) { get; set; } | Obtient ou définit un fournisseur qui renvoie un style de bibliographie pour le[`FieldBibliography`](../fieldbibliography/) et[`FieldCitation`](../fieldcitation/) champs. |
| [BuiltInTemplatesPaths](../../aspose.words.fields/fieldoptions/builtintemplatespaths/) { get; set; } | Obtient ou définit les chemins des modèles intégrés MS Word. |
| [ComparisonExpressionEvaluator](../../aspose.words.fields/fieldoptions/comparisonexpressionevaluator/) { get; set; } | Obtient ou définit l'évaluateur des expressions de comparaison de champs. |
| [CurrentUser](../../aspose.words.fields/fieldoptions/currentuser/) { get; set; } | Obtient ou définit les informations utilisateur actuelles. |
| [CustomTocStyleSeparator](../../aspose.words.fields/fieldoptions/customtocstyleseparator/) { get; set; } | Obtient ou définit un séparateur de style personnalisé pour le commutateur \t dans[`FieldToc`](../fieldtoc/) champ. |
| [DefaultDocumentAuthor](../../aspose.words.fields/fieldoptions/defaultdocumentauthor/) { get; set; } | Obtient ou définit le nom de l'auteur du document par défaut. Si le nom de l'auteur est déjà spécifié dans les propriétés intégrées du document, cette option n'est pas prise en compte. |
| [FieldDatabaseProvider](../../aspose.words.fields/fieldoptions/fielddatabaseprovider/) { get; set; } | Obtient ou définit un fournisseur qui renvoie un résultat de requête pour le[`FieldDatabase`](../fielddatabase/) champ. |
| [FieldIndexFormat](../../aspose.words.fields/fieldoptions/fieldindexformat/) { get; set; } | Obtient ou définit un[`FieldIndexFormat`](./fieldindexformat/) qui représente le formatage du[`FieldIndex`](../fieldindex/) champs dans le document. |
| [FieldUpdateCultureProvider](../../aspose.words.fields/fieldoptions/fieldupdatecultureprovider/) { get; set; } | Obtient ou définit un fournisseur qui renvoie un objet de culture spécifique à chaque champ particulier. |
| [FieldUpdateCultureSource](../../aspose.words.fields/fieldoptions/fieldupdateculturesource/) { get; set; } | Spécifie la culture à utiliser pour formater le résultat du champ. |
| [FieldUpdatingCallback](../../aspose.words.fields/fieldoptions/fieldupdatingcallback/) { get; set; } | Obtient ou définit[`IFieldUpdatingCallback`](../ifieldupdatingcallback/) mise en œuvre |
| [FieldUpdatingProgressCallback](../../aspose.words.fields/fieldoptions/fieldupdatingprogresscallback/) { get; set; } | Obtient ou définit[`IFieldUpdatingProgressCallback`](../ifieldupdatingprogresscallback/) mise en œuvre. |
| [FileName](../../aspose.words.fields/fieldoptions/filename/) { get; set; } | Obtient ou définit le nom de fichier du document. |
| [IsBidiTextSupportedOnUpdate](../../aspose.words.fields/fieldoptions/isbiditextsupportedonupdate/) { get; set; } | Obtient ou définit la valeur indiquant si le texte bidirectionnel est entièrement pris en charge lors de la mise à jour du champ ou non. |
| [LegacyNumberFormat](../../aspose.words.fields/fieldoptions/legacynumberformat/) { get; set; } | Obtient ou définit la valeur indiquant si le format numérique existant (antérieur à AW 13.10) pour les champs est activé ou non. |
| [PreProcessCulture](../../aspose.words.fields/fieldoptions/preprocessculture/) { get; set; } | Obtient ou définit la culture pour prétraiter les valeurs des champs. |
| [ResultFormatter](../../aspose.words.fields/fieldoptions/resultformatter/) { get; set; } | Permet de contrôler la façon dont le résultat du champ est formaté. |
| [TemplateName](../../aspose.words.fields/fieldoptions/templatename/) { get; set; } | Obtient ou définit le nom de fichier du modèle utilisé par le document. |
| [ToaCategories](../../aspose.words.fields/fieldoptions/toacategories/) { get; set; } | Obtient ou définit la table des catégories d'autorités. |
| [UseInvariantCultureNumberFormat](../../aspose.words.fields/fieldoptions/useinvariantculturenumberformat/) { get; set; } | Obtient ou définit la valeur indiquant que le format numérique est analysé à l'aide d'une culture invariante ou not |
| [UserPromptRespondent](../../aspose.words.fields/fieldoptions/userpromptrespondent/) { get; set; } | Obtient ou définit le répondant sur les invites de l'utilisateur lors de la mise à jour du champ. |

## Exemples

Montre comment spécifier la source de la culture utilisée pour le formatage de la date lors d'une mise à jour de champ ou d'un publipostage.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insère deux champs de fusion avec les paramètres régionaux allemands.
builder.Font.LocaleId = new CultureInfo("de-DE").LCID;
builder.InsertField("MERGEFIELD Date1 \\@ \"dddd, d MMMM yyyy\"");
builder.Write(" - ");
builder.InsertField("MERGEFIELD Date2 \\@ \"dddd, d MMMM yyyy\"");

// Définit la culture actuelle sur l'anglais américain après avoir conservé sa valeur d'origine dans une variable.
CultureInfo currentCulture = Thread.CurrentThread.CurrentCulture;
Thread.CurrentThread.CurrentCulture = new CultureInfo("en-US");

// Cette fusion utilisera la culture du fil de discussion actuel pour formater la date, en anglais américain.
doc.MailMerge.Execute(new[] { "Date1" }, new object[] { new DateTime(2020, 1, 01) });

// Configurez la prochaine fusion pour obtenir sa valeur de culture à partir du code de champ. La valeur de cette culture sera allemande.
doc.FieldOptions.FieldUpdateCultureSource = FieldUpdateCultureSource.FieldCode;
doc.MailMerge.Execute(new[] { "Date2" }, new object[] { new DateTime(2020, 1, 01) });

// Le premier résultat de fusion contient une date formatée en anglais, tandis que la seconde est en allemand.
Assert.AreEqual("Wednesday, 1 January 2020 - Mittwoch, 1 Januar 2020", doc.Range.Text.Trim());

// Restaurer la culture d'origine du fil.
Thread.CurrentThread.CurrentCulture = currentCulture;
```

### Voir également

* espace de noms [Aspose.Words.Fields](../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../)
