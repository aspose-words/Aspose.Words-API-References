---
title: FieldAddressBlock.LanguageId
second_title: Référence de l'API Aspose.Words pour .NET
description: FieldAddressBlock propriété. Obtient ou définit lID de langue utilisé pour formater ladresse.
type: docs
weight: 50
url: /fr/net/aspose.words.fields/fieldaddressblock/languageid/
---
## FieldAddressBlock.LanguageId property

Obtient ou définit l'ID de langue utilisé pour formater l'adresse.

```csharp
public string LanguageId { get; set; }
```

### Exemples

Montre comment insérer un champ ADDRESSBLOCK.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldAddressBlock field = (FieldAddressBlock)builder.InsertField(FieldType.FieldAddressBlock, true);

Assert.AreEqual(" ADDRESSBLOCK ", field.GetFieldCode());

// Définir ceci sur "2" inclura tous les pays et régions,
// sauf s'il s'agit de celui spécifié dans la propriété ExcludedCountryOrRegionName.
field.IncludeCountryOrRegionName = "2";
field.FormatAddressOnCountryOrRegion = true;
field.ExcludedCountryOrRegionName = "United States";
field.NameAndAddressFormat = "<Title> <Forename> <Surname> <Address Line 1> <Region> <Postcode> <Country>";

// Par défaut, cette propriété contiendra l'ID de langue du premier caractère du document.
// Nous pouvons définir une culture différente pour le champ avec lequel formater le résultat comme ceci.
field.LanguageId = new CultureInfo("en-US").LCID.ToString();

Assert.AreEqual(
    " ADDRESSBLOCK  \\c 2 \\d \\e \"United States\" \\f \"<Title> <Forename> <Surname> <Address Line 1> <Region> <Postcode> <Country>\" \\l 1033",
    field.GetFieldCode());
```

### Voir également

* class [FieldAddressBlock](../)
* espace de noms [Aspose.Words.Fields](../../fieldaddressblock/)
* Assemblée [Aspose.Words](../../../)


