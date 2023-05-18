---
title: Aspose::Words::Saving::PdfEncryptionDetails::get_Permissions method
linktitle: get_Permissions
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::PdfEncryptionDetails::get_Permissions method. Specifies the operations that are allowed to a user on an encrypted PDF document. The default value is DisallowAll in C++.'
type: docs
weight: 4000
url: /cpp/aspose.words.saving/pdfencryptiondetails/get_permissions/
---
## PdfEncryptionDetails::get_Permissions method


Specifies the operations that are allowed to a user on an encrypted PDF document. The default value is [DisallowAll](../../pdfpermissions/).

```cpp
Aspose::Words::Saving::PdfPermissions Aspose::Words::Saving::PdfEncryptionDetails::get_Permissions() const
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
