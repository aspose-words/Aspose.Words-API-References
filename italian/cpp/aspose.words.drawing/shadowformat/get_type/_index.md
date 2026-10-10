---
title: "Metodo Aspose::Words::Drawing::ShadowFormat::get_Type"
linktitle: "get_Type"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Drawing::ShadowFormat::get_Type. Ottiene o imposta lo ShadowType specificato per ShadowFormat in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words.drawing/shadowformat/get_type/
---
## ShadowFormat::get_Type method


Ottiene o imposta lo [ShadowType](../../shadowtype/) specificato per [ShadowFormat](../).

```cpp
Aspose::Words::Drawing::ShadowType Aspose::Words::Drawing::ShadowFormat::get_Type()
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

* Enum [ShadowType](../../shadowtype/)
* Class [ShadowFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
