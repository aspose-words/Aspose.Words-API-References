---
title: "Aspose::Words::Fields::FieldUserAddress::get_UserAddress‑Methode"
linktitle: "get_UserAddress"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fields::FieldUserAddress::get_UserAddress‑Methode. Liest oder setzt die aktuelle Postadresse des Benutzers in C++."
type: docs
weight: 2000
url: /de/cpp/aspose.words.fields/fielduseraddress/get_useraddress/
---
## FieldUserAddress::get_UserAddress method


Liest oder setzt die Postadresse des aktuellen Benutzers.

```cpp
System::String Aspose::Words::Fields::FieldUserAddress::get_UserAddress()
```


## Beispiele



Zeigt, wie das USERADDRESS-Feld verwendet wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Erstellen Sie ein UserInformation-Objekt und setzen Sie es als Quelle für Benutzerinformationen für alle Felder, die wir erstellen.
auto userInformation = System::MakeObject<Aspose::Words::Fields::UserInformation>();
userInformation->set_Address(u"123 Main Street");
doc->get_FieldOptions()->set_CurrentUser(userInformation);

// Erstellen Sie ein USERADDRESS-Feld, um die Adresse des aktuellen Benutzers anzuzeigen,
// entnommen aus dem oben erstellten UserInformation-Objekt.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
auto fieldUserAddress = System::ExplicitCast<Aspose::Words::Fields::FieldUserAddress>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldUserAddress, true));

ASSERT_EQ(u" USERADDRESS ", fieldUserAddress->GetFieldCode());
ASSERT_EQ(u"123 Main Street", fieldUserAddress->get_Result());

// Wir können diese Eigenschaft festlegen, damit unser Feld den derzeit im UserInformation-Objekt gespeicherten Wert überschreibt.
fieldUserAddress->set_UserAddress(u"456 North Road");
fieldUserAddress->Update();

ASSERT_EQ(u" USERADDRESS  \"456 North Road\"", fieldUserAddress->GetFieldCode());
ASSERT_EQ(u"456 North Road", fieldUserAddress->get_Result());

// Dies wirkt sich nicht auf den Wert im UserInformation-Objekt aus.
ASSERT_EQ(u"123 Main Street", doc->get_FieldOptions()->get_CurrentUser()->get_Address());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.USERADDRESS.docx");
```

## Siehe auch

* Class [FieldUserAddress](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
