---
title: Aspose::Words::Saving::PdfEncryptionDetails::PdfEncryptionDetails constructor
linktitle: PdfEncryptionDetails
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::PdfEncryptionDetails::PdfEncryptionDetails constructor. Initializes an instance of this class in C++.'
type: docs
weight: 2000
url: /cpp/aspose.words.saving/pdfencryptiondetails/pdfencryptiondetails/
---
## PdfEncryptionDetails::PdfEncryptionDetails(const System::String\&, const System::String\&) constructor


Initializes an instance of this class.

```cpp
Aspose::Words::Saving::PdfEncryptionDetails::PdfEncryptionDetails(const System::String &userPassword, const System::String &ownerPassword)
```

## See Also

* Class [PdfEncryptionDetails](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
## PdfEncryptionDetails::PdfEncryptionDetails(const System::String\&, const System::String\&, Aspose::Words::Saving::PdfPermissions) constructor


Initializes an instance of this class.

```cpp
Aspose::Words::Saving::PdfEncryptionDetails::PdfEncryptionDetails(const System::String &userPassword, const System::String &ownerPassword, Aspose::Words::Saving::PdfPermissions permissions)
```


## Examples



Shows how to set permissions on a saved PDF document. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

builder->Writeln(u"Hello world!");

auto encryptionDetails = MakeObject<PdfEncryptionDetails>(u"password", String::Empty);

// Start by disallowing all permissions.
encryptionDetails->set_Permissions(PdfPermissions::DisallowAll);

// Extend permissions to allow the editing of annotations.
encryptionDetails->set_Permissions(PdfPermissions::ModifyAnnotations | PdfPermissions::DocumentAssembly);

// Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .PDF.
auto saveOptions = MakeObject<PdfSaveOptions>();

// Enable encryption via the "EncryptionDetails" property.
saveOptions->set_EncryptionDetails(encryptionDetails);

// When we open this document, we will need to provide the password before accessing its contents.
doc->Save(ArtifactsDir + u"PdfSaveOptions.EncryptionPermissions.pdf", saveOptions);
```

## See Also

* Enum [PdfPermissions](../../pdfpermissions/)
* Class [PdfEncryptionDetails](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
