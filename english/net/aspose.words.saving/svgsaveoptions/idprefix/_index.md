---
title: SvgSaveOptions.IdPrefix
linktitle: IdPrefix
articleTitle: IdPrefix
second_title: Aspose.Words for .NET
description: SvgSaveOptions IdPrefix property. Specifies a prefix that is prepended to all generated element IDs in the output document. Default value is null and no prefix is prepended in C#.
type: docs
weight: 40
url: /net/aspose.words.saving/svgsaveoptions/idprefix/
---
## SvgSaveOptions.IdPrefix property

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

Shows how to add a prefix that is prepended to all generated element IDs (svg).

```csharp
Document doc = new Document(MyDir + "Id prefix.docx");

SvgSaveOptions saveOptions = new SvgSaveOptions();
saveOptions.IdPrefix = "pfx1_";

doc.Save(ArtifactsDir + "SvgSaveOptions.IdPrefixSvg.html", saveOptions);
```

### See Also

* class [SvgSaveOptions](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)
