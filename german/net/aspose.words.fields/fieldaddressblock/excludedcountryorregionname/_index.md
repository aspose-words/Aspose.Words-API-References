---
title: FieldAddressBlock.ExcludedCountryOrRegionName
second_title: Aspose.Words für .NET-API-Referenz
description: FieldAddressBlock eigendom. Ruft den Namen des ausgeschlossenen Landes/der ausgeschlossenen Region ab oder legt ihn fest.
type: docs
weight: 20
url: /de/net/aspose.words.fields/fieldaddressblock/excludedcountryorregionname/
---
## FieldAddressBlock.ExcludedCountryOrRegionName property

Ruft den Namen des ausgeschlossenen Landes/der ausgeschlossenen Region ab oder legt ihn fest.

```csharp
public string ExcludedCountryOrRegionName { get; set; }
```

### Beispiele

Zeigt, wie ein ADRESSBLOCK-Feld eingefügt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldAddressBlock field = (FieldAddressBlock)builder.InsertField(FieldType.FieldAddressBlock, true);

Assert.AreEqual(" ADDRESSBLOCK ", field.GetFieldCode());

// Wenn Sie dies auf "2" setzen, werden alle Länder und Regionen eingeschlossen,
// es sei denn, es handelt sich um den in der Eigenschaft ExcludedCountryOrRegionName angegebenen.
field.IncludeCountryOrRegionName = "2";
field.FormatAddressOnCountryOrRegion = true;
field.ExcludedCountryOrRegionName = "United States";
field.NameAndAddressFormat = "<Title> <Forename> <Surname> <Address Line 1> <Region> <Postcode> <Country>";

// Standardmäßig enthält diese Eigenschaft die Sprach-ID des ersten Zeichens des Dokuments.
// Wir können eine andere Kultur für das Feld festlegen, um das Ergebnis so zu formatieren.
field.LanguageId = new CultureInfo("en-US").LCID.ToString();

Assert.AreEqual(
    " ADDRESSBLOCK  \\c 2 \\d \\e \"United States\" \\f \"<Title> <Forename> <Surname> <Address Line 1> <Region> <Postcode> <Country>\" \\l 1033",
    field.GetFieldCode());
```

### Siehe auch

* class [FieldAddressBlock](../)
* namensraum [Aspose.Words.Fields](../../fieldaddressblock/)
* Montage [Aspose.Words](../../../)


