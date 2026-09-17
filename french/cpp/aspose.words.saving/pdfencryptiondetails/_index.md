---
title: "Aspose::Words::Saving::PdfEncryptionDetails class"
linktitle: "PdfEncryptionDetails"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::PdfEncryptionDetails class. Contient les détails pour le chiffrement et les autorisations d'accès d'un document PDF. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 24000
url: /fr/cpp/aspose.words.saving/pdfencryptiondetails/
---
## PdfEncryptionDetails class


Contient les détails pour le chiffrement et les autorisations d'accès d'un document PDF. Pour en savoir plus, consultez l'article de documentation [Protect or Encrypt a Document](https://docs.aspose.com/words/cpp/protect-or-encrypt-a-document/).

```cpp
class PdfEncryptionDetails : public System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [get_OwnerPassword](./get_ownerpassword/)() const | Spécifie le mot de passe propriétaire du document PDF chiffré. |
| [get_Permissions](./get_permissions/)() const | Spécifie les opérations autorisées à un utilisateur sur un document PDF chiffré. La valeur par défaut est [DisallowAll](../pdfpermissions/). |
| [get_UserPassword](./get_userpassword/)() const | Spécifie le mot de passe utilisateur requis pour ouvrir le document PDF chiffré. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [PdfEncryptionDetails](./pdfencryptiondetails/)(const System::String\&, const System::String\&) | Initialise une instance de cette classe. |
| [PdfEncryptionDetails](./pdfencryptiondetails/)(const System::String\&, const System::String\&, Aspose::Words::Saving::PdfPermissions) | Initialise une instance de cette classe. |
| [set_OwnerPassword](./set_ownerpassword/)(const System::String\&) | Mutateur pour [Aspose::Words::Saving::PdfEncryptionDetails::get_OwnerPassword](./get_ownerpassword/). |
| [set_Permissions](./set_permissions/)(Aspose::Words::Saving::PdfPermissions) | Spécifie les opérations autorisées à un utilisateur sur un document PDF chiffré. La valeur par défaut est [DisallowAll](../pdfpermissions/). |
| [set_UserPassword](./set_userpassword/)(const System::String\&) | Mutateur pour [Aspose::Words::Saving::PdfEncryptionDetails::get_UserPassword](./get_userpassword/). |
| static [Type](./type/)() |  |
## Voir aussi

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
