---
title: "Aspose::Words::Drawing::VerticalAlignment enum"
linktitle: "VerticalAlignment"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::VerticalAlignment enum. Especifica la alineación vertical de una forma flotante, un marco de texto o una tabla flotante en C++."
type: docs
weight: 43000
url: /es/cpp/aspose.words.drawing/verticalalignment/
---
## VerticalAlignment enum


Especifica la alineación vertical de una forma flotante, marco de texto o tabla flotante.

```cpp
enum class VerticalAlignment
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| None | 0 | El objeto está posicionado explícitamente, normalmente usando su propiedad **Top**. |
| Superior | 1 | Especifica que el objeto debe estar en la parte superior de la base de alineación vertical. |
| Centro | 2 | Especifica que el objeto debe estar centrado con respecto a la base de alineación vertical. |
| Inferior | 3 | Especifica que el objeto debe estar en la parte inferior de la base de alineación vertical. |
| Dentro | 4 | Especifica que el objeto debe estar dentro de la base de alineación horizontal. |
| Exterior | 5 | Especifica que el objeto debe estar fuera de la base de alineación vertical. |
| En línea | -1 | No documentado. Parece ser un valor posible para párrafos y tablas flotantes. |
| Default | n/a | Lo mismo que [None](./). |


## Ejemplos



Muestra cómo insertar una imagen flotante en el centro de una página.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserta una imagen flotante que aparecerá detrás del texto superpuesto y alinéala al centro de la página.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);
shape->set_BehindText(true);
shape->set_RelativeHorizontalPosition(Aspose::Words::Drawing::RelativeHorizontalPosition::Page);
shape->set_RelativeVerticalPosition(Aspose::Words::Drawing::RelativeVerticalPosition::Page);
shape->set_HorizontalAlignment(Aspose::Words::Drawing::HorizontalAlignment::Center);
shape->set_VerticalAlignment(Aspose::Words::Drawing::VerticalAlignment::Center);

doc->Save(get_ArtifactsDir() + u"Image.CreateFloatingPageCenter.docx");
```

## Ver también

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
