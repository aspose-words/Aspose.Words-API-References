---
title: "Aspose::Words::Fields::Field::get_DisplayResult method"
linktitle: "get_DisplayResult"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Fields::Field::get_DisplayResult method. Obtiene el texto que representa el resultado del campo mostrado en C++."
type: docs
weight: 2000
url: /es/cpp/aspose.words.fields/field/get_displayresult/
---
## Field::get_DisplayResult method


Obtiene el texto que representa el resultado del campo mostrado.

```cpp
System::String Aspose::Words::Fields::Field::get_DisplayResult()
```


## Ejemplos



Muestra cómo obtener el texto real que un campo muestra en el documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"This document was written by ");
auto fieldAuthor = System::ExplicitCast<Aspose::Words::Fields::FieldAuthor>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldAuthor, true));
fieldAuthor->set_AuthorName(u"John Doe");

// Podemos usar la propiedad DisplayResult para verificar qué texto exacto
// un campo mostraría en su lugar en el documento.
ASSERT_EQ(System::String::Empty, fieldAuthor->get_DisplayResult());

// Los campos no mantienen valores de resultado precisos en tiempo real.
// Para asegurarnos de que nuestros campos muestren resultados precisos en cualquier momento,
// como justo antes de una operación de guardado, necesitamos actualizarlos manualmente.
fieldAuthor->Update();

ASSERT_EQ(u"John Doe", fieldAuthor->get_DisplayResult());

doc->Save(get_ArtifactsDir() + u"Field.DisplayResult.docx");
```

## Ver también

* Class [Field](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
