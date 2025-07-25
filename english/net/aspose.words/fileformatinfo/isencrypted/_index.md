---
title: FileFormatInfo.IsEncrypted
linktitle: IsEncrypted
articleTitle: IsEncrypted
second_title: Aspose.Words for .NET
description: Discover if your document is secure with the FileFormatInfo IsEncrypted property—returns true for encrypted files needing a password to access.
type: docs
weight: 40
url: /net/aspose.words/fileformatinfo/isencrypted/
---
## FileFormatInfo.IsEncrypted property

Returns `true` if the document is encrypted and requires a password to open.

```csharp
public bool IsEncrypted { get; }
```

## Remarks

This property exists to help you sort documents that are encrypted from those that are not. If you attempt to load an encrypted document using Aspose.Words without supplying a password an exception will be thrown. You can use this property to detect whether a document requires a password and take some action before loading a document, for example, prompt the user for a password.

## Examples

Shows how to use the FileFormatUtil class to detect the document format and encryption.

```csharp
Document doc = new Document();

// Configure a SaveOptions object to encrypt the document
// with a password when we save it, and then save the document.
OdtSaveOptions saveOptions = new OdtSaveOptions(SaveFormat.Odt);
saveOptions.Password = "MyPassword";

doc.Save(ArtifactsDir + "File.DetectDocumentEncryption.odt", saveOptions);

// Verify the file type of our document, and its encryption status.
FileFormatInfo info = FileFormatUtil.DetectFileFormat(ArtifactsDir + "File.DetectDocumentEncryption.odt");

Assert.That(FileFormatUtil.LoadFormatToExtension(info.LoadFormat), Is.EqualTo(".odt"));
Assert.That(info.IsEncrypted, Is.True);
```

### See Also

* class [FileFormatInfo](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
