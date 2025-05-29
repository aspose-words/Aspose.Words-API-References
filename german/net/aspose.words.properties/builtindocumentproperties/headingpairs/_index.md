---
title: BuiltInDocumentProperties.HeadingPairs
linktitle: HeadingPairs
articleTitle: HeadingPairs
second_title: Aspose.Words für .NET
description: Erkunden Sie die Eigenschaft „HeadingPairs“ in „BuiltInDocumentProperties“, um Dokumentüberschriften einfach zu verwalten und Ihre Dokumentorganisation zu verbessern.
type: docs
weight: 110
url: /de/net/aspose.words.properties/builtindocumentproperties/headingpairs/
---
## BuiltInDocumentProperties.HeadingPairs property

Gibt Dokumentüberschriften und deren Namen an.

```csharp
public object[] HeadingPairs { get; set; }
```

## Bemerkungen

Jedes Überschriftenpaar belegt zwei Elemente in diesem Array.

Das erste Element des Paares ist einString und gibt den Namen der Überschrift an. Das zweite Element des Paares ist einInt32 und gibt die Anzahl der document Teile für diese Überschrift in der[`TitlesOfParts`](../titlesofparts/) Eigentum.

Die Gesamtsumme der Zählungen für alle Überschriftenpaare in dieser Eigenschaft muss gleich der Anzahl der Elemente in der[`TitlesOfParts`](../titlesofparts/) Eigentum.

Aspose.Words aktualisiert diese Eigenschaft nicht.

## Beispiele

Zeigt die Beziehung zwischen den Eigenschaften „HeadingPairs“ und „TitlesOfParts“.

```csharp
Document doc = new Document(MyDir + "Heading pairs and titles of parts.docx");

// Wir können die kombinierten Werte dieser Sammlungen finden über
// "Datei" -> "Eigenschaften" -> "Erweiterte Eigenschaften" -> Registerkarte "Inhalt".
// Die Eigenschaft HeadingPairs ist eine Sammlung von <string, int> Paaren, die
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
* namensraum [Aspose.Words.Properties](../../../aspose.words.properties/)
* Montage [Aspose.Words](../../../)
