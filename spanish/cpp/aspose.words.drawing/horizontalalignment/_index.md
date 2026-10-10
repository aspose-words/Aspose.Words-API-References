---
title: "Enumeración Aspose::Words::Drawing::HorizontalAlignment"
linktitle: "HorizontalAlignment"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Enumeración Aspose::Words::Drawing::HorizontalAlignment. Especifica la alineación horizontal de una forma flotante, marco de texto o tabla flotante en C++."
type: docs
weight: 26000
url: /es/cpp/aspose.words.drawing/horizontalalignment/
---
## HorizontalAlignment enum


Especifica la alineación horizontal de una forma flotante, marco de texto o tabla flotante.

```cpp
enum class HorizontalAlignment
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| None | 0 | El objeto se posiciona explícitamente, normalmente usando su propiedad **Left**. |
| Default | n/a | Lo mismo que [None](./). |
| Izquierda | 1 | Especifica que el objeto debe alinearse a la izquierda con respecto a la base de alineación horizontal. |
| Centro | 2 | Especifica que el objeto debe centrarse con respecto a la base de alineación horizontal. |
| Derecha | 3 | Especifica que el objeto debe estar alineado a la derecha con respecto a la base de alineación horizontal. |
| Dentro | 4 | Especifica que el objeto debe estar dentro de la base de alineación horizontal. |
| Exterior | 5 | Especifica que el objeto debe estar fuera de la base de alineación horizontal. |


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
