---
title: Aspose::Words::Saving::PdfEncryptionDetails::get_UserPassword method
linktitle: get_UserPassword
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::PdfEncryptionDetails::get_UserPassword method. Specifies the user password required for opening the encrypted PDF document in C++.'
type: docs
weight: 5000
url: /cpp/aspose.words.saving/pdfencryptiondetails/get_userpassword/
---
## PdfEncryptionDetails::get_UserPassword method


Specifies the user password required for opening the encrypted PDF document.

```cpp
System::String Aspose::Words::Saving::PdfEncryptionDetails::get_UserPassword() const
```

## Remarks


The user password will be required to open an encrypted PDF document for viewing. The permissions specified in [Permissions](../get_permissions/) will be enforced by the reader software.

The user password can be **null** or empty string, in this case no password will be required from the user when opening the PDF document. The user password cannot be the same as the owner password. 
## See Also

* Class [PdfEncryptionDetails](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
