---
title: "Aspose::Words::Fields::FieldToc::get_CaptionlessTableOfFiguresLabel Methode"
linktitle: "get_CaptionlessTableOfFiguresLabel"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fields::FieldToc::get_CaptionlessTableOfFiguresLabel method. Gibt den Namen des Sequenzidentifikators zurück oder legt ihn fest, der beim Erstellen eines Abbildungsverzeichnisses verwendet wird, das die Beschriftungsbezeichnung und -nummer nicht enthält, in C++."
type: docs
weight: 4000
url: /de/cpp/aspose.words.fields/fieldtoc/get_captionlesstableoffigureslabel/
---
## FieldToc::get_CaptionlessTableOfFiguresLabel method


Liest oder setzt den Namen des Sequenzidentifikators, der beim Erstellen eines Abbildungsverzeichnisses verwendet wird, das die Beschriftungsbezeichnung und -nummer nicht enthält.

```cpp
System::String Aspose::Words::Fields::FieldToc::get_CaptionlessTableOfFiguresLabel()
```


## Beispiele



Zeigt, wie der Name des Sequenzidentifikators festgelegt wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto fieldToc = System::ExplicitCast<Aspose::Words::Fields::FieldToc>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldTOC, true));
fieldToc->set_CaptionlessTableOfFiguresLabel(u"Test");

ASSERT_EQ(u" TOC  \\a Test", fieldToc->GetFieldCode());
```

## Siehe auch

* Class [FieldToc](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
