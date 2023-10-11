---
title: FieldAddressBlock.NameAndAddressFormat
second_title: Aspose.Words per .NET API Reference
description: FieldAddressBlock proprietà. Ottiene o imposta il formato del nome e dellindirizzo.
type: docs
weight: 60
url: /it/net/aspose.words.fields/fieldaddressblock/nameandaddressformat/
---
## FieldAddressBlock.NameAndAddressFormat property

Ottiene o imposta il formato del nome e dell'indirizzo.

```csharp
public string NameAndAddressFormat { get; set; }
```

### Esempi

Mostra come inserire un campo ADDRESSBLOCK.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldAddressBlock field = (FieldAddressBlock)builder.InsertField(FieldType.FieldAddressBlock, true);

Assert.AreEqual(" ADDRESSBLOCK ", field.GetFieldCode());

// Impostandolo su "2" includerà tutti i paesi e le regioni,
// a meno che non sia quello specificato nella proprietà ExcludedCountryOrRegionName.
field.IncludeCountryOrRegionName = "2";
field.FormatAddressOnCountryOrRegion = true;
field.ExcludedCountryOrRegionName = "United States";
field.NameAndAddressFormat = "<Title> <Forename> <Surname> <Address Line 1> <Region> <Postcode> <Country>";

// Per impostazione predefinita, questa proprietà conterrà l'ID della lingua del primo carattere del documento.
// Possiamo impostare una cultura diversa per il campo con cui formattare il risultato in questo modo.
field.LanguageId = new CultureInfo("en-US").LCID.ToString();

Assert.AreEqual(
    " ADDRESSBLOCK  \\c 2 \\d \\e \"United States\" \\f \"<Title> <Forename> <Surname> <Address Line 1> <Region> <Postcode> <Country>\" \\l 1033",
    field.GetFieldCode());
```

### Guarda anche

* class [FieldAddressBlock](../)
* spazio dei nomi [Aspose.Words.Fields](../../fieldaddressblock/)
* assemblea [Aspose.Words](../../../)


