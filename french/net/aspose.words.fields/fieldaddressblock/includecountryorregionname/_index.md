---
title: FieldAddressBlock.IncludeCountryOrRegionName
linktitle: IncludeCountryOrRegionName
articleTitle: IncludeCountryOrRegionName
second_title: Aspose.Words pour .NET
description: FieldAddressBlock IncludeCountryOrRegionName propriété. Obtient ou définit sil faut inclure le nom du pays/de la région en C#.
type: docs
weight: 40
url: /fr/net/aspose.words.fields/fieldaddressblock/includecountryorregionname/
---
## FieldAddressBlock.IncludeCountryOrRegionName property

Obtient ou définit s'il faut inclure le nom du pays/de la région.

```csharp
public string IncludeCountryOrRegionName { get; set; }
```

## Exemples

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
* espace de noms [Aspose.Words.Fields](../../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../../)
