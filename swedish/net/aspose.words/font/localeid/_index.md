---
title: Font.LocaleId
linktitle: LocaleId
articleTitle: LocaleId
second_title: Aspose.Words för .NET
description: Upptäck hur egenskapen Font LocaleId förbättrar din textformatering genom att hantera språkidentifierare för olika teckenspråk. Förbättra din kodning idag!
type: docs
weight: 200
url: /sv/net/aspose.words/font/localeid/
---
## Font.LocaleId property

Hämtar eller anger språkidentifieraren för de formaterade tecknen.

```csharp
public int LocaleId { get; set; }
```

## Anmärkningar

För en lista över språkidentifierare, se https://msdn.microsoft.com/en-us/library/cc233965.aspx

## Exempel

Visar hur man ställer in språkinställningarna för texten som vi lägger till med en dokumentbyggare.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Om vi ställer in teckensnittets språkinställning till engelska och infogar rysk text,
// stavningskontrollen för engelska språkinställningar kommer inte att känna igen texten och upptäcka den som ett stavfel.
builder.Font.LocaleId = new CultureInfo("en-US", false).LCID;
builder.Writeln("Привет!");

// Ange en matchande språkinställning för texten som vi ska lägga till för att tillämpa lämplig stavningskontroll.
builder.Font.LocaleId = new CultureInfo("ru-RU", false).LCID;
builder.Writeln("Привет!");

doc.Save(ArtifactsDir + "Font.LocaleId.docx");
```

### Se även

* class [Font](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
