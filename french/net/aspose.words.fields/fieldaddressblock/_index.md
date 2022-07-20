---
title: FieldAddressBlock
second_title: Référence de l'API Aspose.Words pour .NET
description: Implémente le champ ADDRESSBLOCK.
type: docs
weight: 1380
url: /fr/net/aspose.words.fields/fieldaddressblock/
---
## FieldAddressBlock class

Implémente le champ ADDRESSBLOCK.

```csharp
public class FieldAddressBlock : Field
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [FieldAddressBlock](fieldaddressblock)() | Default_Constructor |

## Propriétés

| Nom | La description |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult) { get; } | Obtient le texte qui représente le résultat du champ affiché. |
| [End](../../aspose.words.fields/field/end) { get; } | Obtient le nœud qui représente la fin du champ. |
| [ExcludedCountryOrRegionName](../../aspose.words.fields/fieldaddressblock/excludedcountryorregionname) { get; set; } | Obtient ou définit le nom du pays/région exclu. |
| [Format](../../aspose.words.fields/field/format) { get; } | Obtient un[`FieldFormat`](../fieldformat) objet qui fournit un accès typé au formatage du champ. |
| [FormatAddressOnCountryOrRegion](../../aspose.words.fields/fieldaddressblock/formataddressoncountryorregion) { get; set; } | Obtient ou définit s'il faut formater l'adresse en fonction du pays/région du destinataire tel que défini par POST*CODE (Union postale universelle 2006). |
| [IncludeCountryOrRegionName](../../aspose.words.fields/fieldaddressblock/includecountryorregionname) { get; set; } | Obtient ou définit s'il faut inclure le nom du pays/de la région. |
| [IsDirty](../../aspose.words.fields/field/isdirty) { get; set; } | Obtient ou définit si le résultat actuel du champ n'est plus correct (périmé) en raison d'autres modifications apportées au document. |
| [IsLocked](../../aspose.words.fields/field/islocked) { get; set; } | Obtient ou définit si le champ est verrouillé (ne doit pas recalculer son résultat). |
| [LanguageId](../../aspose.words.fields/fieldaddressblock/languageid) { get; set; } | Obtient ou définit l'ID de langue utilisé pour formater l'adresse. |
| [LocaleId](../../aspose.words.fields/field/localeid) { get; set; } | Obtient ou définit le LCID du champ. |
| [NameAndAddressFormat](../../aspose.words.fields/fieldaddressblock/nameandaddressformat) { get; set; } | Obtient ou définit le format du nom et de l'adresse. |
| [Result](../../aspose.words.fields/field/result) { get; set; } | Obtient ou définit le texte qui se trouve entre le séparateur de champ et la fin du champ. |
| [Separator](../../aspose.words.fields/field/separator) { get; } | Obtient le nœud qui représente le séparateur de champs. Peut être null. |
| [Start](../../aspose.words.fields/field/start) { get; } | Obtient le nœud qui représente le début du champ. |
| virtual [Type](../../aspose.words.fields/field/type) { get; } | Obtient le type de champ Microsoft Word. |

## Méthodes

| Nom | La description |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)() | Renvoie le texte entre le début du champ et le séparateur de champ (ou la fin du champ s'il n'y a pas de séparateur). Le code de champ et le résultat du champ des champs enfants sont inclus. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)(bool) | Renvoie le texte entre le début du champ et le séparateur de champ (ou la fin du champ s'il n'y a pas de séparateur). |
| [GetFieldNames](../../aspose.words.fields/fieldaddressblock/getfieldnames)() | Renvoie une collection de noms de champs de fusion et publipostage utilisés par le champ. |
| [Remove](../../aspose.words.fields/field/remove)() | Supprime le champ du document. Renvoie un nœud juste après le champ. Si la fin du champ est le dernier enfant de son nœud parent, renvoie son paragraphe parent. Si le champ est déjà supprimé, renvoie **nul** . |
| [Unlink](../../aspose.words.fields/field/unlink)() | Effectue la dissociation du champ. |
| [Update](../../aspose.words.fields/field/update)() | Effectue la mise à jour du champ. Lance si le champ est déjà mis à jour. |
| [Update](../../aspose.words.fields/field/update)(bool) | Effectue une mise à jour du champ. Lance si le champ est déjà mis à jour. |

### Remarques

Représente un bloc d'adresse. Unbloc d'adresse est un bloc de texte spécifiant les informations appropriées pour une adresse postale, dans l'ordre requis par le pays de destination.

### Exemples

Montre comment obtenir les noms de champs de fusion et publipostage utilisés par un champ.

```csharp
Document doc = new Document(MyDir + "Field sample - ADDRESSBLOCK.docx");

string[] addressFieldsExpect =
{
    "Company", "First Name", "Middle Name", "Last Name", "Suffix", "Address 1", "City", "State",
    "Country or Region", "Postal Code"
};

FieldAddressBlock addressBlockField = (FieldAddressBlock) doc.Range.Fields[0];
string[] addressBlockFieldNames = addressBlockField.GetFieldNames();
```

### Voir également

* class [Field](../field)
* espace de noms [Aspose.Words.Fields](../../aspose.words.fields)
* Assemblée [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
