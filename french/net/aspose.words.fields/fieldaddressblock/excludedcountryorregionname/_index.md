---
title: FieldAddressBlock.ExcludedCountryOrRegionName
second_title: Référence de l'API Aspose.Words pour .NET
description: FieldAddressBlock propriété. Obtient ou définit le nom du pays/de la région exclu.
type: docs
weight: 20
url: /fr/net/aspose.words.fields/fieldaddressblock/excludedcountryorregionname/
---
## FieldAddressBlock.ExcludedCountryOrRegionName property

Obtient ou définit le nom du pays/de la région exclu.

```csharp
public string ExcludedCountryOrRegionName { get; set; }
```

### Exemples

Montre comment insérer un champ ADDRESSBLOCK.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldAddressBlock field = (FieldAddressBlock)builder.InsertField(FieldType.FieldAddressBlock, true);

Assert.AreEqual(" ADDRESSBLOCK ", field.GetFieldCode());

// Définir ceci sur "2" inclura tous les pays et régions,
// sauf s'il s'agit de celui spécifié dans la propriété ExcludCountryOrRegionName.
field.IncludeCountryOrRegionName = "2";
field.FormatAddressOnCountryOrRegion = true;
field.ExcludedCountryOrRegionName = "United States";
field.NameAndAddressFormat = "<Title> <Forename> <Surname> <Address Line 1> <Region> <Postcode> <Country>";

// Par défaut, cette propriété contiendra l'ID de langue du premier caractère du document.
// Nous pouvons définir une culture différente pour le champ afin de formater le résultat comme ceci.
field.LanguageId = new CultureInfo("en-US").LCID.ToString();

Assert.AreEqual(
    " ADDRESSBLOCK  \\c 2 \\d \\e \"United States\" \\f \"<Title> <Forename> <Surname> <Address Line 1> <Region> <Postcode> <Country>\" \\l 1033",
    field.GetFieldCode());
```

### Voir également

* class [FieldAddressBlock](../)
* espace de noms [Aspose.Words.Fields](../../fieldaddressblock/)
* Assemblée [Aspose.Words](../../../)


