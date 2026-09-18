---
title: "Aspose::Words::Run::get_IsPhoneticGuide-Methode"
linktitle: "get_IsPhoneticGuide"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Run::get_IsPhoneticGuide-Methode. Gibt einen booleschen Wert zurück, der angibt, ob der Run ein phonetischer Leitfaden ist, in C++."
type: docs
weight: 3500
url: /de/cpp/aspose.words/run/get_isphoneticguide/
---
## Run::get_IsPhoneticGuide method


Gibt einen booleschen Wert zurück, der angibt, ob der Lauf ein phonetischer Leitfaden ist.

```cpp
bool Aspose::Words::Run::get_IsPhoneticGuide()
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

* Class [Run](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
