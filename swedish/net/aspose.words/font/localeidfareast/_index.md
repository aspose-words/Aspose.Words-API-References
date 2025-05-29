---
title: Font.LocaleIdFarEast
linktitle: LocaleIdFarEast
articleTitle: LocaleIdFarEast
second_title: Aspose.Words för .NET
description: Upptäck egenskapen Font LocaleIdFarEast för att enkelt hantera språkidentifierare för formaterade asiatiska tecken och förbättra dina flerspråkiga applikationer.
type: docs
weight: 220
url: /sv/net/aspose.words/font/localeidfareast/
---
## Font.LocaleIdFarEast property

Hämtar eller anger språkidentifieraren för de formaterade asiatiska tecknen.

```csharp
public int LocaleIdFarEast { get; set; }
```

## Anmärkningar

För en lista över språkidentifierare, se https://msdn.microsoft.com/en-us/library/cc233965.aspx

## Exempel

Visar hur man infogar och formaterar text på ett språk från Fjärran Östen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ange teckensnittsinställningar som dokumentbyggaren ska tillämpa på all text som infogas.
builder.Font.Name = "Courier New";
builder.Font.LocaleId = new CultureInfo("en-US", false).LCID;

// Namnge motsvarigheter till "Fjärran Östen" för vårt teckensnitt och vår språkinställning.
// Om byggaren infogar asiatiska tecken med denna teckensnittskonfiguration, så kommer varje körning som innehåller
// dessa tecken kommer att visas med teckensnittet/språket "FarEast" istället för standardinställningen.
// Detta kan vara användbart när ett västerländskt typsnitt inte har idealiska representationer för asiatiska tecken.
builder.Font.NameFarEast = "SimSun";
builder.Font.LocaleIdFarEast = new CultureInfo("zh-CN", false).LCID;

// Den här texten kommer att visas med standardteckensnittet/språket.
builder.Writeln("Hello world!");

// Eftersom dessa är asiatiska tecken kommer den här körningen att använda våra motsvarigheter för teckensnitt/språk "Fjärran Östen".
builder.Writeln("你好世界");

doc.Save(ArtifactsDir + "Font.FarEast.docx");
```

### Se även

* class [Font](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
