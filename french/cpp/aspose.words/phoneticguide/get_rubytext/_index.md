---
title: "Méthode Aspose::Words::PhoneticGuide::get_RubyText"
linktitle: "get_RubyText"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::PhoneticGuide::get_RubyText. Obtient le texte ruby du guide phonétique en C++."
type: docs
weight: 3000
url: /fr/cpp/aspose.words/phoneticguide/get_rubytext/
---
## PhoneticGuide::get_RubyText method


Obtient le texte ruby du guide phonétique.

```cpp
System::String Aspose::Words::PhoneticGuide::get_RubyText()
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

* Class [PhoneticGuide](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
