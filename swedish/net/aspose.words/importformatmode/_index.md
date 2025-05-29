---
title: ImportFormatMode Enum
linktitle: ImportFormatMode
articleTitle: ImportFormatMode
second_title: Aspose.Words för .NET
description: Upptäck hur Aspose.Words.ImportFormatMode förbättrar dokumentformateringen genom att sömlöst sammanfoga stilar från importerat innehåll för optimala resultat.
type: docs
weight: 3680
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
| UseDestinationStyles | `0` | Använd måldokumentets formatmallar och kopiera nya formatmallar. Detta är standardalternativet. |
| KeepSourceFormatting | `1` | Kopiera alla nödvändiga stilar till destinationsdokumentet, generera unika stilnamn om det behövs. |
| KeepDifferentStyles | `2` | Kopiera endast stilar som skiljer sig från de i källdokumentet. |

## Anmärkningar

När du kopierar noder från ett dokument till ett annat anger det här alternativet hur formatering ska lösas när båda dokumenten har en stil med samma namn men olika formatering.

Formateringen löses enligt följande:

1. Inbyggda stilar matchas med hjälp av deras språkoberoende stilidentifierare. Användardefinierade stilar matchas med hjälp av skiftlägeskänsligt stilnamn.
2. Om ett matchande format inte hittas i destinationsdokumentet kopieras style (och alla format som refereras av det) till destinationsdokumentet document och de importerade noderna uppdateras för att referera till det nya formatet.
3. Om en matchande stil redan finns i destinationsdokumentet beror det som händer på`importFormatMode` parameter skickad till [`ImportNode`](../documentbase/importnode/) enligt beskrivningen nedan.

När du använderUseDestinationStyles alternativet, om en matchande stil redan finns i destinationsdokumentet, kopieras inte stilen och de importerade noderna uppdateras för att referera till den befintliga stilen.

Nackdelen med att användaUseDestinationStylesär att den importerade texten kan se annorlunda ut i destinationsdokumentet jämfört med källdokumentet. Till exempel använder formatet "Rubrik 1" i källdokumentet Arial 16pt-typsnittet och använder formatet "Rubrik 1" i destinationsdokumentet Times New Roman 14pt-typsnittet. När du importerar text i formatet "Rubrik 1" utan annan direkt formatering kommer den att visas som Times New Roman 14pt-typsnitt i destinationsdokumentet.

KeepSourceFormattingAlternativet gör det möjligt att säkerställa att det importerade innehållet ser ut på samma sätt i destinationsdokumentet som det ser ut i källdokumentet. Om en matchande stil redan finns i destinationsdokumentet expanderas källstilens formatering till direkta nodattribut och stilen ändras till Normal. Om stilen inte finns i destinationsdokumentet importeras källstilen till destinationsdokumentet och tillämpas på den importerade noden. Observera att det inte alltid är möjligt att bevara källstilen även om den inte finns i destinationsdokumentet. I det här fallet kommer formateringen av en sådan stil att expanderas till direkta nodattribut till förmån för att bevara den ursprungliga nodformateringen.

Nackdelen med att användaKeepSourceFormattingär att om du utför flera importer, kan du få många stilar i destinationsdokumentet och det kan göra det svårt att använda konsekvent stilformatering i Microsoft Word för det här dokumentet.

AnvändningKeepDifferentStyles Alternativet tillåter återanvändning av destinationsstilar om formateringen de tillhandahåller är identisk med stilarna i källdokumentet. Om stilen i destinationsdokumentet skiljer sig från källdokumentet importeras den.

## Exempel

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
