---
title: "Aspose::Words::Fields::FieldUserAddress::get_UserAddress metodo"
linktitle: "get_UserAddress"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Fields::FieldUserAddress::get_UserAddress metodo. Ottiene o imposta l'indirizzo postale dell'utente corrente in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words.fields/fielduseraddress/get_useraddress/
---
## FieldUserAddress::get_UserAddress method


Ottiene o imposta l'indirizzo postale dell'utente corrente.

```cpp
System::String Aspose::Words::Fields::FieldUserAddress::get_UserAddress()
```


## Esempi



Mostra come utilizzare il campo USERADDRESS.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Crea un oggetto UserInformation e impostalo come origine delle informazioni utente per tutti i campi che creiamo.
auto userInformation = System::MakeObject<Aspose::Words::Fields::UserInformation>();
userInformation->set_Address(u"123 Main Street");
doc->get_FieldOptions()->set_CurrentUser(userInformation);

// Crea un campo USERADDRESS per visualizzare l'indirizzo dell'utente corrente,
// preso dall'oggetto UserInformation che abbiamo creato sopra.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
auto fieldUserAddress = System::ExplicitCast<Aspose::Words::Fields::FieldUserAddress>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldUserAddress, true));

ASSERT_EQ(u" USERADDRESS ", fieldUserAddress->GetFieldCode());
ASSERT_EQ(u"123 Main Street", fieldUserAddress->get_Result());

// Possiamo impostare questa proprietà per far sì che il nostro campo sovrascriva il valore attualmente memorizzato nell'oggetto UserInformation.
fieldUserAddress->set_UserAddress(u"456 North Road");
fieldUserAddress->Update();

ASSERT_EQ(u" USERADDRESS  \"456 North Road\"", fieldUserAddress->GetFieldCode());
ASSERT_EQ(u"456 North Road", fieldUserAddress->get_Result());

// Questo non influisce sul valore nell'oggetto UserInformation.
ASSERT_EQ(u"123 Main Street", doc->get_FieldOptions()->get_CurrentUser()->get_Address());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.USERADDRESS.docx");
```

## Vedi anche

* Class [FieldUserAddress](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
