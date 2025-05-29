---
title: DocumentDirection Enum
linktitle: DocumentDirection
articleTitle: DocumentDirection
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.DocumentDirection enum för att enkelt kontrollera textflödet i dina dokument. Förbättra läsbarhet och formatering med denna kraftfulla funktion!
type: docs
weight: 4030
url: /sv/net/aspose.words.loading/documentdirection/
---
## DocumentDirection enumeration

Gör det möjligt att ange riktningen för textflödet i ett dokument.

```csharp
public enum DocumentDirection
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| LeftToRight | `0` | Vänster till höger riktning. |
| RightToLeft | `1` | Höger till vänster riktning. |
| Auto | `2` | Automatisk riktningsdetektering. |

## Exempel

Visar hur man identifierar textriktningen i klartextdokument.

```csharp
// Skapa ett "TxtLoadOptions"-objekt, som vi kan skicka till ett dokuments konstruktor
// för att ändra hur vi laddar ett klartextdokument.
TxtLoadOptions loadOptions = new TxtLoadOptions();

// Sätt egenskapen "DocumentDirection" till "DocumentDirection.Auto" identifierar automatiskt
// riktningen för varje textstycke som Aspose.Words laddar från klartext.
// Varje styckes "Bidi"-egenskap lagrar dess riktning.
loadOptions.DocumentDirection = DocumentDirection.Auto;

// Identifiera hebreisk text som höger-till-vänster.
Document doc = new Document(MyDir + "Hebrew text.txt", loadOptions);

Assert.True(doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Bidi);

// Identifiera engelsk text som höger-till-vänster.
doc = new Document(MyDir + "English text.txt", loadOptions);

Assert.False(doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Bidi);
```

### Se även

* namnutrymme [Aspose.Words.Loading](../../aspose.words.loading/)
* hopsättning [Aspose.Words](../../)
