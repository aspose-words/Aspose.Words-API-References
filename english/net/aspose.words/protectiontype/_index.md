---
title: ProtectionType Enum
linktitle: ProtectionType
articleTitle: ProtectionType
second_title: Aspose.Words for .NET
description: Discover Aspose.Words.ProtectionType enum for robust document security. Enhance your documents with customizable protection options today!
type: docs
weight: 5240
url: /net/aspose.words/protectiontype/
---
## ProtectionType enumeration

Protection type for a document.

```csharp
public enum ProtectionType
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| AllowOnlyComments | `1` | User can only modify comments in the document. |
| AllowOnlyFormFields | `2` | User can only enter data in the form fields in the document. |
| AllowOnlyRevisions | `0` | User can only add revision marks to the document. |
| ReadOnly | `3` | No changes are allowed to the document. Available since Microsoft Word 2003. |
| NoProtection | `-1` | The document is not protected. |

## Examples

Shows how to turn off protection for a section.

```csharp
Document doc = new Document();

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Section 1. Hello world!");
builder.InsertBreak(BreakType.SectionBreakNewPage);

builder.Writeln("Section 2. Hello again!");
builder.Write("Please enter text here: ");
builder.InsertTextInput("TextInput1", TextFormFieldType.Regular, "", "Placeholder text", 0);

// Apply write protection to every section in the document.
doc.Protect(ProtectionType.AllowOnlyFormFields);

// Turn off write protection for the first section.
doc.Sections[0].ProtectedForForms = false;

// In this output document, we will be able to edit the first section freely,
// and we will only be able to edit the contents of the form field in the second section.
doc.Save(ArtifactsDir + "Section.Protect.docx");
```

### See Also

* namespace [Aspose.Words](../../aspose.words/)
* assembly [Aspose.Words](../../)
