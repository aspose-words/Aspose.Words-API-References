---
title: "Aspose::Words::ImportFormatMode-enum"
linktitle: "ImportFormatMode"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::ImportFormatMode-enum. Anger hur formatering slås samman när innehåll importeras från ett annat dokument i C++."
type: docs
weight: 93000
url: /sv/cpp/aspose.words/importformatmode/
---
## ImportFormatMode enum


Anger hur formatering slås ihop när innehåll importeras från ett annat dokument.

```cpp
enum class ImportFormatMode
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| UseDestinationStyles | 0 | Använd destinationsdokumentets stilar och kopiera nya stilar. Detta är standardalternativet. |
| KeepSourceFormatting | 1 | Kopiera alla nödvändiga formatmallar till destinationsdokumentet, skapa unika formatmallnamn om det behövs. |
| KeepDifferentStyles | 2 | Kopiera endast formatmallar som skiljer sig från dem i källdokumentet. |

## Anmärkningar


När du kopierar noder från ett dokument till ett annat anger detta alternativ hur formatering löses när båda dokumenten har en formatmall med samma namn, men olika formatering.

Formateringen löses enligt följande:

1. Inbyggda formatmallar matchas med deras språkoberoende stilidentifierare. Användardefinierade formatmallar matchas med skiftlägeskänsligt stilnamn.
1. Om en matchande formatmall inte hittas i destinationsdokumentet kopieras formatmallen (och alla formatmallar som den refererar till) till destinationsdokumentet och de importerade noderna uppdateras för att referera till den nya formatmallen.
1. Om en matchande formatmall redan finns i destinationsdokumentet beror vad som händer på parametern **importFormatMode** som skickas till [ImportNode()](../) enligt beskrivningen nedan.



När du använder alternativet [UseDestinationStyles](./) och en matchande formatmall redan finns i destinationsdokumentet kopieras inte formatmallen och de importerade noderna uppdateras för att referera till den befintliga formatmallen.

Nackdelen med att använda [UseDestinationStyles](./) är att den importerade texten kan se annorlunda ut i destinationsdokumentet jämfört med källdokumentet. Till exempel använder formatmallen "Heading 1" i källdokumentet Arial 16pt och formatmallen "Heading 1" i destinationsdokumentet Times New Roman 14pt. När text med formatmallen "Heading 1" importeras utan annan direkt formatering kommer den att visas som Times New Roman 14pt i destinationsdokumentet.

[KeepSourceFormatting](./) option allows to make sure the imported content looks the same in the destination document like it looks in the source document. If a matching style already exists in the destination document, the source style formatting is expanded into direct [Node](../node/) attributes and the style is changed to Normal. If the style does not exist in the destination document, then the source style is imported into the destination document and applied to the imported node. Note, that it is not always possible to preserve the source style even if it does not exist in the destination document. In this case formatting of such style will be expanded into direct [Node](../node/) attributes in favor of preserving original [Node](../node/) formatting.

Nackdelen med att använda [KeepSourceFormatting](./) är att om du utför flera importeringar kan du få många formatmallar i destinationsdokumentet, vilket kan göra det svårt att använda enhetlig stilformatering i Microsoft Word för detta dokument.

Att använda alternativet [KeepDifferentStyles](./) möjliggör återanvändning av destinationsformatmallar om den formatering de ger är identisk med formatmallarna i källdokumentet. Om formatmallen i destinationsdokumentet skiljer sig från källan importeras den.

## Exempel



Visar hur man infogar ett dokument i ett annat dokument.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->MoveToDocumentEnd();
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

auto docToInsert = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Formatted elements.docx");

builder->InsertDocument(docToInsert, Aspose::Words::ImportFormatMode::KeepSourceFormatting);
builder->get_Document()->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertDocument.docx");
```

## Se även

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
