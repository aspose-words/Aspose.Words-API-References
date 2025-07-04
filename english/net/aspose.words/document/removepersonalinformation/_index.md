---
title: Document.RemovePersonalInformation
linktitle: RemovePersonalInformation
articleTitle: RemovePersonalInformation
second_title: Aspose.Words for .NET
description: Ensure privacy with the Document RemovePersonalInformation feature in Word, automatically deleting user data from comments and properties upon saving.
type: docs
weight: 360
url: /net/aspose.words/document/removepersonalinformation/
---
## Document.RemovePersonalInformation property

Gets or sets a flag indicating that Microsoft Word will remove all user information from comments, revisions and document properties upon saving the document.

```csharp
public bool RemovePersonalInformation { get; set; }
```

## Examples

Shows how to enable the removal of personal information during a manual save.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insert some content with personal information.
doc.BuiltInDocumentProperties.Author = "John Doe";
doc.BuiltInDocumentProperties.Company = "Placeholder Inc.";

doc.StartTrackRevisions(doc.BuiltInDocumentProperties.Author, DateTime.Now);
builder.Write("Hello world!");
doc.StopTrackRevisions();

// This flag is equivalent to File -> Options -> Trust Center -> Trust Center Settings... ->
// Privacy Options -> "Remove personal information from file properties on save" in Microsoft Word.
doc.RemovePersonalInformation = saveWithoutPersonalInfo;

// This option will not take effect during a save operation made using Aspose.Words.
// Personal data will be removed from our document with the flag set when we save it manually using Microsoft Word.
doc.Save(ArtifactsDir + "Document.RemovePersonalInformation.docx");
doc = new Document(ArtifactsDir + "Document.RemovePersonalInformation.docx");

Assert.That(doc.RemovePersonalInformation, Is.EqualTo(saveWithoutPersonalInfo));
Assert.That(doc.BuiltInDocumentProperties.Author, Is.EqualTo("John Doe"));
Assert.That(doc.BuiltInDocumentProperties.Company, Is.EqualTo("Placeholder Inc."));
Assert.That(doc.Revisions[0].Author, Is.EqualTo("John Doe"));
```

### See Also

* class [Document](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
