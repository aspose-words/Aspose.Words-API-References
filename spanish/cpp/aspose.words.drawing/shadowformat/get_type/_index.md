---
title: "Método Aspose::Words::Drawing::ShadowFormat::get_Type"
linktitle: "get_Type"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Drawing::ShadowFormat::get_Type. Obtiene o establece el ShadowType especificado para ShadowFormat en C++."
type: docs
weight: 3000
url: /es/cpp/aspose.words.drawing/shadowformat/get_type/
---
## ShadowFormat::get_Type method


Obtiene o establece el [ShadowType](../../shadowtype/) especificado para [ShadowFormat](../).

```cpp
Aspose::Words::Drawing::ShadowType Aspose::Words::Drawing::ShadowFormat::get_Type()
```


## Ejemplos



Muestra cómo obtener el color de la sombra.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Shadow color.docx");
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
System::SharedPtr<Aspose::Words::Drawing::ShadowFormat> shadowFormat = shape->get_ShadowFormat();

ASSERT_EQ(System::Drawing::Color::get_Red().ToArgb(), shadowFormat->get_Color().ToArgb());
ASSERT_EQ(Aspose::Words::Drawing::ShadowType::ShadowMixed, shadowFormat->get_Type());
```

## Ver también

* Enum [ShadowType](../../shadowtype/)
* Class [ShadowFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
