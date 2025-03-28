---
title: Document.ShowSpellingErrors
linktitle: ShowSpellingErrors
articleTitle: ShowSpellingErrors
second_title: Aspose.Words for .NET
description: Control spelling error visibility in your document with the ShowSpellingErrors property. Enhance your editing process and improve document quality.
type: docs
weight: 420
url: /net/aspose.words/document/showspellingerrors/
---
## Document.ShowSpellingErrors property

Specifies whether to display spelling errors in this document.

```csharp
public bool ShowSpellingErrors { get; set; }
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
