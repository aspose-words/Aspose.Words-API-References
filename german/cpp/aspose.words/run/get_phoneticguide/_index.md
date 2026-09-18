---
title: "Aspose::Words::Run::get_PhoneticGuide-Methode"
linktitle: "get_PhoneticGuide"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Run::get_PhoneticGuide-Methode. Gibt ein PhoneticGuide-Objekt in C++ zurück."
type: docs
weight: 4500
url: /de/cpp/aspose.words/run/get_phoneticguide/
---
## Run::get_PhoneticGuide method


Ruft ein [PhoneticGuide](./)-Objekt ab.

```cpp
System::SharedPtr<Aspose::Words::PhoneticGuide> Aspose::Words::Run::get_PhoneticGuide()
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

* Class [PhoneticGuide](../../phoneticguide/)
* Class [Run](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
