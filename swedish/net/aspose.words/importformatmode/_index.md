---
title: Enum ImportFormatMode
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.ImportFormatMode uppräkning. Anger hur formatering slås samman vid import av innehåll från ett annat dokument.
type: docs
weight: 3230
url: /sv/net/aspose.words/importformatmode/
---
## ImportFormatMode enumeration

Anger hur formatering slås samman vid import av innehåll från ett annat dokument.

```csharp
public enum ImportFormatMode
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| UseDestinationStyles | `0` | Använd måldokumentstilarna och kopiera nya formatmallar. Detta är standardalternativet. |
| KeepSourceFormatting | `1` | Kopiera alla nödvändiga stilar till måldokumentet, generera unika stilnamn om det behövs. |
| KeepDifferentStyles | `2` | Kopiera bara stilar som skiljer sig från de i källdokumentet. |

### Anmärkningar

När du kopierar noder från ett dokument till ett annat anger det här alternativet hur formatting löses när båda dokumenten har en stil med samma namn, men olika formatering.

Formateringen löses enligt följande:

1. Inbyggda stilar matchas med deras lokaloberoende stilidentifierare. Användardefinierade stilar matchas med skiftlägeskänsliga stilnamn.
2. Om en matchande stil inte hittas i måldokumentet, kopieras style (och alla stilar som den refererar till) till destinationen document och de importerade noderna uppdateras för att referera till den nya stilen.
3. Om en matchande stil redan finns i måldokumentet beror vad som händer på`importFormatMode` parameter skickad till [`Document.ImportNode`](../documentbase/importnode/) enligt beskrivningen nedan.

När du använderUseDestinationStyles alternativet, om en matchande stil redan existerar i måldokumentet, kopieras inte stilen och de importerade noderna uppdateras för att referera till den befintliga stilen.

Nackdelen med att användaUseDestinationStylesär att den importerade texten kanske ser annorlunda ut i måldokumentet jämfört med källdokumentet. Till exempel använder stilen "Rubrik 1" i källdokumentet Arial 16pt teckensnitt och stilen "Rubrik 1" i måldokumentet använder Times New Roman 14pt font. När du importerar text med stilen "Rubrik 1" utan annan direkt formatering, kommer den att visas som Times New Roman 14pt font i måldokumentet.

KeepSourceFormattingalternativet gör det möjligt att se till att det importerade innehållet ser likadant ut i måldokumentet som det ser ut i källdokumentet. Om en matchande stil redan finns i måldokumentet expanderas källformatet till direkta nodattribut och stilen är ändras till Normal. Om stilen inte finns i måldokumentet importeras källformatet till måldokumentet och tillämpas på den importerade noden. Observera att det inte alltid är möjligt att bevara källformatet även om det finns inte i måldokumentet. I det här fallet kommer formateringen av en sådan stil att utökas till direkta nodattribut till förmån för att bevara den ursprungliga nodformateringen.

Nackdelen med att användaKeepSourceFormattingär att om du utför flera importer, kan du få många stilar i måldokumentet och det kan göra det svårt att använda konsekvent formatering i Microsoft Word för detta dokument.

Använder sig avKeepDifferentStyles alternativet tillåter att återanvända destinationsstilar om formateringen de tillhandahåller är identisk med stilarna i källdokumentet. Om stilen i måldokumentet skiljer sig från källan importeras den.

### Exempel

Visar hur man infogar ett dokument i ett annat dokument.

```csharp
Document doc = new Document(MyDir + "Document.docx");

DocumentBuilder builder = new DocumentBuilder(doc);
builder.MoveToDocumentEnd();
builder.InsertBreak(BreakType.PageBreak);

Document docToInsert = new Document(MyDir + "Formatted elements.docx");

builder.InsertDocument(docToInsert, ImportFormatMode.KeepSourceFormatting);
builder.Document.Save(ArtifactsDir + "DocumentBuilder.InsertDocument.docx");
```

### Se även

* namnutrymme [Aspose.Words](../../aspose.words/)
* hopsättning [Aspose.Words](../../)


