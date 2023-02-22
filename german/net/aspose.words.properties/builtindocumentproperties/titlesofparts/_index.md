---
title: BuiltInDocumentProperties.TitlesOfParts
second_title: Aspose.Words für .NET-API-Referenz
description: BuiltInDocumentProperties eigendom. Jede Zeichenfolge im Array gibt den Namen eines Teils im Dokument an.
type: docs
weight: 300
url: /de/net/aspose.words.properties/builtindocumentproperties/titlesofparts/
---
## BuiltInDocumentProperties.TitlesOfParts property

Jede Zeichenfolge im Array gibt den Namen eines Teils im Dokument an.

```csharp
public string[] TitlesOfParts { get; set; }
```

### Bemerkungen

Aspose.Words aktualisiert diese Eigenschaft nicht.

### Beispiele

Zeigt die Beziehung zwischen den Eigenschaften „HeadingPairs“ und „TitlesOfParts“.

```csharp
Document doc = new Document(MyDir + "Heading pairs and titles of parts.docx");

// Wir können die kombinierten Werte dieser Sammlungen finden über
// "Datei" -> "Eigenschaften" -> "Erweiterte Eigenschaften" -> Reiter „Inhalt“.
// Die Eigenschaft HeadingPairs ist eine Sammlung von <string, int> paart das
// bestimmt, über wie viele Dokumentteile sich eine Überschrift erstreckt.
object[] headingPairs = doc.BuiltInDocumentProperties.HeadingPairs;

// Die Eigenschaft TitlesOfParts enthält die Namen der Teile, die zu den obigen Überschriften gehören.
string[] titlesOfParts = doc.BuiltInDocumentProperties.TitlesOfParts;

int headingPairsIndex = 0;
int titlesOfPartsIndex = 0;
while (headingPairsIndex < headingPairs.Length)
{
    Console.WriteLine($"Parts for {headingPairs[headingPairsIndex++]}:");
    int partsCount = Convert.ToInt32(headingPairs[headingPairsIndex++]);

    for (int i = 0; i < partsCount; i++)
        Console.WriteLine($"\t\"{titlesOfParts[titlesOfPartsIndex++]}\"");
}
```

### Siehe auch

* class [BuiltInDocumentProperties](../)
* namensraum [Aspose.Words.Properties](../../builtindocumentproperties/)
* Montage [Aspose.Words](../../../)


