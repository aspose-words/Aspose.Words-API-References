---
title: Font.LocaleIdFarEast
second_title: Aspose.Words för .NET API Referens
description: Font fast egendom. Hämtar eller ställer in lokalidentifieraren språket för de formaterade asiatiska tecknen.
type: docs
weight: 220
url: /sv/net/aspose.words/font/localeidfareast/
---
## Font.LocaleIdFarEast property

Hämtar eller ställer in lokalidentifieraren (språket) för de formaterade asiatiska tecknen.

```csharp
public int LocaleIdFarEast { get; set; }
```

### Anmärkningar

För listan över lokalkoder se https://msdn.microsoft.com/en-us/library/cc233965.aspx

### Exempel

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

* class [Font](../)
* namnutrymme [Aspose.Words](../../font/)
* hopsättning [Aspose.Words](../../../)


