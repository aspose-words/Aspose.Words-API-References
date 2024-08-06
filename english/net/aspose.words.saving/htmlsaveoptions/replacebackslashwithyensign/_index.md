---
title: HtmlSaveOptions.ReplaceBackslashWithYenSign
linktitle: ReplaceBackslashWithYenSign
articleTitle: ReplaceBackslashWithYenSign
second_title: Aspose.Words for .NET
description: HtmlSaveOptions ReplaceBackslashWithYenSign property. Specifies whether backslash characters should be replaced with yen signs. Default value is false in C#.
type: docs
weight: 410
url: /net/aspose.words.saving/htmlsaveoptions/replacebackslashwithyensign/
---
## HtmlSaveOptions.ReplaceBackslashWithYenSign property

Specifies whether backslash characters should be replaced with yen signs. Default value is `false`.

```csharp
public bool ReplaceBackslashWithYenSign { get; set; }
```

## Remarks

By default, Aspose.Words mimics MS Word's behavior and doesn't replace backslash characters with yen signs in generated HTML documents. However, previous versions of Aspose.Words performed such replacements in certain scenarios. This flag enables backward compatibility with previous versions of Aspose.Words.

## Examples

Shows how to replace backslash characters with yen signs (Html).

```csharp
Document doc = new Document(MyDir + "Korean backslash symbol.docx");

// By default, Aspose.Words mimics MS Word's behavior and doesn't replace backslash characters with yen signs in
// generated HTML documents. However, previous versions of Aspose.Words performed such replacements in certain
// scenarios. This flag enables backward compatibility with previous versions of Aspose.Words.
HtmlSaveOptions saveOptions = new HtmlSaveOptions();
saveOptions.ReplaceBackslashWithYenSign = true;

doc.Save(ArtifactsDir + "HtmlSaveOptions.ReplaceBackslashWithYenSign.html", saveOptions);
```

### See Also

* class [HtmlSaveOptions](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)
