---
title: "Aspose::Words::Fields::FieldUserInitials::get_UserInitials Methode"
linktitle: "get_UserInitials"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fields::FieldUserInitials::get_UserInitials Methode. Liest oder setzt die Initialen des aktuellen Benutzers in C++."
type: docs
weight: 2000
url: /de/cpp/aspose.words.fields/fielduserinitials/get_userinitials/
---
## FieldUserInitials::get_UserInitials method


Liest oder setzt die Initialen des aktuellen Benutzers.

```cpp
System::String Aspose::Words::Fields::FieldUserInitials::get_UserInitials()
```


## Beispiele



Zeigt, wie das Feld USERINITIALS verwendet wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Erstellen Sie ein UserInformation-Objekt und setzen Sie es als Quelle für Benutzerinformationen für alle Felder, die wir erstellen.
auto userInformation = System::MakeObject<Aspose::Words::Fields::UserInformation>();
userInformation->set_Initials(u"J. D.");
doc->get_FieldOptions()->set_CurrentUser(userInformation);

// Erstellen Sie ein USERINITIALS-Feld, um die Initialen des aktuellen Benutzers anzuzeigen,
// entnommen aus dem oben erstellten UserInformation-Objekt.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
auto fieldUserInitials = System::ExplicitCast<Aspose::Words::Fields::FieldUserInitials>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldUserInitials, true));
ASSERT_EQ(userInformation->get_Initials(), fieldUserInitials->get_Result());

ASSERT_EQ(u" USERINITIALS ", fieldUserInitials->GetFieldCode());
ASSERT_EQ(u"J. D.", fieldUserInitials->get_Result());

// Wir können diese Eigenschaft festlegen, damit unser Feld den derzeit im UserInformation-Objekt gespeicherten Wert überschreibt.
fieldUserInitials->set_UserInitials(u"J. C.");
fieldUserInitials->Update();

ASSERT_EQ(u" USERINITIALS  \"J. C.\"", fieldUserInitials->GetFieldCode());
ASSERT_EQ(u"J. C.", fieldUserInitials->get_Result());

// Dies wirkt sich nicht auf den Wert im UserInformation-Objekt aus.
ASSERT_EQ(u"J. D.", doc->get_FieldOptions()->get_CurrentUser()->get_Initials());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.USERINITIALS.docx");
```

## Siehe auch

* Class [FieldUserInitials](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
