---
title: FieldAddressBlock.LanguageId
linktitle: LanguageId
articleTitle: LanguageId
second_title: Aspose.Words per .NET
description: Gestisci la formattazione degli indirizzi senza problemi con la proprietà LanguageId di FieldAddressBlock. Imposta o recupera l'ID della lingua per una localizzazione fluida.
type: docs
weight: 50
url: /it/net/aspose.words.fields/fieldaddressblock/languageid/
---
## FieldAddressBlock.LanguageId property

Ottiene o imposta l'ID della lingua utilizzata per formattare l'indirizzo.

```csharp
public string LanguageId { get; set; }
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
