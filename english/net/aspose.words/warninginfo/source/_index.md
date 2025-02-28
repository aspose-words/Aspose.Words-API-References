---
title: WarningInfo.Source
linktitle: Source
articleTitle: Source
second_title: Aspose.Words for .NET
description: Discover the WarningInfo Source property that reveals the origin of warnings, enhancing your application's reliability and user experience.
type: docs
weight: 20
url: /net/aspose.words/warninginfo/source/
---
## WarningInfo.Source property

Returns the source of the warning.

```csharp
public WarningSource Source { get; }
```

## Examples

Shows how to work with the warning source.

```csharp
Document doc = new Document(MyDir + "Emphases markdown warning.docx");

WarningInfoCollection warnings = new WarningInfoCollection();
doc.WarningCallback = warnings;
doc.Save(ArtifactsDir + "DocumentBuilder.EmphasesWarningSourceMarkdown.md");

foreach (WarningInfo warningInfo in warnings)
{
    if (warningInfo.Source == WarningSource.Markdown)
        Assert.AreEqual("The (*, 0:11) cannot be properly written into Markdown.", warningInfo.Description);
}
```

### See Also

* enum [WarningSource](../../warningsource/)
* class [WarningInfo](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
