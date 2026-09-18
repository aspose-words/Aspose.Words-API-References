---
title: "Aspose::Words::Drawing::ShapeBase::get_MarkupLanguage Methode"
linktitle: "get_MarkupLanguage"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::ShapeBase::get_MarkupLanguage Methode. Gibt die für dieses Grafikobjekt in C++ verwendete Auszeichnungssprache zurück."
type: docs
weight: 39000
url: /de/cpp/aspose.words.drawing/shapebase/get_markuplanguage/
---
## ShapeBase::get_MarkupLanguage method


Liest die für dieses Grafikobjekt verwendete MarkupLanguage.

```cpp
Aspose::Words::Drawing::ShapeMarkupLanguage Aspose::Words::Drawing::ShapeBase::get_MarkupLanguage() const
```


## Beispiele



Zeigt, wie die Größe einer Form und die Auszeichnungssprache überprüft werden.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Transparent background logo.png");

ASSERT_EQ(Aspose::Words::Drawing::ShapeMarkupLanguage::Dml, shape->get_MarkupLanguage());
ASPOSE_ASSERT_EQ(System::Drawing::SizeF(300.0f, 300.0f), shape->get_SizeInPoints());
```

## Siehe auch

* Enum [ShapeMarkupLanguage](../../shapemarkuplanguage/)
* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
