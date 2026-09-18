---
title: "Aspose::Words::Document::get_ShadeFormData Methode"
linktitle: "get_ShadeFormData"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Document::get_ShadeFormData Methode. Gibt an, ob die graue Schattierung für Formularfelder in C++ aktiviert werden soll."
type: docs
weight: 49000
url: /de/cpp/aspose.words/document/get_shadeformdata/
---
## Document::get_ShadeFormData method


Gibt an, ob die graue Schattierung bei Formularfeldern aktiviert werden soll.

```cpp
bool Aspose::Words::Document::get_ShadeFormData()
```


## Beispiele



Zeigt, wie man graue Schattierung auf Formularfelder anwendet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Hello world! ");
builder->InsertTextInput(u"My form field", Aspose::Words::Fields::TextFormFieldType::Regular, u"", u"Text contents of form field, which are shaded in grey by default.", 0);

// Wir können die graue Schattierung ausschalten, sodass der markierte Text sich in den übrigen Text einfügt.
doc->set_ShadeFormData(useGreyShading);
doc->Save(get_ArtifactsDir() + u"Document.ShadeFormData.docx");
```

## Siehe auch

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
