---
title: "Aspose::Words::PhoneticGuide::get_BaseText Methode"
linktitle: "get_BaseText"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::PhoneticGuide::get_BaseText-Methode. Gibt den Basistext des phonetischen Leitfadens in C++ zurück."
type: docs
weight: 2000
url: /de/cpp/aspose.words/phoneticguide/get_basetext/
---
## PhoneticGuide::get_BaseText method


Liest den Basistext des Phonetic Guide.

```cpp
System::String Aspose::Words::PhoneticGuide::get_BaseText()
```


## Beispiele



Zeigt, wie man die Eigenschaften des phonetischen Leitfadens abruft.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Phonetic guide.docx");

System::SharedPtr<Aspose::Words::RunCollection> runs = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs();
// Verwenden Sie den phonetischen Leitfaden im asiatischen Text.
ASPOSE_ASSERT_EQ(true, runs->idx_get(0)->get_IsPhoneticGuide());
ASSERT_EQ(u"base", runs->idx_get(0)->get_PhoneticGuide()->get_BaseText());
ASSERT_EQ(u"ruby", runs->idx_get(0)->get_PhoneticGuide()->get_RubyText());
```

## Siehe auch

* Class [PhoneticGuide](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
