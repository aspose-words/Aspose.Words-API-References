---
title: LoadOptions.MswVersion
linktitle: MswVersion
articleTitle: MswVersion
second_title: Aspose.Words för .NET
description: Optimera dokumentinläsningen med LoadOptions MswVersion. Säkerställ kompatibilitet med specifika MS Word-versioner, med Word 2019 som standard för sömlös integration.
type: docs
weight: 100
url: /sv/net/aspose.words.loading/loadoptions/mswversion/
---
## LoadOptions.MswVersion property

Gör det möjligt att ange att dokumentinläsningsprocessen ska matcha en specifik MS Word-version. Standardvärdet ärWord2019

```csharp
public MsWordVersion MswVersion { get; set; }
```

## Anmärkningar

Olika Word-versioner kan hantera vissa aspekter av dokumentinnehåll och formatering något olika under laddningsprocessen, vilket kan resultera i mindre skillnader i dokumentobjektmodellen.

## Exempel

Visar hur man emulerar laddningsproceduren för en specifik Microsoft Word-version vid dokumentladdning.

```csharp
// Som standard laddar Aspose.Words dokument enligt Microsoft Word 2019-specifikationen.
LoadOptions loadOptions = new LoadOptions();

Assert.AreEqual(MsWordVersion.Word2019, loadOptions.MswVersion);

// Standardformateringen för stycke saknas i det här dokumentet.
// Denna standardstil kommer att genereras om när vi laddar dokumentet antingen med Microsoft Word eller Aspose.Words.
loadOptions.MswVersion = MsWordVersion.Word2007;
Document doc = new Document(MyDir + "Document.docx", loadOptions);

// Stilens radavstånd kommer att ha detta värde när det laddas av Microsoft Word 2007-specifikationen.
Assert.AreEqual(12.95d, doc.Styles.DefaultParagraphFormat.LineSpacing, 0.01d);
```

### Se även

* enum [MsWordVersion](../../../aspose.words.settings/mswordversion/)
* class [LoadOptions](../)
* namnutrymme [Aspose.Words.Loading](../../../aspose.words.loading/)
* hopsättning [Aspose.Words](../../../)
