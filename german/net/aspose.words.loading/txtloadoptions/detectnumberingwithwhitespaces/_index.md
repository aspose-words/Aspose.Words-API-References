---
title: TxtLoadOptions.DetectNumberingWithWhitespaces
second_title: Aspose.Words für .NET-API-Referenz
description: TxtLoadOptions eigendom. Ermöglicht die Angabe wie nummerierte Listenelemente erkannt werden wenn ein Dokument aus dem NurTextFormat importiert wird. Der Standardwert istWAHR.
type: docs
weight: 40
url: /de/net/aspose.words.loading/txtloadoptions/detectnumberingwithwhitespaces/
---
## TxtLoadOptions.DetectNumberingWithWhitespaces property

Ermöglicht die Angabe, wie nummerierte Listenelemente erkannt werden, wenn ein Dokument aus dem Nur-Text-Format importiert wird. Der Standardwert ist`WAHR`.

```csharp
public bool DetectNumberingWithWhitespaces { get; set; }
```

### Bemerkungen

Wenn diese Option auf eingestellt ist`FALSCH`Der Listenerkennungsalgorithmus erkennt Listenabsätze, wenn Listennummern mit enden, entweder mit einem Punkt, einer rechten Klammer oder einem Aufzählungszeichen (z. B. „•“, „*“, „-“ oder „o“).

Wenn diese Option auf eingestellt ist`WAHR`Leerzeichen werden auch als Trennzeichen für Listennummern verwendet: Der Listenerkennungsalgorithmus für die Nummerierung im arabischen Stil (1., 1.1.2.) verwendet sowohl Leerzeichen als auch Punktsymbole (".").

### Beispiele

Zeigt, wie Listen beim Laden von Klartextdokumenten erkannt werden.

```csharp
// Erstelle ein Klartextdokument in einem String mit vier separaten Teilen, die wir als Listen interpretieren können,
// mit unterschiedlichen Trennzeichen. Beim Laden des Klartextdokuments in ein „Document“-Objekt,
// Aspose.Words erkennt immer die ersten drei Listen und fügt ein „List“-Objekt hinzu
// für jedes in die Eigenschaft „Lists“ des Dokuments.
const string textDoc = "Full stop delimiters:\n" +
                       "1. First list item 1\n" +
                       "2. First list item 2\n" +
                       "3. First list item 3\n\n" +
                       "Right bracket delimiters:\n" +
                       "1) Second list item 1\n" +
                       "2) Second list item 2\n" +
                       "3) Second list item 3\n\n" +
                       "Bullet delimiters:\n" +
                       "• Third list item 1\n" +
                       "• Third list item 2\n" +
                       "• Third list item 3\n\n" +
                       "Whitespace delimiters:\n" +
                       "1 Fourth list item 1\n" +
                       "2 Fourth list item 2\n" +
                       "3 Fourth list item 3";

// Erstelle ein „TxtLoadOptions“-Objekt, das wir an den Konstruktor eines Dokuments übergeben können
// um zu ändern, wie wir ein Klartextdokument laden.
TxtLoadOptions loadOptions = new TxtLoadOptions();

// Setzen Sie die Eigenschaft „DetectNumberingWithWhitespaces“ auf „true“, um nummerierte Elemente zu erkennen
// mit Leerzeichen-Trennzeichen, wie die vierte Liste in unserem Dokument, als Listen.
// Dies kann auch dazu führen, dass Absätze, die mit Zahlen beginnen, fälschlicherweise als Listen erkannt werden.
// Setze die Eigenschaft „DetectNumberingWithWhitespaces“ auf „false“
// um keine Listen aus nummerierten Elementen mit Leerzeichen als Trennzeichen zu erstellen.
loadOptions.DetectNumberingWithWhitespaces = detectNumberingWithWhitespaces;

Document doc = new Document(new MemoryStream(Encoding.UTF8.GetBytes(textDoc)), loadOptions);

if (detectNumberingWithWhitespaces)
{
    Assert.AreEqual(4, doc.Lists.Count);
    Assert.True(doc.FirstSection.Body.Paragraphs.Any(p => p.GetText().Contains("Fourth list") && ((Paragraph)p).IsListItem));
}
else
{
    Assert.AreEqual(3, doc.Lists.Count);
    Assert.False(doc.FirstSection.Body.Paragraphs.Any(p => p.GetText().Contains("Fourth list") && ((Paragraph)p).IsListItem));
}
```

### Siehe auch

* class [TxtLoadOptions](../)
* namensraum [Aspose.Words.Loading](../../txtloadoptions/)
* Montage [Aspose.Words](../../../)


