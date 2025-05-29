---
title: MarkdownSaveOptions.ListExportMode
linktitle: ListExportMode
articleTitle: ListExportMode
second_title: Aspose.Words för .NET
description: Upptäck egenskapen ListExportMode i MarkdownSaveOptions, som styr hur listobjekt visas. Optimera dina filer med flexibel MarkdownSyntax!
type: docs
weight: 110
url: /sv/net/aspose.words.saving/markdownsaveoptions/listexportmode/
---
## MarkdownSaveOptions.ListExportMode property

Anger hur listobjekt ska skrivas till utdatafilen. Standardvärdet ärMarkdownSyntax .

```csharp
public MarkdownListExportMode ListExportMode { get; set; }
```

## Anmärkningar

När den här egenskapen är inställd påPlainText alla listetiketter är uppdaterade med[`UpdateListLabels`](../../../aspose.words/document/updatelistlabels/) och exporteras med deras faktiska värden. Sådana listor kan vara inkompatibla med Markdown-formatet och kommer i det här fallet att identifieras som vanlig text vid import.

När den här egenskapen är inställd påMarkdownSyntax, författaren försöker export listobjekt på ett sätt som gör det möjligt att numrera listobjekt i automatiskt läge med Markdown.

## Exempel

Visar hur man listar objekt som kommer att skrivas till markdown-dokumentet.

```csharp
Document doc = new Document(MyDir + "List item.docx");

// Använd MarkdownListExportMode.PlainText eller MarkdownListExportMode.MarkdownSyntax för att exportera listan.
MarkdownSaveOptions options = new MarkdownSaveOptions { ListExportMode = markdownListExportMode };
doc.Save(ArtifactsDir + "MarkdownSaveOptions.ListExportMode.md", options);
```

### Se även

* enum [MarkdownListExportMode](../../markdownlistexportmode/)
* class [MarkdownSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
