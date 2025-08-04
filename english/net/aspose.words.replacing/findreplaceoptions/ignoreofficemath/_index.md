---
title: FindReplaceOptions.IgnoreOfficeMath
linktitle: IgnoreOfficeMath
articleTitle: IgnoreOfficeMath
second_title: Aspose.Words for .NET
description: Skip OfficeMath text during find-and-replace operations with IgnoreOfficeMath to simplify content updates.
type: docs
weight: 110
url: /net/aspose.words.replacing/findreplaceoptions/ignoreofficemath/
---
## FindReplaceOptions.IgnoreOfficeMath property

Gets or sets a boolean value indicating either to ignore text inside OfficeMath/&gt;. The default value is `true`.

```csharp
public bool IgnoreOfficeMath { get; set; }
```

## Examples

Shows how to find and replace text within OfficeMath.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

Assert.That(doc.FirstSection.Body.FirstParagraph.GetText().Trim(), Is.EqualTo("i+b-c≥iM+bM-cM"));

FindReplaceOptions options = new FindReplaceOptions();
options.IgnoreOfficeMath = isIgnoreOfficeMath;
doc.Range.Replace("b", "x", options);

if (isIgnoreOfficeMath)
    Assert.That(doc.FirstSection.Body.FirstParagraph.GetText().Trim(), Is.EqualTo("i+b-c≥iM+bM-cM"));
else
    Assert.That(doc.FirstSection.Body.FirstParagraph.GetText().Trim(), Is.EqualTo("i+x-c≥iM+xM-cM"));
```

### See Also

* class [FindReplaceOptions](../)
* namespace [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* assembly [Aspose.Words](../../../)
