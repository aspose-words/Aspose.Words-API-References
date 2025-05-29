---
title: FieldOptions Class
linktitle: FieldOptions
articleTitle: FieldOptions
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.Fields.FieldOptions pour optimiser la gestion des champs dans les documents, améliorant ainsi votre flux de travail et l'efficacité de la gestion des documents.
type: docs
weight: 2660
url: /fr/net/aspose.words.fields/fieldoptions/
---
## FieldOptions class

Représente les options permettant de contrôler la gestion des champs dans un document.

Pour en savoir plus, visitez le[Travailler avec les champs](https://docs.aspose.com/words/net/working-with-fields/) article de documentation.

```csharp
public sealed class FieldOptions
```

## Propriétés

| Nom | La description |
| --- | --- |
| [BarcodeGenerator](../../aspose.words.fields/fieldoptions/barcodegenerator/) { get; set; } | Obtient ou définit un générateur de codes-barres personnalisé. |
| [BibliographyStylesProvider](../../aspose.words.fields/fieldoptions/bibliographystylesprovider/) { get; set; } | Obtient ou définit un fournisseur qui renvoie un style de bibliographie pour le[`FieldBibliography`](../fieldbibliography/) et[`FieldCitation`](../fieldcitation/) champs. |
| [BuiltInTemplatesPaths](../../aspose.words.fields/fieldoptions/builtintemplatespaths/) { get; set; } | Obtient ou définit les chemins des modèles intégrés de MS Word. |
| [ComparisonExpressionEvaluator](../../aspose.words.fields/fieldoptions/comparisonexpressionevaluator/) { get; set; } | Obtient ou définit l'évaluateur des expressions de comparaison de champs. |
| [CurrentUser](../../aspose.words.fields/fieldoptions/currentuser/) { get; set; } | Obtient ou définit les informations de l'utilisateur actuel. |
| [CustomTocStyleSeparator](../../aspose.words.fields/fieldoptions/customtocstyleseparator/) { get; set; } | Obtient ou définit un séparateur de style personnalisé pour le commutateur \t dans[`FieldToc`](../fieldtoc/) champ. |
| [DefaultDocumentAuthor](../../aspose.words.fields/fieldoptions/defaultdocumentauthor/) { get; set; } | Récupère ou définit le nom de l'auteur par défaut du document. Si le nom de l'auteur est déjà spécifié dans les propriétés intégrées du document, cette option n'est pas prise en compte. |
| [FieldDatabaseProvider](../../aspose.words.fields/fieldoptions/fielddatabaseprovider/) { get; set; } | Obtient ou définit un fournisseur qui renvoie un résultat de requête pour le[`FieldDatabase`](../fielddatabase/) champ. |
| [FieldIndexFormat](../../aspose.words.fields/fieldoptions/fieldindexformat/) { get; set; } | Obtient ou définit un[`FieldIndexFormat`](./fieldindexformat/) qui représente le formatage pour le[`FieldIndex`](../fieldindex/) champs dans le document. |
| [FieldUpdateCultureProvider](../../aspose.words.fields/fieldoptions/fieldupdatecultureprovider/) { get; set; } | Obtient ou définit un fournisseur qui renvoie un objet de culture spécifique pour chaque champ particulier. |
| [FieldUpdateCultureSource](../../aspose.words.fields/fieldoptions/fieldupdateculturesource/) { get; set; } | Spécifie la culture à utiliser pour formater le résultat du champ. |
| [FieldUpdatingCallback](../../aspose.words.fields/fieldoptions/fieldupdatingcallback/) { get; set; } | Obtient ou définit[`IFieldUpdatingCallback`](../ifieldupdatingcallback/) implémentation |
| [FieldUpdatingProgressCallback](../../aspose.words.fields/fieldoptions/fieldupdatingprogresscallback/) { get; set; } | Obtient ou définit[`IFieldUpdatingProgressCallback`](../ifieldupdatingprogresscallback/) implémentation. |
| [FileName](../../aspose.words.fields/fieldoptions/filename/) { get; set; } | Obtient ou définit le nom de fichier du document. |
| [IsBidiTextSupportedOnUpdate](../../aspose.words.fields/fieldoptions/isbiditextsupportedonupdate/) { get; set; } | Obtient ou définit la valeur indiquant si le texte bidirectionnel est entièrement pris en charge lors de la mise à jour du champ ou non. |
| [LegacyNumberFormat](../../aspose.words.fields/fieldoptions/legacynumberformat/) { get; set; } | Obtient ou définit la valeur indiquant si le format numérique hérité (antérieur à AW 13.10) pour les champs est activé ou non. |
| [PreProcessCulture](../../aspose.words.fields/fieldoptions/preprocessculture/) { get; set; } | Obtient ou définit la culture pour prétraiter les valeurs de champ. |
| [ResultFormatter](../../aspose.words.fields/fieldoptions/resultformatter/) { get; set; } | Permet de contrôler la façon dont le résultat du champ est formaté. |
| [TemplateName](../../aspose.words.fields/fieldoptions/templatename/) { get; set; } | Obtient ou définit le nom de fichier du modèle utilisé par le document. |
| [ToaCategories](../../aspose.words.fields/fieldoptions/toacategories/) { get; set; } | Obtient ou définit le tableau des catégories d'autorités. |
| [UseInvariantCultureNumberFormat](../../aspose.words.fields/fieldoptions/useinvariantculturenumberformat/) { get; set; } | Obtient ou définit la valeur indiquant que le format du nombre est analysé à l'aide d'une culture invariante ou non |
| [UserPromptRespondent](../../aspose.words.fields/fieldoptions/userpromptrespondent/) { get; set; } | Obtient ou définit le répondant aux invites utilisateur lors de la mise à jour du champ. |

## Exemples

Montre comment spécifier la source de la culture utilisée pour le formatage de la date lors d'une mise à jour de champ ou d'un publipostage.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insérer deux champs de fusion avec les paramètres régionaux allemands.
builder.Font.LocaleId = new CultureInfo("de-DE").LCID;
builder.InsertField("MERGEFIELD Date1 \\@ \"dddd, d MMMM yyyy\"");
builder.Write(" - ");
builder.InsertField("MERGEFIELD Date2 \\@ \"dddd, d MMMM yyyy\"");

// Définissez la culture actuelle sur l'anglais américain après avoir conservé sa valeur d'origine dans une variable.
CultureInfo currentCulture = Thread.CurrentThread.CurrentCulture;
Thread.CurrentThread.CurrentCulture = new CultureInfo("en-US");

// Cette fusion utilisera la culture du thread actuel pour formater la date, en anglais américain.
doc.MailMerge.Execute(new[] { "Date1" }, new object[] { new DateTime(2020, 1, 01) });

// Configurez la fusion suivante pour que sa valeur de culture soit issue du code du champ. La valeur de cette culture sera allemande.
doc.FieldOptions.FieldUpdateCultureSource = FieldUpdateCultureSource.FieldCode;
doc.MailMerge.Execute(new[] { "Date2" }, new object[] { new DateTime(2020, 1, 01) });

// Le premier résultat de fusion contient une date formatée en anglais, tandis que le second est en allemand.
Assert.AreEqual("Wednesday, 1 January 2020 - Mittwoch, 1 Januar 2020", doc.Range.Text.Trim());

// Restaurer la culture d'origine du thread.
Thread.CurrentThread.CurrentCulture = currentCulture;
```

### Voir également

* espace de noms [Aspose.Words.Fields](../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../)
