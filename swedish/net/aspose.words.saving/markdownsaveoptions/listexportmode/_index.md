---
title: MarkdownSaveOptions.ListExportMode
linktitle: ListExportMode
articleTitle: ListExportMode
second_title: Aspose.Words för .NET
description: MarkdownSaveOptions ListExportMode fast egendom. Anger hur listobjekt ska skrivas till utdatafilen. Standardvärdet ärMarkdownSyntax  i C#.
type: docs
weight: 60
url: /sv/net/aspose.words.saving/markdownsaveoptions/listexportmode/
---
## MarkdownSaveOptions.ListExportMode property

Anger hur listobjekt ska skrivas till utdatafilen. Standardvärdet ärMarkdownSyntax .

```csharp
public MarkdownListExportMode ListExportMode { get; set; }
```

## Anmärkningar

När den här egenskapen är inställd påPlainText alla listetiketter är uppdateras med[`UpdateListLabels`](../../../aspose.words/document/updatelistlabels/)och exporteras med sina faktiska värden. Sådana lists kan vara icke-kompatibla med Markdown-format och kommer att kännas igen som vanlig text vid import i detta fall.

När den här egenskapen är inställd påMarkdownSyntax, writer försöker exportera listobjekt på ett sätt som gör det möjligt att numrera listobjekt i automatiskt läge med Markdown.

## Exempel

Visar hur man listar objekt kommer att skrivas till markdown-dokumentet.

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
