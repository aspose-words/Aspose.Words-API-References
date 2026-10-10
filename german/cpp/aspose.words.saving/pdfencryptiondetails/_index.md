---
title: "Aspose::Words::Saving::PdfEncryptionDetails Klasse"
linktitle: "PdfEncryptionDetails"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::PdfEncryptionDetails Klasse. Enthält Details zum Verschlüsseln und zu Zugriffsberechtigungen für ein PDF-Dokument. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 24000
url: /de/cpp/aspose.words.saving/pdfencryptiondetails/
---
## PdfEncryptionDetails class


Enthält Details zur Verschlüsselung und zu Zugriffsberechtigungen für ein PDF‑Dokument. Weitere Informationen finden Sie im Dokumentationsartikel [Protect or Encrypt a Document](https://docs.aspose.com/words/cpp/protect-or-encrypt-a-document/).

```cpp
class PdfEncryptionDetails : public System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [get_OwnerPassword](./get_ownerpassword/)() const | Gibt das Besitzerpasswort für das verschlüsselte PDF-Dokument an. |
| [get_Permissions](./get_permissions/)() const | Gibt die Vorgänge an, die einem Benutzer bei einem verschlüsselten PDF-Dokument erlaubt sind. Der Standardwert ist [DisallowAll](../pdfpermissions/). |
| [get_UserPassword](./get_userpassword/)() const | Gibt das Benutzerpasswort an, das zum Öffnen des verschlüsselten PDF-Dokuments erforderlich ist. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [PdfEncryptionDetails](./pdfencryptiondetails/)(const System::String\&, const System::String\&) | Initialisiert eine Instanz dieser Klasse. |
| [PdfEncryptionDetails](./pdfencryptiondetails/)(const System::String\&, const System::String\&, Aspose::Words::Saving::PdfPermissions) | Initialisiert eine Instanz dieser Klasse. |
| [set_OwnerPassword](./set_ownerpassword/)(const System::String\&) | Setter für [Aspose::Words::Saving::PdfEncryptionDetails::get_OwnerPassword](./get_ownerpassword/). |
| [set_Permissions](./set_permissions/)(Aspose::Words::Saving::PdfPermissions) | Gibt die Vorgänge an, die einem Benutzer bei einem verschlüsselten PDF-Dokument erlaubt sind. Der Standardwert ist [DisallowAll](../pdfpermissions/). |
| [set_UserPassword](./set_userpassword/)(const System::String\&) | Setter für [Aspose::Words::Saving::PdfEncryptionDetails::get_UserPassword](./get_userpassword/). |
| static [Type](./type/)() |  |
## Siehe auch

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
