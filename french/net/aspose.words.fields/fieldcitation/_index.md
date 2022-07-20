---
title: FieldCitation
second_title: Référence de l'API Aspose.Words pour .NET
description: Implémente le champ CITATION.
type: docs
weight: 1530
url: /fr/net/aspose.words.fields/fieldcitation/
---
## FieldCitation class

Implémente le champ CITATION.

```csharp
public class FieldCitation : Field
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [FieldCitation](fieldcitation)() | Default_Constructor |

## Propriétés

| Nom | La description |
| --- | --- |
| [AnotherSourceTag](../../aspose.words.fields/fieldcitation/anothersourcetag) { get; set; } | Obtient ou définit une valeur qui calcule le **Étiquette** valeur de l'élément d'une autre source à inclure dans la citation. |
| [DisplayResult](../../aspose.words.fields/field/displayresult) { get; } | Obtient le texte qui représente le résultat du champ affiché. |
| [End](../../aspose.words.fields/field/end) { get; } | Obtient le nœud qui représente la fin du champ. |
| [Format](../../aspose.words.fields/field/format) { get; } | Obtient un[`FieldFormat`](../fieldformat) objet qui fournit un accès typé au formatage du champ. |
| [FormatLanguageId](../../aspose.words.fields/fieldcitation/formatlanguageid) { get; set; } | Obtient ou définit l'ID de langue utilisé conjointement avec le style bibliographique spécifié pour formater la citation dans le document. |
| [IsDirty](../../aspose.words.fields/field/isdirty) { get; set; } | Obtient ou définit si le résultat actuel du champ n'est plus correct (périmé) en raison d'autres modifications apportées au document. |
| [IsLocked](../../aspose.words.fields/field/islocked) { get; set; } | Obtient ou définit si le champ est verrouillé (ne doit pas recalculer son résultat). |
| [LocaleId](../../aspose.words.fields/field/localeid) { get; set; } | Obtient ou définit le LCID du champ. |
| [PageNumber](../../aspose.words.fields/fieldcitation/pagenumber) { get; set; } | Obtient ou définit un numéro de page associé à la citation. |
| [Prefix](../../aspose.words.fields/fieldcitation/prefix) { get; set; } | Obtient ou définit un préfixe ajouté à la citation. |
| [Result](../../aspose.words.fields/field/result) { get; set; } | Obtient ou définit le texte qui se trouve entre le séparateur de champ et la fin du champ. |
| [Separator](../../aspose.words.fields/field/separator) { get; } | Obtient le nœud qui représente le séparateur de champs. Peut être null. |
| [SourceTag](../../aspose.words.fields/fieldcitation/sourcetag) { get; set; } | Obtient ou définit une valeur qui calcule le **Étiquette**valeur de l'élément de la source à insérer. |
| [Start](../../aspose.words.fields/field/start) { get; } | Obtient le nœud qui représente le début du champ. |
| [Suffix](../../aspose.words.fields/fieldcitation/suffix) { get; set; } | Obtient ou définit un suffixe qui est ajouté à la citation. |
| [SuppressAuthor](../../aspose.words.fields/fieldcitation/suppressauthor) { get; set; } | Obtient ou définit si les informations sur l'auteur sont supprimées de la citation. |
| [SuppressTitle](../../aspose.words.fields/fieldcitation/suppresstitle) { get; set; } | Obtient ou définit si les informations sur le titre sont supprimées de la citation. |
| [SuppressYear](../../aspose.words.fields/fieldcitation/suppressyear) { get; set; } | Obtient ou définit si les informations sur l'année sont supprimées de la citation. |
| virtual [Type](../../aspose.words.fields/field/type) { get; } | Obtient le type de champ Microsoft Word. |
| [VolumeNumber](../../aspose.words.fields/fieldcitation/volumenumber) { get; set; } | Obtient ou définit un numéro de volume associé à la citation. |

## Méthodes

| Nom | La description |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)() | Renvoie le texte entre le début du champ et le séparateur de champ (ou la fin du champ s'il n'y a pas de séparateur). Le code de champ et le résultat du champ des champs enfants sont inclus. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)(bool) | Renvoie le texte entre le début du champ et le séparateur de champ (ou la fin du champ s'il n'y a pas de séparateur). |
| [Remove](../../aspose.words.fields/field/remove)() | Supprime le champ du document. Renvoie un nœud juste après le champ. Si la fin du champ est le dernier enfant de son nœud parent, renvoie son paragraphe parent. Si le champ est déjà supprimé, renvoie **nul** . |
| [Unlink](../../aspose.words.fields/field/unlink)() | Effectue la dissociation du champ. |
| [Update](../../aspose.words.fields/field/update)() | Effectue la mise à jour du champ. Lance si le champ est déjà mis à jour. |
| [Update](../../aspose.words.fields/field/update)(bool) | Effectue une mise à jour du champ. Lance si le champ est déjà mis à jour. |

### Remarques

Insère le contenu du **La source** élément avec un spécifié **Étiquette** élément utilisant un style bibliographique.

### Exemples

Montre comment travailler avec les champs CITATION et BIBLIOGRAPHIE.

```csharp
// Ouvre un document contenant des sources bibliographiques que l'on peut trouver dans
// Microsoft Word via Références -> Citations & Bibliographie -> Gérer les sources.
Document doc = new Document(MyDir + "Bibliography.docx");
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Text to be cited with one source.");

// Crée une citation avec juste le numéro de page et l'auteur du livre référencé.
FieldCitation fieldCitation = (FieldCitation)builder.InsertField(FieldType.FieldCitation, true);

// Nous nous référons aux sources en utilisant leurs noms de balises.
fieldCitation.SourceTag = "Book1";
fieldCitation.PageNumber = "85";
fieldCitation.SuppressAuthor = false;
fieldCitation.SuppressTitle = true;
fieldCitation.SuppressYear = true;

Assert.AreEqual(" CITATION  Book1 \\p 85 \\t \\y", fieldCitation.GetFieldCode());

// Crée une citation plus détaillée qui cite deux sources.
builder.InsertParagraph();
builder.Write("Text to be cited with two sources.");
fieldCitation = (FieldCitation)builder.InsertField(FieldType.FieldCitation, true);
fieldCitation.SourceTag = "Book1";
fieldCitation.AnotherSourceTag = "Book2";
fieldCitation.FormatLanguageId = "en-US";
fieldCitation.PageNumber = "19";
fieldCitation.Prefix = "Prefix ";
fieldCitation.Suffix = " Suffix";
fieldCitation.SuppressAuthor = false;
fieldCitation.SuppressTitle = false;
fieldCitation.SuppressYear = false;
fieldCitation.VolumeNumber = "VII";

Assert.AreEqual(" CITATION  Book1 \\m Book2 \\l en-US \\p 19 \\f \"Prefix \" \\s \" Suffix\" \\v VII", fieldCitation.GetFieldCode());

// Nous pouvons utiliser un champ BIBLIOGRAPHIE pour afficher toutes les sources dans le document.
builder.InsertBreak(BreakType.PageBreak);
FieldBibliography fieldBibliography = (FieldBibliography)builder.InsertField(FieldType.FieldBibliography, true);
fieldBibliography.FormatLanguageId = "1124";

Assert.AreEqual(" BIBLIOGRAPHY  \\l 1124", fieldBibliography.GetFieldCode());

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.CITATION.docx");
```

### Voir également

* class [Field](../field)
* espace de noms [Aspose.Words.Fields](../../aspose.words.fields)
* Assemblée [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
