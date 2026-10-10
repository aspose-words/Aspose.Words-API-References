---
title: "Aspose::Words::Fields::UserInformation::get_Address Methode"
linktitle: "get_Address"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fields::UserInformation::get_Address Methode. Liest oder setzt die Postadresse des Benutzers in C++."
type: docs
weight: 4000
url: /de/cpp/aspose.words.fields/userinformation/get_address/
---
## UserInformation::get_Address method


Liest oder setzt die Postadresse des Benutzers.

```cpp
System::String Aspose::Words::Fields::UserInformation::get_Address() const
```


## Beispiele



Zeigt, wie Benutzerdetails festgelegt und mithilfe von Feldern angezeigt werden.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Erstellen Sie ein UserInformation-Objekt und setzen Sie es als Datenquelle für Felder, die Benutzerinformationen anzeigen.
auto userInformation = System::MakeObject<Aspose::Words::Fields::UserInformation>();
userInformation->set_Name(u"John Doe");
userInformation->set_Initials(u"J. D.");
userInformation->set_Address(u"123 Main Street");
doc->get_FieldOptions()->set_CurrentUser(userInformation);

// Fügen Sie die Felder USERNAME, USERINITIALS und USERADDRESS ein, die Werte von
// den jeweiligen Eigenschaften des oben erstellten UserInformation-Objekts.
ASSERT_EQ(userInformation->get_Name(), builder->InsertField(u" USERNAME ")->get_Result());
ASSERT_EQ(userInformation->get_Initials(), builder->InsertField(u" USERINITIALS ")->get_Result());
ASSERT_EQ(userInformation->get_Address(), builder->InsertField(u" USERADDRESS ")->get_Result());

// Das Feldoptionen-Objekt verfügt außerdem über einen statischen Standardbenutzer, auf den Felder aus allen Dokumenten verweisen können.
Aspose::Words::Fields::UserInformation::get_DefaultUser()->set_Name(u"Default User");
Aspose::Words::Fields::UserInformation::get_DefaultUser()->set_Initials(u"D. U.");
Aspose::Words::Fields::UserInformation::get_DefaultUser()->set_Address(u"One Microsoft Way");
doc->get_FieldOptions()->set_CurrentUser(Aspose::Words::Fields::UserInformation::get_DefaultUser());

ASSERT_EQ(u"Default User", builder->InsertField(u" USERNAME ")->get_Result());
ASSERT_EQ(u"D. U.", builder->InsertField(u" USERINITIALS ")->get_Result());
ASSERT_EQ(u"One Microsoft Way", builder->InsertField(u" USERADDRESS ")->get_Result());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"FieldOptions.CurrentUser.docx");
```

## Siehe auch

* Class [UserInformation](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
