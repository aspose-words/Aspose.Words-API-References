---
title: BuiltInDocumentProperties.HeadingPairs
second_title: Aspose.Words für .NET-API-Referenz
description: BuiltInDocumentProperties eigendom. Gibt Dokumentüberschriften und deren Namen an.
type: docs
weight: 110
url: /de/net/aspose.words.properties/builtindocumentproperties/headingpairs/
---
## BuiltInDocumentProperties.HeadingPairs property

Gibt Dokumentüberschriften und deren Namen an.

```csharp
public object[] HeadingPairs { get; set; }
```

### Bemerkungen

Jedes Überschriftenpaar belegt zwei Elemente in diesem Array.

Das erste Element des Paares ist aString und gibt den Überschriftennamen an. Das zweite Element des Paares ist einInt32 und gibt die Anzahl der document Teile für diese Überschrift im an[`TitlesOfParts`](../titlesofparts/) Eigentum.

Die Gesamtsumme der Zählungen für alle Überschriftenpaare in dieser Eigenschaft muss gleich der Anzahl der Elemente in der sein[`TitlesOfParts`](../titlesofparts/) Eigentum.

Aspose.Words aktualisiert diese Eigenschaft nicht.

### Beispiele

Zeigt die Beziehung zwischen den Eigenschaften „HeadingPairs“ und „TitlesOfParts“.

```csharp
Document doc = new Document(MyDir + "Heading pairs and titles of parts.docx");

// Wir können die kombinierten Werte dieser Sammlungen finden über
// "Datei" -> „Eigenschaften“ -> „Erweiterte Eigenschaften“ -> Registerkarte „Inhalt“.
// Die HeadingPairs-Eigenschaft ist eine Sammlung von <string, int> passt das zusammen
// bestimmt, über wie viele Dokumentteile sich eine Überschrift erstreckt.
object[] headingPairs = doc.BuiltInDocumentProperties.HeadingPairs;

// Die Eigenschaft TitlesOfParts enthält die Namen der Teile, die zu den oben genannten Überschriften gehören.
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


