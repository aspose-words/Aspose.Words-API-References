---
title: Document.GrammarChecked
linktitle: GrammarChecked
articleTitle: GrammarChecked
second_title: Aspose.Words for .NET
description: Document GrammarChecked property. Returns true if the document has been checked for grammar in C#.
type: docs
weight: 180
url: /net/aspose.words/document/grammarchecked/
---
## Document.GrammarChecked property

Returns `true` if the document has been checked for grammar.

```csharp
public bool GrammarChecked { get; set; }
```

## Remarks

To recheck the grammar in the document, set this property to `false`.

## Examples

Shows how to set spelling or grammar verifying.

```csharp
Document doc = new Document();

// The string with spelling errors.
doc.FirstSection.Body.FirstParagraph.Runs.Add(new Run(doc, "The speeling in this documentz is all broked."));

// Spelling/Grammar check start if we set properties to false. 
// We can see all errors in Microsoft Word via Review -> Spelling & Grammar.
// Note that Microsoft Word does not start grammar/spell check automatically for DOC and RTF document format.
doc.SpellingChecked = checkSpellingGrammar;
doc.GrammarChecked = checkSpellingGrammar;

doc.Save(ArtifactsDir + "Document.SpellingOrGrammar.docx");
```

### See Also

* class [Document](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
