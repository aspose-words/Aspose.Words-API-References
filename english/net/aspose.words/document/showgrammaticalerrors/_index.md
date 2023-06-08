---
title: Document.ShowGrammaticalErrors
linktitle: ShowGrammaticalErrors
articleTitle: ShowGrammaticalErrors
second_title: Aspose.Words for .NET
description: Document ShowGrammaticalErrors property. Specifies whether to display grammar errors in this document in C#.
type: docs
weight: 390
url: /net/aspose.words/document/showgrammaticalerrors/
---
## Document.ShowGrammaticalErrors property

Specifies whether to display grammar errors in this document.

```csharp
public bool ShowGrammaticalErrors { get; set; }
```

## Examples

Shows how to show/hide errors in the document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insert two sentences with mistakes that would be picked up
// by the spelling and grammar checkers in Microsoft Word.
builder.Writeln("There is a speling error in this sentence.");
builder.Writeln("Their is a grammatical error in this sentence.");

// If these options are enabled, then spelling errors will be underlined
// in the output document by a jagged red line, and a double blue line will highlight grammatical mistakes.
doc.ShowGrammaticalErrors = showErrors;
doc.ShowSpellingErrors = showErrors;

doc.Save(ArtifactsDir + "Document.SpellingAndGrammarErrors.docx");
```

### See Also

* class [Document](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
