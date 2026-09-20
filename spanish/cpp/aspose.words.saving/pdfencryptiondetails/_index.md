---
title: "Aspose::Words::Saving::PdfEncryptionDetails class"
linktitle: "PdfEncryptionDetails"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::PdfEncryptionDetails class. Contiene detalles para el cifrado y los permisos de acceso de un documento PDF. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 24000
url: /es/cpp/aspose.words.saving/pdfencryptiondetails/
---
## PdfEncryptionDetails class


Contiene detalles para cifrar y los permisos de acceso de un documento PDF. Para obtener más información, visite el artículo de documentación [Protect or Encrypt a Document](https://docs.aspose.com/words/cpp/protect-or-encrypt-a-document/).

```cpp
class PdfEncryptionDetails : public System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| [get_OwnerPassword](./get_ownerpassword/)() const | Especifica la contraseña del propietario para el documento PDF cifrado. |
| [get_Permissions](./get_permissions/)() const | Especifica las operaciones que se permiten a un usuario en un documento PDF cifrado. El valor predeterminado es [DisallowAll](../pdfpermissions/). |
| [get_UserPassword](./get_userpassword/)() const | Especifica la contraseña de usuario requerida para abrir el documento PDF cifrado. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [PdfEncryptionDetails](./pdfencryptiondetails/)(const System::String\&, const System::String\&) | Inicializa una instancia de esta clase. |
| [PdfEncryptionDetails](./pdfencryptiondetails/)(const System::String\&, const System::String\&, Aspose::Words::Saving::PdfPermissions) | Inicializa una instancia de esta clase. |
| [set_OwnerPassword](./set_ownerpassword/)(const System::String\&) | Método set para [Aspose::Words::Saving::PdfEncryptionDetails::get_OwnerPassword](./get_ownerpassword/). |
| [set_Permissions](./set_permissions/)(Aspose::Words::Saving::PdfPermissions) | Especifica las operaciones que se permiten a un usuario en un documento PDF cifrado. El valor predeterminado es [DisallowAll](../pdfpermissions/). |
| [set_UserPassword](./set_userpassword/)(const System::String\&) | Método set para [Aspose::Words::Saving::PdfEncryptionDetails::get_UserPassword](./get_userpassword/). |
| static [Type](./type/)() |  |
## Ver también

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
