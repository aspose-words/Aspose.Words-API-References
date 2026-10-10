---
title: "Aspose::Words::Saving::PdfEncryptionDetails class"
linktitle: "PdfEncryptionDetails"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::PdfEncryptionDetails class. Contiene i dettagli per la crittografia e le autorizzazioni di accesso di un documento PDF. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 24000
url: /it/cpp/aspose.words.saving/pdfencryptiondetails/
---
## PdfEncryptionDetails class


Contiene i dettagli per la crittografia e le autorizzazioni di accesso per un documento PDF. Per saperne di più, visita l'articolo di documentazione [Protect or Encrypt a Document](https://docs.aspose.com/words/cpp/protect-or-encrypt-a-document/).

```cpp
class PdfEncryptionDetails : public System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [get_OwnerPassword](./get_ownerpassword/)() const | Specifica la password del proprietario per il documento PDF crittografato. |
| [get_Permissions](./get_permissions/)() const | Specifica le operazioni consentite a un utente su un documento PDF crittografato. Il valore predefinito è [DisallowAll](../pdfpermissions/). |
| [get_UserPassword](./get_userpassword/)() const | Specifica la password utente necessaria per aprire il documento PDF crittografato. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [PdfEncryptionDetails](./pdfencryptiondetails/)(const System::String\&, const System::String\&) | Inizializza un'istanza di questa classe. |
| [PdfEncryptionDetails](./pdfencryptiondetails/)(const System::String\&, const System::String\&, Aspose::Words::Saving::PdfPermissions) | Inizializza un'istanza di questa classe. |
| [set_OwnerPassword](./set_ownerpassword/)(const System::String\&) | Impostatore per [Aspose::Words::Saving::PdfEncryptionDetails::get_OwnerPassword](./get_ownerpassword/). |
| [set_Permissions](./set_permissions/)(Aspose::Words::Saving::PdfPermissions) | Specifica le operazioni consentite a un utente su un documento PDF crittografato. Il valore predefinito è [DisallowAll](../pdfpermissions/). |
| [set_UserPassword](./set_userpassword/)(const System::String\&) | Impostatore per [Aspose::Words::Saving::PdfEncryptionDetails::get_UserPassword](./get_userpassword/). |
| static [Type](./type/)() |  |
## Vedi anche

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
