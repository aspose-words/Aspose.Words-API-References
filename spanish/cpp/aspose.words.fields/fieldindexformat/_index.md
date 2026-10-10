---
title: "Aspose::Words::Fields::FieldIndexFormat enum"
linktitle: "FieldIndexFormat"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Fields::FieldIndexFormat enum. Especifica el formato de los campos FieldIndex en un documento en C++."
type: docs
weight: 129000
url: /es/cpp/aspose.words.fields/fieldindexformat/
---
## FieldIndexFormat enum


Especifica el formato de los campos [FieldIndex](../fieldindex/) en un documento.

```cpp
enum class FieldIndexFormat
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Plantilla | 0 | Desde la plantilla. |
| Clásico | 1 | Clásico. |
| Elegante | 2 | Elegante. |
| Moderna | 3 | Moderno. |
| Con viñetas | 4 | Con viñetas. |
| Formal | 5 | Formal. |
| Simple | 6 | Simple. |


## Ejemplos



Muestra cómo formatear los campos [FieldIndex](../fieldindex/).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Write(u"A");
builder->InsertBreak(Aspose::Words::BreakType::LineBreak);
builder->InsertField(u"XE \"A\"");
builder->Write(u"B");

builder->InsertField(u" INDEX \\e \" · \" \\h \"A\" \\c \"2\" \\z \"1033\"", nullptr);

doc->get_FieldOptions()->set_FieldIndexFormat(Aspose::Words::Fields::FieldIndexFormat::Fancy);
doc->UpdateFields();

doc->Save(get_ArtifactsDir() + u"Field.SetFieldIndexFormat.docx");
```

## Ver también

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
