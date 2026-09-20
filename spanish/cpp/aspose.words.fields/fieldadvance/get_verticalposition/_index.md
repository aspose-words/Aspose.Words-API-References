---
title: "Aspose::Words::Fields::FieldAdvance::get_VerticalPosition método"
linktitle: "get_VerticalPosition"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Fields::FieldAdvance::get_VerticalPosition método. Obtiene o establece el número de puntos por los que el texto que sigue al campo debe desplazarse verticalmente desde el borde superior de la página en C++."
type: docs
weight: 7000
url: /es/cpp/aspose.words.fields/fieldadvance/get_verticalposition/
---
## FieldAdvance::get_VerticalPosition method


Obtiene o establece el número de puntos por los que el texto que sigue al campo debe moverse verticalmente desde el borde superior de la página.

```cpp
System::String Aspose::Words::Fields::FieldAdvance::get_VerticalPosition()
```


## Ejemplos



Muestra cómo insertar un campo ADVANCE y editar sus propiedades.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"This text is in its normal place.");

// A continuación se presentan dos formas de usar el campo ADVANCE para ajustar la posición del texto que le sigue.
// Los efectos de un campo ADVANCE continúan aplicándose hasta que finaliza el párrafo,
// o otro campo ADVANCE actualiza los valores de desplazamiento/coordenadas.
// 1 -  Especifique un desplazamiento direccional:
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldAdvance>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldAdvance, true));
field->set_RightOffset(u"5");
field->set_UpOffset(u"5");

ASSERT_EQ(u" ADVANCE  \\r 5 \\u 5", field->GetFieldCode());

builder->Write(u"This text will be moved up and to the right.");

field = System::ExplicitCast<Aspose::Words::Fields::FieldAdvance>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldAdvance, true));
field->set_DownOffset(u"5");
field->set_LeftOffset(u"100");

ASSERT_EQ(u" ADVANCE  \\d 5 \\l 100", field->GetFieldCode());

builder->Writeln(u"This text is moved down and to the left, overlapping the previous text.");

// 2 -  Mueva el texto a una posición especificada por coordenadas:
field = System::ExplicitCast<Aspose::Words::Fields::FieldAdvance>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldAdvance, true));
field->set_HorizontalPosition(u"-100");
field->set_VerticalPosition(u"200");

ASSERT_EQ(u" ADVANCE  \\x -100 \\y 200", field->GetFieldCode());

builder->Write(u"This text is in a custom position.");

doc->Save(get_ArtifactsDir() + u"Field.ADVANCE.docx");
```

## Ver también

* Class [FieldAdvance](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
