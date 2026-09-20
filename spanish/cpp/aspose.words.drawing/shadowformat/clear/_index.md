---
title: "Método Aspose::Words::Drawing::ShadowFormat::Clear"
linktitle: "Clear"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Drawing::ShadowFormat::Clear. Borra el formato de sombra en C++."
type: docs
weight: 2000
url: /es/cpp/aspose.words.drawing/shadowformat/clear/
---
## ShadowFormat::Clear method


Borra el formato de sombra.

```cpp
void Aspose::Words::Drawing::ShadowFormat::Clear()
```


## Ejemplos



Muestra cómo trabajar con un formato de sombra para la forma.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Shape stroke pattern border.docx");
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->idx_get(0));

if (shape->get_ShadowFormat()->get_Visible() && shape->get_ShadowFormat()->get_Type() == Aspose::Words::Drawing::ShadowType::Shadow2)
{
    shape->get_ShadowFormat()->set_Type(Aspose::Words::Drawing::ShadowType::Shadow7);
}

if (shape->get_ShadowFormat()->get_Type() == Aspose::Words::Drawing::ShadowType::ShadowMixed)
{
    shape->get_ShadowFormat()->Clear();
}
```

## Ver también

* Class [ShadowFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
