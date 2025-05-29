---
title: Document.UpdateWordCount
linktitle: UpdateWordCount
articleTitle: UpdateWordCount
second_title: Aspose.Words för .NET
description: Förbättra dokumentets effektivitet med UpdateWordCount-metoden, vilket säkerställer korrekta ordräkningsegenskaper för bättre redigering och granskning.
type: docs
weight: 850
url: /sv/net/aspose.words/document/updatewordcount/
---
## UpdateWordCount() {#updatewordcount}

Uppdaterar dokumentets egenskaper för ordantal.

```csharp
public void UpdateWordCount()
```

## Anmärkningar

`UpdateWordCount` beräknar om och uppdaterar egenskaperna för Tecken, Ord och Stycken i[`BuiltInDocumentProperties`](../builtindocumentproperties/) samling av[`Document`](../).

Observera att`UpdateWordCount` uppdaterar inte egenskaper för antal rader och sidor. Använd`UpdateWordCount` överbelastning och pass`sann` värde som en parameter för att göra det.

När du använder en utvärderingsversion kommer även utvärderingsvattenmärket att inkluderas i ordantalet.

## Exempel

Visar hur man uppdaterar alla listetiketter i ett dokument.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
builder.Write("Ut enim ad minim veniam, " +
                "quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

// Aspose.Words spårar inte dokumentstatistik som dessa i realtid.
Assert.AreEqual(0, doc.BuiltInDocumentProperties.Characters);
Assert.AreEqual(0, doc.BuiltInDocumentProperties.Words);
Assert.AreEqual(1, doc.BuiltInDocumentProperties.Paragraphs);
Assert.AreEqual(1, doc.BuiltInDocumentProperties.Lines);

// För att få korrekta värden för tre av dessa egenskaper måste vi uppdatera dem manuellt.
doc.UpdateWordCount();

Assert.AreEqual(196, doc.BuiltInDocumentProperties.Characters);
Assert.AreEqual(36, doc.BuiltInDocumentProperties.Words);
Assert.AreEqual(2, doc.BuiltInDocumentProperties.Paragraphs);

// För radantalet måste vi anropa en specifik överbelastning av uppdateringsmetoden.
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

Uppdaterar dokumentets ordantal, uppdaterar valfritt[`Lines`](../../../aspose.words.properties/builtindocumentproperties/lines/) egendom.

```csharp
public void UpdateWordCount(bool updateLinesCount)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| updateLinesCount | Boolean | `sann` om antalet rader i dokumentet ska beräknas. |

## Anmärkningar

Den här metoden kommer att återskapa dokumentets sidlayout.

## Exempel

Visar hur man uppdaterar alla listetiketter i ett dokument.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
builder.Write("Ut enim ad minim veniam, " +
                "quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

// Aspose.Words spårar inte dokumentstatistik som dessa i realtid.
Assert.AreEqual(0, doc.BuiltInDocumentProperties.Characters);
Assert.AreEqual(0, doc.BuiltInDocumentProperties.Words);
Assert.AreEqual(1, doc.BuiltInDocumentProperties.Paragraphs);
Assert.AreEqual(1, doc.BuiltInDocumentProperties.Lines);

// För att få korrekta värden för tre av dessa egenskaper måste vi uppdatera dem manuellt.
doc.UpdateWordCount();

Assert.AreEqual(196, doc.BuiltInDocumentProperties.Characters);
Assert.AreEqual(36, doc.BuiltInDocumentProperties.Words);
Assert.AreEqual(2, doc.BuiltInDocumentProperties.Paragraphs);

// För radantalet måste vi anropa en specifik överbelastning av uppdateringsmetoden.
Assert.AreEqual(1, doc.BuiltInDocumentProperties.Lines);

doc.UpdateWordCount(true);

Assert.AreEqual(4, doc.BuiltInDocumentProperties.Lines);
```

### Se även

* class [Document](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
