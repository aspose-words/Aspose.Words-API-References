---
title: "Aspose::Words::Fields::FieldImport::get_SourceFullName método"
linktitle: "get_SourceFullName"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Fields::FieldImport::get_SourceFullName método. Obtiene o establece la ubicación de la imagen en C++."
type: docs
weight: 4000
url: /es/cpp/aspose.words.fields/fieldimport/get_sourcefullname/
---
## FieldImport::get_SourceFullName method


Obtiene o establece la ubicación de la imagen.

```cpp
System::String Aspose::Words::Fields::FieldImport::get_SourceFullName() override
```


## Ejemplos



Muestra cómo insertar imágenes usando los campos IMPORT e INCLUDEPICTURE.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// A continuación se presentan dos tipos de campo similares que podemos usar para mostrar imágenes enlazadas desde el sistema de archivos local.
// 1 -  El campo INCLUDEPICTURE:
auto fieldIncludePicture = System::ExplicitCast<Aspose::Words::Fields::FieldIncludePicture>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIncludePicture, true));
fieldIncludePicture->set_SourceFullName(get_ImageDir() + u"Transparent background logo.png");

ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(fieldIncludePicture->GetFieldCode(), u" INCLUDEPICTURE  .*")->get_Success());

// Aplicar el filtro PNG32.FLT.
fieldIncludePicture->set_GraphicFilter(u"PNG32");
fieldIncludePicture->set_IsLinked(true);
fieldIncludePicture->set_ResizeHorizontally(true);
fieldIncludePicture->set_ResizeVertically(true);

// 2 -  El campo IMPORT:
auto fieldImport = System::ExplicitCast<Aspose::Words::Fields::FieldImport>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldImport, true));
fieldImport->set_SourceFullName(get_ImageDir() + u"Transparent background logo.png");
fieldImport->set_GraphicFilter(u"PNG32");
fieldImport->set_IsLinked(true);

ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(fieldImport->GetFieldCode(), u" IMPORT  .* \\\\c PNG32 \\\\d")->get_Success());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.IMPORT.INCLUDEPICTURE.docx");
```

## Ver también

* Class [FieldImport](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
