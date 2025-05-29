---
title: HtmlSaveOptions.ReplaceBackslashWithYenSign
linktitle: ReplaceBackslashWithYenSign
articleTitle: ReplaceBackslashWithYenSign
second_title: Aspose.Words för .NET
description: Upptäck hur egenskapen HtmlSaveOptions ReplaceBackslashWithYenSign förbättrar din HTML-utdata genom att konvertera bakåtsnedstreck till yen-tecken. Standardvärdet är falskt.
type: docs
weight: 420
url: /sv/net/aspose.words.saving/htmlsaveoptions/replacebackslashwithyensign/
---
## HtmlSaveOptions.ReplaceBackslashWithYenSign property

Anger om bakåtsnedstreck ska ersättas med yen-tecken. Standardvärdet är`falsk` .

```csharp
public bool ReplaceBackslashWithYenSign { get; set; }
```

## Anmärkningar

Som standard härmar Aspose.Words MS Words beteende och ersätter inte omvänt snedstreck med yen-tecken i genererade HTML-dokument. Tidigare versioner av Aspose.Words utförde dock sådana ersättningar i vissa scenarier. Denna flagga möjliggör bakåtkompatibilitet med tidigare versioner av Aspose.Words.

## Exempel

Visar hur man ersätter bakåtsnedstreck med yen-tecken (Html).

```csharp
Document doc = new Document(MyDir + "Korean backslash symbol.docx");

// Som standard härmar Aspose.Words MS Words beteende och ersätter inte omvänt snedstreck med yen-tecken i
// genererade HTML-dokument. Tidigare versioner av Aspose.Words utförde dock sådana ersättningar i vissa fall
// scenarier. Denna flagga möjliggör bakåtkompatibilitet med tidigare versioner av Aspose.Words.
HtmlSaveOptions saveOptions = new HtmlSaveOptions();
saveOptions.ReplaceBackslashWithYenSign = true;

doc.Save(ArtifactsDir + "HtmlSaveOptions.ReplaceBackslashWithYenSign.html", saveOptions);
```

### Se även

* class [HtmlSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
