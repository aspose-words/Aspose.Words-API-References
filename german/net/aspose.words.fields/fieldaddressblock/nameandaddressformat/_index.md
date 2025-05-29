---
title: FieldAddressBlock.NameAndAddressFormat
linktitle: NameAndAddressFormat
articleTitle: NameAndAddressFormat
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „NameAndAddressFormat“ des FieldAddressBlocks, um Namens- und Adressformate für eine verbesserte Datenverwaltung einfach anzupassen.
type: docs
weight: 60
url: /de/net/aspose.words.fields/fieldaddressblock/nameandaddressformat/
---
## FieldAddressBlock.NameAndAddressFormat property

Ruft das Namens- und Adressformat ab oder legt es fest.

```csharp
public string NameAndAddressFormat { get; set; }
```

## Beispiele

Zeigt, wie ein ADDRESSBLOCK-Feld eingefügt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldAddressBlock field = (FieldAddressBlock)builder.InsertField(FieldType.FieldAddressBlock, true);

Assert.AreEqual(" ADDRESSBLOCK ", field.GetFieldCode());

// Wenn Sie diesen Wert auf "2" setzen, werden alle Länder und Regionen einbezogen.
// es sei denn, es handelt sich um das in der Eigenschaft „ExcludedCountryOrRegionName“ angegebene Land.
field.IncludeCountryOrRegionName = "2";
field.FormatAddressOnCountryOrRegion = true;
field.ExcludedCountryOrRegionName = "United States";
field.NameAndAddressFormat = "<Title> <Forename> <Surname> <Address Line 1> <Region> <Postcode> <Country>";

// Standardmäßig enthält diese Eigenschaft die Sprach-ID des ersten Zeichens des Dokuments.
// Wir können eine andere Kultur für das Feld festlegen, um das Ergebnis wie folgt zu formatieren.
field.LanguageId = new CultureInfo("en-US").LCID.ToString();

Assert.AreEqual(
    " ADDRESSBLOCK  \\c 2 \\d \\e \"United States\" \\f \"<Title> <Forename> <Surname> <Address Line 1> <Region> <Postcode> <Country>\" \\l 1033",
    field.GetFieldCode());
```

### Siehe auch

* class [FieldAddressBlock](../)
* namensraum [Aspose.Words.Fields](../../../aspose.words.fields/)
* Montage [Aspose.Words](../../../)
