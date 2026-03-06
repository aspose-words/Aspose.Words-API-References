---
title: JoinRunsOptions Class
linktitle: JoinRunsOptions
articleTitle: JoinRunsOptions
second_title: Aspose.Words for .NET
description: Configure run-merging behavior in Aspose.Words. Control how document runs with similar formatting are combined for cleaner, optimized Word documents.
type: docs
weight: 3770
url: /net/aspose.words/joinrunsoptions/
---
## JoinRunsOptions class

Provides configuration flags for the join runs operation.

```csharp
public class JoinRunsOptions
```

## Constructors

| Name | Description |
| --- | --- |
| [JoinRunsOptions](joinrunsoptions/)() | The default constructor. |

## Properties

| Name | Description |
| --- | --- |
| [IgnoreInsignificant](../../aspose.words/joinrunsoptions/ignoreinsignificant/) { get; set; } | True indicates that the insignificant attributes of all runs will be ignored when joining runs with same formatting. |
| [IgnoreRedundant](../../aspose.words/joinrunsoptions/ignoreredundant/) { get; set; } | True indicates that the redundant attributes of all runs will be ignored when joining runs with same formatting. |
| [IgnoreSpacing](../../aspose.words/joinrunsoptions/ignorespacing/) { get; set; } | True indicates that the spacing attributes of all runs will be ignored when joining runs with same formatting. |

## Examples

Shows how to join runs with the same formatting while ignoring redundant and insignificant attributes.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Create runs with identical visible formatting but some internal differences.
builder.Font.Name = "Arial";
builder.Font.Size = 12;
builder.Write("Hello ");
builder.Write("world");

// Verify runs before join.
Assert.That(doc.FirstSection.Body.FirstParagraph.Runs.Count, Is.EqualTo(2));
Assert.That(doc.FirstSection.Body.FirstParagraph.Runs[0].Text, Is.EqualTo("Hello "));
Assert.That(doc.FirstSection.Body.FirstParagraph.Runs[1].Text, Is.EqualTo("world"));

// Configure options to ignore redundant and insignificant attributes during join.
JoinRunsOptions options = new JoinRunsOptions();
options.IgnoreRedundant = true; // Ignore redundant run properties that don't affect appearance.
options.IgnoreInsignificant = true; // Ignore insignificant differences like whitespace-only runs.

// Join runs that have the same visible formatting using the extended options.
doc.FirstSection.Body.FirstParagraph.JoinRunsWithSameFormatting(options);

// Verify that runs were successfully joined.
Assert.That(doc.FirstSection.Body.FirstParagraph.Runs.Count, Is.EqualTo(1));
Assert.That(doc.FirstSection.Body.FirstParagraph.Runs[0].Text, Is.EqualTo("Hello world"));

doc.Save(ArtifactsDir + "Paragraph.JoinRunsWithSameFormattingWithOptions.docx");
```

### See Also

* namespace [Aspose.Words](../../aspose.words/)
* assembly [Aspose.Words](../../)
