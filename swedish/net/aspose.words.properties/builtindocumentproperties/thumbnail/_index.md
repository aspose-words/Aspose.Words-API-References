---
title: BuiltInDocumentProperties.Thumbnail
linktitle: Thumbnail
articleTitle: Thumbnail
second_title: Aspose.Words för .NET
description: Hantera ditt dokuments visuella attraktionskraft med BuiltInDocumentProperties. Hämta eller ställ enkelt in miniatyrbilder för förbättrad presentation och organisation.
type: docs
weight: 310
url: /sv/net/aspose.words.properties/builtindocumentproperties/thumbnail/
---
## BuiltInDocumentProperties.Thumbnail property

Hämtar eller ställer in miniatyrbilden av dokumentet.

```csharp
public byte[] Thumbnail { get; set; }
```

### Undantag

| undantag | skick |
| --- | --- |
| InvalidOperationException | Utlöses om bilden är ogiltig eller om dess format inte stöds för ett specifikt dokumentformat. |

## Anmärkningar

För närvarande används den här egenskapen endast när ett dokument exporteras till ePub, det läses inte från och skrivs till andra dokumentformat.

Bilden i godtyckligt format kan ställas in på den här egenskapen, men formatet kontrolleras under exporten.

Endast gif-, jpeg- och png-bilder kan användas för ePub-publicering.

## Exempel

Visar hur man lägger till en miniatyrbild i ett dokument som vi sparar som en Epub.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Om vi sparar ett dokument, vars "Thumbnail"-egenskap innehåller bilddata som vi har lagt till, som en Epub,
// en läsare som öppnar dokumentet kan visa bilden före den första sidan.
BuiltInDocumentProperties properties = doc.BuiltInDocumentProperties;

byte[] thumbnailBytes = File.ReadAllBytes(ImageDir + "Logo.jpg");
properties.Thumbnail = thumbnailBytes;

doc.Save(ArtifactsDir + "DocumentProperties.Thumbnail.epub");

// Vi kan extrahera en dokumentminiatyrbild och spara den i det lokala filsystemet.
DocumentProperty thumbnail = doc.BuiltInDocumentProperties["Thumbnail"];
File.WriteAllBytes(ArtifactsDir + "DocumentProperties.Thumbnail.gif", thumbnail.ToByteArray());
```

### Se även

* class [BuiltInDocumentProperties](../)
* namnutrymme [Aspose.Words.Properties](../../../aspose.words.properties/)
* hopsättning [Aspose.Words](../../../)
