---
title: "Metodo Aspose::Words::Drawing::ShapeBase::get_ShadowFormat"
linktitle: "get_ShadowFormat"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Drawing::ShapeBase::get_ShadowFormat. Ottiene la formattazione dell'ombra per la forma in C++."
type: docs
weight: 47000
url: /it/cpp/aspose.words.drawing/shapebase/get_shadowformat/
---
## ShapeBase::get_ShadowFormat method


Ottiene la formattazione dell'ombra per la forma.

```cpp
System::SharedPtr<Aspose::Words::Drawing::ShadowFormat> Aspose::Words::Drawing::ShapeBase::get_ShadowFormat()
```


## Esempi



Mostra come ottenere il colore dell'ombra.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Shadow color.docx");
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
System::SharedPtr<Aspose::Words::Drawing::ShadowFormat> shadowFormat = shape->get_ShadowFormat();

ASSERT_EQ(System::Drawing::Color::get_Red().ToArgb(), shadowFormat->get_Color().ToArgb());
ASSERT_EQ(Aspose::Words::Drawing::ShadowType::ShadowMixed, shadowFormat->get_Type());
```

## Vedi anche

* Class [ShadowFormat](../../shadowformat/)
* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
