---
title: Document.UpdateWordCount
linktitle: UpdateWordCount
articleTitle: UpdateWordCount
second_title: Aspose.Words för .NET
description: Document UpdateWordCount metod. Uppdaterar ordräkningsegenskaper för dokumentet i C#.
type: docs
weight: 790
url: /sv/net/aspose.words/document/updatewordcount/
---
## UpdateWordCount() {#updatewordcount}

Uppdaterar ordräkningsegenskaper för dokumentet.

```csharp
public void UpdateWordCount()
```

## Anmärkningar

`UpdateWordCount` räknar om och uppdaterar egenskaperna Characters, Words and Paragraphs i[`BuiltInDocumentProperties`](../builtindocumentproperties/) samling av[`Document`](../).

Anteckna det`UpdateWordCount`uppdaterar inte antalet rader och sidor egenskaper. Använd`UpdateWordCount` överbelastning och passera`Sann` värde som en parameter för att göra det.

När du använder en utvärderingsversion kommer utvärderingsvattenstämpeln också att inkluderas i ordantalet.

## Exempel

Visar hur du uppdaterar alla listetiketter i ett dokument.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
builder.Write("Ut enim ad minim veniam, " +
                "quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

// Aspose.Words spårar inte dokumentmått som dessa i realtid.
Assert.AreEqual(0, doc.BuiltInDocumentProperties.Characters);
Assert.AreEqual(0, doc.BuiltInDocumentProperties.Words);
Assert.AreEqual(1, doc.BuiltInDocumentProperties.Paragraphs);
Assert.AreEqual(1, doc.BuiltInDocumentProperties.Lines);

// För att få korrekta värden för tre av dessa egenskaper måste vi uppdatera dem manuellt.
doc.UpdateWordCount();

Assert.AreEqual(196, doc.BuiltInDocumentProperties.Characters);
Assert.AreEqual(36, doc.BuiltInDocumentProperties.Words);
Assert.AreEqual(2, doc.BuiltInDocumentProperties.Paragraphs);

// För radräkningen måste vi anropa en specifik överbelastning av uppdateringsmetoden.
Assert.AreEqual(1, doc.BuiltInDocumentProperties.Lines);

doc.UpdateWordCount(true);

Assert.AreEqual(4, doc.BuiltInDocumentProperties.Lines);
```

### Se även

* class [Document](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)

---

## UpdateWordCount(*bool*) {#updatewordcount_1}

Uppdaterar ordräkningsegenskaper för dokumentet, uppdaterar eventuellt[`Lines`](../../../aspose.words.properties/builtindocumentproperties/lines/) egenskap.

```csharp
public void UpdateWordCount(bool updateLinesCount)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| updateLinesCount | Boolean | `Sann` om antal rader i dokumentet ska beräknas. |

## Anmärkningar

Den här metoden kommer att återskapa sidlayouten för dokumentet.

## Exempel

Visar hur du uppdaterar alla listetiketter i ett dokument.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
builder.Write("Ut enim ad minim veniam, " +
                "quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

// Aspose.Words spårar inte dokumentmått som dessa i realtid.
Assert.AreEqual(0, doc.BuiltInDocumentProperties.Characters);
Assert.AreEqual(0, doc.BuiltInDocumentProperties.Words);
Assert.AreEqual(1, doc.BuiltInDocumentProperties.Paragraphs);
Assert.AreEqual(1, doc.BuiltInDocumentProperties.Lines);

// För att få korrekta värden för tre av dessa egenskaper måste vi uppdatera dem manuellt.
doc.UpdateWordCount();

Assert.AreEqual(196, doc.BuiltInDocumentProperties.Characters);
Assert.AreEqual(36, doc.BuiltInDocumentProperties.Words);
Assert.AreEqual(2, doc.BuiltInDocumentProperties.Paragraphs);

// För radräkningen måste vi anropa en specifik överbelastning av uppdateringsmetoden.
Assert.AreEqual(1, doc.BuiltInDocumentProperties.Lines);

doc.UpdateWordCount(true);

Assert.AreEqual(4, doc.BuiltInDocumentProperties.Lines);
```

### Se även

* class [Document](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
