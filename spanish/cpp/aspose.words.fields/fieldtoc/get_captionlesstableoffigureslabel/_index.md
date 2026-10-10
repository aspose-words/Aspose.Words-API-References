---
title: "Aspose::Words::Fields::FieldToc::get_CaptionlessTableOfFiguresLabel método"
linktitle: "get_CaptionlessTableOfFiguresLabel"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Fields::FieldToc::get_CaptionlessTableOfFiguresLabel método. Obtiene o establece el nombre del identificador de secuencia utilizado al crear una tabla de figuras que no incluye la etiqueta y el número del subtítulo en C++."
type: docs
weight: 4000
url: /es/cpp/aspose.words.fields/fieldtoc/get_captionlesstableoffigureslabel/
---
## FieldToc::get_CaptionlessTableOfFiguresLabel method


Obtiene o establece el nombre del identificador de secuencia utilizado al crear una tabla de figuras que no incluye la etiqueta y el número del título.

```cpp
System::String Aspose::Words::Fields::FieldToc::get_CaptionlessTableOfFiguresLabel()
```


## Ejemplos



Muestra cómo establecer el nombre del identificador de secuencia.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto fieldToc = System::ExplicitCast<Aspose::Words::Fields::FieldToc>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldTOC, true));
fieldToc->set_CaptionlessTableOfFiguresLabel(u"Test");

ASSERT_EQ(u" TOC  \\a Test", fieldToc->GetFieldCode());
```

## Ver también

* Class [FieldToc](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
