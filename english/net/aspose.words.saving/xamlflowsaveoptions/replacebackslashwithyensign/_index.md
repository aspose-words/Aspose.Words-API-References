---
title: XamlFlowSaveOptions.ReplaceBackslashWithYenSign
linktitle: ReplaceBackslashWithYenSign
articleTitle: ReplaceBackslashWithYenSign
second_title: Aspose.Words for .NET
description: Discover how XamlFlowSaveOptions' ReplaceBackslashWithYenSign property enhances your data formatting by converting backslashes to yen signs. Default: false.
type: docs
weight: 50
url: /net/aspose.words.saving/xamlflowsaveoptions/replacebackslashwithyensign/
---
## XamlFlowSaveOptions.ReplaceBackslashWithYenSign property

Specifies whether backslash characters should be replaced with yen signs. Default value is `false`.

```csharp
public bool ReplaceBackslashWithYenSign { get; set; }
```

## Remarks

By default, Aspose.Words mimics MS Word's behavior and doesn't replace backslash characters with yen signs in generated XAML documents. However, previous versions of Aspose.Words performed such replacements in certain scenarios. This flag enables backward compatibility with previous versions of Aspose.Words.

## Examples

Shows how to replace backslash characters with yen signs (Xaml).

```csharp
Document doc = new Document(MyDir + "Korean backslash symbol.docx");

// By default, Aspose.Words mimics MS Word's behavior and doesn't replace backslash characters with yen signs in
// generated HTML documents. However, previous versions of Aspose.Words performed such replacements in certain
// scenarios. This flag enables backward compatibility with previous versions of Aspose.Words.
XamlFlowSaveOptions saveOptions = new XamlFlowSaveOptions();
saveOptions.ReplaceBackslashWithYenSign = true;

doc.Save(ArtifactsDir + "HtmlSaveOptions.ReplaceBackslashWithYenSign.xaml", saveOptions);
```

### See Also

* class [XamlFlowSaveOptions](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)
