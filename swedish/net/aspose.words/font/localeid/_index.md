---
title: Font.LocaleId
second_title: Aspose.Words för .NET API Referens
description: Font fast egendom. Hämtar eller ställer in lokalidentifieraren språket för de formaterade tecknen.
type: docs
weight: 200
url: /sv/net/aspose.words/font/localeid/
---
## Font.LocaleId property

Hämtar eller ställer in lokalidentifieraren (språket) för de formaterade tecknen.

```csharp
public int LocaleId { get; set; }
```

### Anmärkningar

För listan över lokalkoder se https://msdn.microsoft.com/en-us/library/cc233965.aspx

### Exempel

Visar hur man ställer in språket för texten som vi lägger till med en dokumentbyggare.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Om vi ställer in teckensnittets lokalitet till engelska och infogar lite rysk text,
// den engelska stavningskontrollen känner inte igen texten och upptäcker den som ett stavfel.
builder.Font.LocaleId = new CultureInfo("en-US", false).LCID;
builder.Writeln("Привет!");

// Ställ in en matchande plats för texten som vi ska lägga till för att tillämpa lämplig stavningskontroll.
builder.Font.LocaleId = new CultureInfo("ru-RU", false).LCID;
builder.Writeln("Привет!");

doc.Save(ArtifactsDir + "Font.LocaleId.docx");
```

### Se även

* class [Font](../)
* namnutrymme [Aspose.Words](../../font/)
* hopsättning [Aspose.Words](../../../)


