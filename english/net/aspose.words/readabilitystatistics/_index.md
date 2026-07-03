---
title: ReadabilityStatistics Class
linktitle: ReadabilityStatistics
articleTitle: ReadabilityStatistics
second_title: Aspose.Words for .NET
description: API class to measure text complexity. Get detailed grade levels and readability statistics for Word documents automatically.
type: docs
weight: 5320
url: /net/aspose.words/readabilitystatistics/
---
## ReadabilityStatistics class

Provides information about document readability score.

```csharp
public class ReadabilityStatistics
```

## Properties

| Name | Description |
| --- | --- |
| [FleschKincaidGradeLevel](../../aspose.words/readabilitystatistics/fleschkincaidgradelevel/) { get; } | Flesch-Kincaid Grade Level score. |
| [FleschReadingEasy](../../aspose.words/readabilitystatistics/fleschreadingeasy/) { get; } | Flesch Reading Easy score. |

## Examples

Shows how to calculate and display the Flesch reading scores for a document.

```csharp
Document doc = new Document();

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("The implementation of artificial intelligence algorithms requires a comprehensive understanding of machine learning methodologies and statistical analysis techniques.");
builder.Writeln("Furthermore, the integration of neural networks into existing software architectures presents significant challenges for developers.");
builder.Writeln("This document serves as an illustrative example for calculating readability metrics using the Flesch reading ease formula.");

// Calculate readability statistics.
ReadabilityStatistics stats = doc.ReadabilityStatistics;
// Verify that the scores are within expected valid ranges.
Assert.That(stats.FleschReadingEasy, Is.GreaterThanOrEqualTo(0).And.LessThanOrEqualTo(190));
Assert.That(stats.FleschKincaidGradeLevel, Is.LessThanOrEqualTo(0));
```

### See Also

* namespace [Aspose.Words](../../aspose.words/)
* assembly [Aspose.Words](../../)
