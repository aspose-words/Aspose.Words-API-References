---
title: HtmlFixedSaveOptions.IdPrefix
linktitle: IdPrefix
articleTitle: IdPrefix
second_title: Aspose.Words for .NET
description: Discover the HtmlFixedSaveOptions IdPrefix property to customize element IDs in your documents. Enhance organization with tailored prefixes for better output!
type: docs
weight: 100
url: /net/aspose.words.saving/htmlfixedsaveoptions/idprefix/
---
## HtmlFixedSaveOptions.IdPrefix property

Specifies a prefix that is prepended to all generated element IDs in the output document. Default value is null and no prefix is prepended.

```csharp
public string IdPrefix { get; set; }
```

### Exceptions

| exception | condition |
| --- | --- |
| ArgumentException | The value does not meet the requirements specified above. |

## Remarks

If the prefix is specified, it can contain only letters, digits, underscores, and hyphens, and must start with a letter.

## Examples

Shows how to add a prefix that is prepended to all generated element IDs.

```csharp
Document doc = new Document(MyDir + "Id prefix.docx");

HtmlFixedSaveOptions saveOptions = new HtmlFixedSaveOptions();
saveOptions.IdPrefix = "pfx1_";

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.IdPrefix.html", saveOptions);
```

### See Also

* class [HtmlFixedSaveOptions](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)
