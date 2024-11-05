---
title: Granularity Enum
linktitle: Granularity
articleTitle: Granularity
second_title: Aspose.Words for .NET
description: Aspose.Words.Comparing.Granularity enum. Specifies the granularity of changes to track when comparing two documents in C#.
type: docs
weight: 460
url: /net/aspose.words.comparing/granularity/
---
## Granularity enumeration

Specifies the granularity of changes to track when comparing two documents.

```csharp
public enum Granularity
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| CharLevel | `0` | Specifies changes at the character level. |
| WordLevel | `1` | Specifies changes at the word level. |

## Examples

Shows to specify a granularity while comparing documents.

```csharp
Document docA = new Document();
DocumentBuilder builderA = new DocumentBuilder(docA);
builderA.Writeln("Alpha Lorem ipsum dolor sit amet, consectetur adipiscing elit");

Document docB = new Document();
DocumentBuilder builderB = new DocumentBuilder(docB);
builderB.Writeln("Lorems ipsum dolor sit amet consectetur - \"adipiscing\" elit");

// Specify whether changes are tracking
// by character ('Granularity.CharLevel'), or by word ('Granularity.WordLevel').
Aspose.Words.Comparing.CompareOptions compareOptions = new Aspose.Words.Comparing.CompareOptions();
compareOptions.Granularity = granularity;

docA.Compare(docB, "author", DateTime.Now, compareOptions);

// The first document's collection of revision groups contains all the differences between documents.
RevisionGroupCollection groups = docA.Revisions.Groups;
Assert.AreEqual(5, groups.Count);
```

### See Also

* namespace [Aspose.Words.Comparing](../../aspose.words.comparing/)
* assembly [Aspose.Words](../../)
