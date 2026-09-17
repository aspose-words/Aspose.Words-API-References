---
title: "Méthode Aspose::Words::Run::get_PhoneticGuide"
linktitle: "get_PhoneticGuide"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Run::get_PhoneticGuide. Obtient un objet PhoneticGuide en C++."
type: docs
weight: 4500
url: /fr/cpp/aspose.words/run/get_phoneticguide/
---
## Run::get_PhoneticGuide method


Obtient un objet [PhoneticGuide](./).

```cpp
System::SharedPtr<Aspose::Words::PhoneticGuide> Aspose::Words::Run::get_PhoneticGuide()
```


## Exemples



Montre comment obtenir les propriétés du guide phonétique.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Phonetic guide.docx");

System::SharedPtr<Aspose::Words::RunCollection> runs = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs();
// Utilisez le guide phonétique dans le texte asiatique.
ASPOSE_ASSERT_EQ(true, runs->idx_get(0)->get_IsPhoneticGuide());
ASSERT_EQ(u"base", runs->idx_get(0)->get_PhoneticGuide()->get_BaseText());
ASSERT_EQ(u"ruby", runs->idx_get(0)->get_PhoneticGuide()->get_RubyText());
```

## Voir aussi

* Class [PhoneticGuide](../../phoneticguide/)
* Class [Run](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
