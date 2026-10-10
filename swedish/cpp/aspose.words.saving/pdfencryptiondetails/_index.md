---
title: "Aspose::Words::Saving::PdfEncryptionDetails klass"
linktitle: "PdfEncryptionDetails"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::PdfEncryptionDetails klass. Innehåller detaljer för kryptering och åtkomstbehörigheter för ett PDF-dokument. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 24000
url: /sv/cpp/aspose.words.saving/pdfencryptiondetails/
---
## PdfEncryptionDetails class


Innehåller detaljer för kryptering och åtkomstbehörigheter för ett PDF-dokument. För att lära dig mer, besök dokumentationsartikeln [Protect or Encrypt a Document](https://docs.aspose.com/words/cpp/protect-or-encrypt-a-document/).

```cpp
class PdfEncryptionDetails : public System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [get_OwnerPassword](./get_ownerpassword/)() const | Anger ägarlösenordet för det krypterade PDF-dokumentet. |
| [get_Permissions](./get_permissions/)() const | Anger de operationer som är tillåtna för en användare på ett krypterat PDF-dokument. Standardvärdet är [DisallowAll](../pdfpermissions/). |
| [get_UserPassword](./get_userpassword/)() const | Anger användarlösenordet som krävs för att öppna det krypterade PDF-dokumentet. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [PdfEncryptionDetails](./pdfencryptiondetails/)(const System::String\&, const System::String\&) | Initierar en instans av denna klass. |
| [PdfEncryptionDetails](./pdfencryptiondetails/)(const System::String\&, const System::String\&, Aspose::Words::Saving::PdfPermissions) | Initierar en instans av denna klass. |
| [set_OwnerPassword](./set_ownerpassword/)(const System::String\&) | Sättare för [Aspose::Words::Saving::PdfEncryptionDetails::get_OwnerPassword](./get_ownerpassword/). |
| [set_Permissions](./set_permissions/)(Aspose::Words::Saving::PdfPermissions) | Anger de operationer som är tillåtna för en användare på ett krypterat PDF-dokument. Standardvärdet är [DisallowAll](../pdfpermissions/). |
| [set_UserPassword](./set_userpassword/)(const System::String\&) | Sättare för [Aspose::Words::Saving::PdfEncryptionDetails::get_UserPassword](./get_userpassword/). |
| static [Type](./type/)() |  |
## Se även

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
