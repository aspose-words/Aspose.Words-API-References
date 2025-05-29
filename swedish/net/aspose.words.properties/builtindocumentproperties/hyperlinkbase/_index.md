---
title: BuiltInDocumentProperties.HyperlinkBase
linktitle: HyperlinkBase
articleTitle: HyperlinkBase
second_title: Aspose.Words för .NET
description: Upptäck egenskapen BuiltInDocumentProperties HyperlinkBase för att optimera relativa hyperlänkar i dina dokument för sömlös navigering och förbättrad användarupplevelse.
type: docs
weight: 120
url: /sv/net/aspose.words.properties/builtindocumentproperties/hyperlinkbase/
---
## BuiltInDocumentProperties.HyperlinkBase property

Anger bassträngen som används för att utvärdera relativa hyperlänkar i detta dokument.

```csharp
public string HyperlinkBase { get; set; }
```

## Anmärkningar

Aspose.Words använder inte den här egenskapen.

## Exempel

Visar hur man lagrar basdelen av en hyperlänk i dokumentets egenskaper.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga en relativ hyperlänk till ett dokument i det lokala filsystemet med namnet "Document.docx".
// Genom att klicka på länken i Microsoft Word öppnas det angivna dokumentet, om det är tillgängligt.
builder.InsertHyperlink("Relative hyperlink", "Document.docx", false);

// Denna länk är relativ. Om det inte finns någon "Document.docx" i samma mapp
// eftersom dokumentet som innehåller den här länken, kommer länken att vara trasig.
Assert.False(File.Exists(ArtifactsDir + "Document.docx"));
doc.Save(ArtifactsDir + "DocumentProperties.HyperlinkBase.BrokenLink.docx");

// Dokumentet vi försöker länka till finns i en annan katalog än den vi planerar att spara dokumentet i.
 // Vi skulle kunna fixa den här typen av länkar genom att lägga till ett absolut filnamn i var och en.
// Alternativt kan vi tillhandahålla en baslänk som varje hyperlänk har ett relativt filnamn
 // kommer att läggas till i sin länk när vi klickar på den.
BuiltInDocumentProperties properties = doc.BuiltInDocumentProperties;
properties.HyperlinkBase = MyDir;

Assert.True(File.Exists(properties.HyperlinkBase + ((FieldHyperlink)doc.Range.Fields[0]).Address));

doc.Save(ArtifactsDir + "DocumentProperties.HyperlinkBase.WorkingLink.docx");
```

### Se även

* class [BuiltInDocumentProperties](../)
* namnutrymme [Aspose.Words.Properties](../../../aspose.words.properties/)
* hopsättning [Aspose.Words](../../../)
