---
title: "Método Aspose::Words::Drawing::ShapeBase::get_IsDecorative"
linktitle: "get_IsDecorative"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Drawing::ShapeBase::get_IsDecorative. Obtiene o establece la bandera que indica si la forma es decorativa en el documento en C++."
type: docs
weight: 25000
url: /es/cpp/aspose.words.drawing/shapebase/get_isdecorative/
---
## ShapeBase::get_IsDecorative method


Obtiene o establece la bandera que especifica si la forma es decorativa en el documento.

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_IsDecorative()
```


## Ejemplos



Muestra cómo establecer que la forma sea decorativa.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Decorative shapes.docx");

auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->idx_get(0));
ASSERT_TRUE(shape->get_IsDecorative());

// Si "AlternativeText" no está vacío, la forma no puede ser decorativa.
// Por eso nuestro valor ha cambiado a 'false'.
shape->set_AlternativeText(u"Alternative text.");
ASSERT_FALSE(shape->get_IsDecorative());

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->MoveToDocumentEnd();
// Cree una nueva forma como decorativa.
shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 100, 100);
shape->set_IsDecorative(true);

doc->Save(get_ArtifactsDir() + u"Shape.IsDecorative.docx");
```

## Ver también

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
