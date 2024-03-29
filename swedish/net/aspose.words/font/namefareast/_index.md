---
title: Font.NameFarEast
linktitle: NameFarEast
articleTitle: NameFarEast
second_title: Aspose.Words för .NET
description: Font NameFarEast fast egendom. Returnerar eller ställer in ett östasiatiskt teckensnittsnamn i C#.
type: docs
weight: 260
url: /sv/net/aspose.words/font/namefareast/
---
## Font.NameFarEast property

Returnerar eller ställer in ett östasiatiskt teckensnittsnamn.

```csharp
public string NameFarEast { get; set; }
```

## Exempel

Visar hur man infogar och formaterar text på ett språk i Fjärran Östern.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ange teckensnittsinställningar som dokumentbyggaren kommer att tillämpa på all text som den infogar.
builder.Font.Name = "Courier New";
builder.Font.LocaleId = new CultureInfo("en-US", false).LCID;

// Namnge "FarEast"-motsvarigheter för vårt teckensnitt och språk.
// Om byggaren infogar asiatiska tecken med den här teckensnittskonfigurationen, så kommer varje körning som innehåller
// dessa tecken kommer att visa dem med "FarEast" font/locale istället för standard.
// Detta kan vara användbart när ett västerländskt teckensnitt inte har idealiska representationer för asiatiska tecken.
builder.Font.NameFarEast = "SimSun";
builder.Font.LocaleIdFarEast = new CultureInfo("zh-CN", false).LCID;

// Den här texten kommer att visas i standardfont/locale.
builder.Writeln("Hello world!");

// Eftersom dessa är asiatiska tecken, kommer denna körning att tillämpa våra "Far East" teckensnitt/lokala motsvarigheter.
builder.Writeln("你好世界");

doc.Save(ArtifactsDir + "Font.FarEast.docx");
```

### Se även

* property [Name](../name/)
* class [Font](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
