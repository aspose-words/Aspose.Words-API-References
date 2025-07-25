---
title: Document.Compliance
linktitle: Compliance
articleTitle: Compliance
second_title: Aspose.Words for .NET
description: Ensure your OOXML documents meet compliance standards effortlessly. Our tool analyzes content to verify OOXML compliance, enhancing document integrity.
type: docs
weight: 70
url: /net/aspose.words/document/compliance/
---
## Document.Compliance property

Gets the OOXML compliance version determined from the loaded document content. Makes sense only for OOXML documents.

```csharp
public OoxmlCompliance Compliance { get; }
```

## Remarks

If you created a new blank document or load non OOXML document returns the Ecma376_2006 value.

## Examples

Shows how to read a loaded document's Open Office XML compliance version.

```csharp
// The compliance version varies between documents created by different versions of Microsoft Word.
Document doc = new Document(MyDir + "Document.doc");
Assert.That(OoxmlCompliance.Ecma376_2006, Is.EqualTo(doc.Compliance));

doc = new Document(MyDir + "Document.docx");
Assert.That(OoxmlCompliance.Iso29500_2008_Transitional, Is.EqualTo(doc.Compliance));
```

### See Also

* enum [OoxmlCompliance](../../../aspose.words.saving/ooxmlcompliance/)
* class [Document](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
