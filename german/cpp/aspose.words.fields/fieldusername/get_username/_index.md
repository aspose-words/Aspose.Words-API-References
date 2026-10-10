---
title: "Aspose::Words::Fields::FieldUserName::get_UserName Methode"
linktitle: "get_UserName"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fields::FieldUserName::get_UserName-Methode. Ruft den Namen des aktuellen Benutzers ab oder legt ihn fest in C++."
type: docs
weight: 2000
url: /de/cpp/aspose.words.fields/fieldusername/get_username/
---
## FieldUserName::get_UserName method


Liest oder setzt den Namen des aktuellen Benutzers.

```cpp
System::String Aspose::Words::Fields::FieldUserName::get_UserName()
```


## Beispiele



Zeigt, wie das USERNAME-Feld verwendet wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Erstellen Sie ein UserInformation-Objekt und setzen Sie es als Quelle für Benutzerinformationen für alle Felder, die wir erstellen.
auto userInformation = System::MakeObject<Aspose::Words::Fields::UserInformation>();
userInformation->set_Name(u"John Doe");
doc->get_FieldOptions()->set_CurrentUser(userInformation);

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Erstellen Sie ein USERNAME-Feld, um den Namen des aktuellen Benutzers anzuzeigen,
// entnommen aus dem oben erstellten UserInformation-Objekt.
auto fieldUserName = System::ExplicitCast<Aspose::Words::Fields::FieldUserName>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldUserName, true));
ASSERT_EQ(userInformation->get_Name(), fieldUserName->get_Result());

ASSERT_EQ(u" USERNAME ", fieldUserName->GetFieldCode());
ASSERT_EQ(u"John Doe", fieldUserName->get_Result());

// Wir können diese Eigenschaft festlegen, damit unser Feld den derzeit im UserInformation-Objekt gespeicherten Wert überschreibt.
fieldUserName->set_UserName(u"Jane Doe");
fieldUserName->Update();

ASSERT_EQ(u" USERNAME  \"Jane Doe\"", fieldUserName->GetFieldCode());
ASSERT_EQ(u"Jane Doe", fieldUserName->get_Result());

// Dies wirkt sich nicht auf den Wert im UserInformation-Objekt aus.
ASSERT_EQ(u"John Doe", doc->get_FieldOptions()->get_CurrentUser()->get_Name());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.USERNAME.docx");
```

## Siehe auch

* Class [FieldUserName](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
