---
title: DocumentProperty.ToString
second_title: Aspose.Words för .NET API Referens
description: DocumentProperty metod. Returnerar egenskapsvärdet som en sträng formaterad enligt det aktuella språket.
type: docs
weight: 110
url: /sv/net/aspose.words.properties/documentproperty/tostring/
---
## DocumentProperty.ToString method

Returnerar egenskapsvärdet som en sträng formaterad enligt det aktuella språket.

```csharp
public override string ToString()
```

### Anmärkningar

Konverterar en boolesk egenskap till "Y" eller "N". Konverterar en date-egenskap till en kort datumsträng. För alla andra typer konverterar en egenskap med Object.ToString().

### Exempel

Visar olika typer av konverteringsmetoder för anpassade dokumentegenskaper.

```csharp
Document doc = new Document();
CustomDocumentProperties properties = doc.CustomDocumentProperties;

DateTime authDate = DateTime.Today;
properties.Add("Authorized", true);
properties.Add("Authorized By", "John Doe");
properties.Add("Authorized Date", authDate);
properties.Add("Authorized Revision", doc.BuiltInDocumentProperties.RevisionNumber);
properties.Add("Authorized Amount", 123.45);

Assert.AreEqual(true, properties["Authorized"].ToBool());
Assert.AreEqual("John Doe", properties["Authorized By"].ToString());
Assert.AreEqual(authDate, properties["Authorized Date"].ToDateTime());
Assert.AreEqual(1, properties["Authorized Revision"].ToInt());
Assert.AreEqual(123.45d, properties["Authorized Amount"].ToDouble());
```

Visar hur man arbetar med anpassade dokumentegenskaper.

```csharp
Document doc = new Document(MyDir + "Properties.docx");

// Varje dokument innehåller en samling anpassade egenskaper, som, liksom de inbyggda egenskaperna, är nyckel-värdepar.
 // Dokumentet har en fast lista med inbyggda egenskaper. Användaren skapar alla anpassade egenskaper.
Assert.AreEqual("Value of custom document property", doc.CustomDocumentProperties["CustomProperty"].ToString());

doc.CustomDocumentProperties.Add("CustomProperty2", "Value of custom document property #2");

Console.WriteLine("Custom Properties:");
foreach (var customDocumentProperty in doc.CustomDocumentProperties)
{
    Console.WriteLine(customDocumentProperty.Name);
    Console.WriteLine($"\tType:\t{customDocumentProperty.Type}");
    Console.WriteLine($"\tValue:\t\"{customDocumentProperty.Value}\"");
}
```

### Se även

* class [DocumentProperty](../)
* namnutrymme [Aspose.Words.Properties](../../documentproperty/)
* hopsättning [Aspose.Words](../../../)


