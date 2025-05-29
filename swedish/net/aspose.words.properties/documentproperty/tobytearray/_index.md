---
title: DocumentProperty.ToByteArray
linktitle: ToByteArray
articleTitle: ToByteArray
second_title: Aspose.Words för .NET
description: Konvertera DocumentProperty till en byte-array utan ansträngning med ToByteArray-metoden. Effektivisera datahanteringen och förbättra din kodningseffektivitet!
type: docs
weight: 70
url: /sv/net/aspose.words.properties/documentproperty/tobytearray/
---
## DocumentProperty.ToByteArray method

Returnerar egenskapsvärdet som en byte-array.

```csharp
public byte[] ToByteArray()
```

## Anmärkningar

Utlöser ett undantag om egenskapstypen inte ärByteArray.

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

* class [DocumentProperty](../)
* namnutrymme [Aspose.Words.Properties](../../../aspose.words.properties/)
* hopsättning [Aspose.Words](../../../)
