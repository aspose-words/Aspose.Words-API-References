---
title: FieldAddressBlock.ExcludedCountryOrRegionName
linktitle: ExcludedCountryOrRegionName
articleTitle: ExcludedCountryOrRegionName
second_title: Aspose.Words per .NET
description: Gestisci facilmente i paesi/regioni esclusi con la proprietà FieldAddressBlock ExcludedCountryOrRegionName. Ottimizza la gestione dei tuoi indirizzi oggi stesso!
type: docs
weight: 20
url: /it/net/aspose.words.fields/fieldaddressblock/excludedcountryorregionname/
---
## FieldAddressBlock.ExcludedCountryOrRegionName property

Ottiene o imposta il nome del paese/regione escluso.

```csharp
public string ExcludedCountryOrRegionName { get; set; }
```

## Esempi

Mostra come inserire un campo ADDRESSBLOCK.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldAddressBlock field = (FieldAddressBlock)builder.InsertField(FieldType.FieldAddressBlock, true);

Assert.AreEqual(" ADDRESSBLOCK ", field.GetFieldCode());

// Impostando questo valore su "2" verranno inclusi tutti i paesi e le regioni,
// a meno che non sia quello specificato nella proprietà ExcludedCountryOrRegionName.
field.IncludeCountryOrRegionName = "2";
field.FormatAddressOnCountryOrRegion = true;
field.ExcludedCountryOrRegionName = "United States";
field.NameAndAddressFormat = "<Title> <Forename> <Surname> <Address Line 1> <Region> <Postcode> <Country>";

// Per impostazione predefinita, questa proprietà conterrà l'ID della lingua del primo carattere del documento.
// Possiamo impostare una cultura diversa per il campo per formattare il risultato in questo modo.
field.LanguageId = new CultureInfo("en-US").LCID.ToString();

Assert.AreEqual(
    " ADDRESSBLOCK  \\c 2 \\d \\e \"United States\" \\f \"<Title> <Forename> <Surname> <Address Line 1> <Region> <Postcode> <Country>\" \\l 1033",
    field.GetFieldCode());
```

### Guarda anche

* class [FieldAddressBlock](../)
* spazio dei nomi [Aspose.Words.Fields](../../../aspose.words.fields/)
* assemblea [Aspose.Words](../../../)
