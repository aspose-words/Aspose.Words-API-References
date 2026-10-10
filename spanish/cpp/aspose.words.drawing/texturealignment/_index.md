---
title: "Aspose::Words::Drawing::TextureAlignment enum"
linktitle: "TextureAlignment"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::TextureAlignment enum. Especifica la alineación para el mosaico del relleno de textura en C++."
type: docs
weight: 42000
url: /es/cpp/aspose.words.drawing/texturealignment/
---
## TextureAlignment enum


Especifica la alineación para el mosaico del relleno de textura.

```cpp
enum class TextureAlignment
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| TopLeft | 0 | Alineación de textura superior izquierda. |
| Superior | 1 | Alineación de textura superior. |
| TopRight | 2 | Alineación de textura superior derecha. |
| Izquierda | 3 | Alineación de textura izquierda. |
| Centro | 4 | Alineación de textura centrada. |
| Derecha | 5 | Alineación de textura derecha. |
| BottomLeft | 6 | Alineación de textura inferior izquierda. |
| Inferior | 7 | Alineación de textura inferior. |
| BottomRight | 8 | Alineación de textura inferior derecha. |
| None | 9 | Sin alineación de textura. |


## Ejemplos



Muestra cómo rellenar y mosaicar la textura dentro de la forma.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 80, 80);

// Aplicar la alineación de textura al relleno de la forma.
shape->get_Fill()->PresetTextured(Aspose::Words::Drawing::PresetTexture::Canvas);
shape->get_Fill()->set_TextureAlignment(Aspose::Words::Drawing::TextureAlignment::TopRight);

// Utilice la opción de cumplimiento para definir la forma usando DML si desea obtener "TextureAlignment"
// propiedad después de que el documento se guarda.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>();
saveOptions->set_Compliance(Aspose::Words::Saving::OoxmlCompliance::Iso29500_2008_Strict);

doc->Save(get_ArtifactsDir() + u"Shape.TextureFill.docx", saveOptions);

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Shape.TextureFill.docx");
shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

ASSERT_EQ(Aspose::Words::Drawing::TextureAlignment::TopRight, shape->get_Fill()->get_TextureAlignment());
ASSERT_EQ(Aspose::Words::Drawing::PresetTexture::Canvas, shape->get_Fill()->get_PresetTexture());
```

## Ver también

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
