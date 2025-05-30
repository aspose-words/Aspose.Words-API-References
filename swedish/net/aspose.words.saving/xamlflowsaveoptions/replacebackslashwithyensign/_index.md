---
title: XamlFlowSaveOptions.ReplaceBackslashWithYenSign
linktitle: ReplaceBackslashWithYenSign
articleTitle: ReplaceBackslashWithYenSign
second_title: Aspose.Words för .NET
description: Upptäck hur XamlFlowSaveOptions egenskap ReplaceBackslashWithYenSign förbättrar din dataformatering genom att konvertera bakåtsnedstreck till yen-tecken. Standardvärde falskt.
type: docs
weight: 50
url: /sv/net/aspose.words.saving/xamlflowsaveoptions/replacebackslashwithyensign/
---
## XamlFlowSaveOptions.ReplaceBackslashWithYenSign property

Anger om bakåtsnedstreck ska ersättas med yen-tecken. Standardvärdet är`falsk` .

```csharp
public bool ReplaceBackslashWithYenSign { get; set; }
```

## Anmärkningar

Som standard härmar Aspose.Words MS Words beteende och ersätter inte omvänt snedstreck med yen-tecken i genererade XAML-dokument. Tidigare versioner av Aspose.Words utförde dock sådana ersättningar i vissa scenarier. Denna flagga möjliggör bakåtkompatibilitet med tidigare versioner av Aspose.Words.

## Exempel

Visar hur man ersätter omvänt snedstreck med yen-tecken (Xaml).

```csharp
Document doc = new Document(MyDir + "Korean backslash symbol.docx");

// Som standard härmar Aspose.Words MS Words beteende och ersätter inte omvänt snedstreck med yen-tecken i
// genererade HTML-dokument. Tidigare versioner av Aspose.Words utförde dock sådana ersättningar i vissa fall
// scenarier. Denna flagga möjliggör bakåtkompatibilitet med tidigare versioner av Aspose.Words.
XamlFlowSaveOptions saveOptions = new XamlFlowSaveOptions();
saveOptions.ReplaceBackslashWithYenSign = true;

doc.Save(ArtifactsDir + "HtmlSaveOptions.ReplaceBackslashWithYenSign.xaml", saveOptions);
```

### Se även

* class [XamlFlowSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
