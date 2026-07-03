---
title: Document.ReadabilityStatistics
linktitle: ReadabilityStatistics
articleTitle: ReadabilityStatistics
second_title: Aspose.Words for .NET
description: Analyze Word document readability programmatically. Easily retrieve text difficulty metrics and reading scores using Aspose.Words.
type: docs
weight: 360
url: /net/aspose.words/document/readabilitystatistics/
---
## Document.ReadabilityStatistics property

Provides readability score information for the document.

```csharp
public ReadabilityStatistics ReadabilityStatistics { get; }
```

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

* class [ReadabilityStatistics](../../readabilitystatistics/)
* class [Document](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
