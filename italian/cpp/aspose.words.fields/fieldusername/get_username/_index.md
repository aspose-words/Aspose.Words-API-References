---
title: "Metodo get_UserName di Aspose::Words::Fields::FieldUserName"
linktitle: "get_UserName"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo get_UserName di Aspose::Words::Fields::FieldUserName. Ottiene o imposta il nome dell'utente corrente in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words.fields/fieldusername/get_username/
---
## FieldUserName::get_UserName method


Ottiene o imposta il nome dell'utente corrente.

```cpp
System::String Aspose::Words::Fields::FieldUserName::get_UserName()
```


## Esempi



Mostra come utilizzare il campo USERNAME.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Crea un oggetto UserInformation e impostalo come origine delle informazioni utente per tutti i campi che creiamo.
auto userInformation = System::MakeObject<Aspose::Words::Fields::UserInformation>();
userInformation->set_Name(u"John Doe");
doc->get_FieldOptions()->set_CurrentUser(userInformation);

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Crea un campo USERNAME per visualizzare il nome dell'utente corrente,
// preso dall'oggetto UserInformation che abbiamo creato sopra.
auto fieldUserName = System::ExplicitCast<Aspose::Words::Fields::FieldUserName>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldUserName, true));
ASSERT_EQ(userInformation->get_Name(), fieldUserName->get_Result());

ASSERT_EQ(u" USERNAME ", fieldUserName->GetFieldCode());
ASSERT_EQ(u"John Doe", fieldUserName->get_Result());

// Possiamo impostare questa proprietà per far sì che il nostro campo sovrascriva il valore attualmente memorizzato nell'oggetto UserInformation.
fieldUserName->set_UserName(u"Jane Doe");
fieldUserName->Update();

ASSERT_EQ(u" USERNAME  \"Jane Doe\"", fieldUserName->GetFieldCode());
ASSERT_EQ(u"Jane Doe", fieldUserName->get_Result());

// Questo non influisce sul valore nell'oggetto UserInformation.
ASSERT_EQ(u"John Doe", doc->get_FieldOptions()->get_CurrentUser()->get_Name());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.USERNAME.docx");
```

## Vedi anche

* Class [FieldUserName](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
