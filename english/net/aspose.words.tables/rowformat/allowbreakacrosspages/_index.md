---
title: RowFormat.AllowBreakAcrossPages
linktitle: AllowBreakAcrossPages
articleTitle: AllowBreakAcrossPages
second_title: Aspose.Words for .NET
description: Discover the RowFormat AllowBreakAcrossPages property, enable seamless text flow in table rows across page breaks for enhanced readability and presentation.
type: docs
weight: 10
url: /net/aspose.words.tables/rowformat/allowbreakacrosspages/
---
## RowFormat.AllowBreakAcrossPages property

True if the text in a table row is allowed to split across a page break.

```csharp
public bool AllowBreakAcrossPages { get; set; }
```

## Examples

Shows how to disable rows breaking across pages for every row in a table.

```csharp
Document doc = new Document(MyDir + "Table spanning two pages.docx");
Table table = doc.FirstSection.Body.Tables[0];

// Set the "AllowBreakAcrossPages" property to "false" to keep the row
// in one piece if a table spans two pages, which break up along that row.
// If the row is too big to fit in one page, Microsoft Word will push it down to the next page.
// Set the "AllowBreakAcrossPages" property to "true" to allow the row to break up across two pages.
foreach (Row row in table)
    row.RowFormat.AllowBreakAcrossPages = allowBreakAcrossPages;

doc.Save(ArtifactsDir + "Table.AllowBreakAcrossPages.docx");
```

### See Also

* class [RowFormat](../)
* namespace [Aspose.Words.Tables](../../../aspose.words.tables/)
* assembly [Aspose.Words](../../../)
