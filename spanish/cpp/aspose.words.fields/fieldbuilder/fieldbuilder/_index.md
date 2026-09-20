---
title: "Aspose::Words::Fields::FieldBuilder::FieldBuilder constructor"
linktitle: "FieldBuilder"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Fields::FieldBuilder::FieldBuilder constructor. Inicializa una instancia de la clase FieldBuilder en C++."
type: docs
weight: 2000
url: /es/cpp/aspose.words.fields/fieldbuilder/fieldbuilder/
---
## FieldBuilder::FieldBuilder constructor


Inicializa una instancia de la clase [FieldBuilder](../).

```cpp
Aspose::Words::Fields::FieldBuilder::FieldBuilder(Aspose::Words::Fields::FieldType fieldType)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| fieldType | Aspose::Words::Fields::FieldType | El tipo del campo a crear. |

## Ejemplos



Muestra cómo crear e insertar un campo usando un constructor de campos.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Una forma conveniente de añadir contenido de texto a un documento es con un constructor de documentos.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Write(u" Hello world! This text is one Run, which is an inline node.");

// Los campos tienen su constructor, que podemos usar para construir el código del campo pieza a pieza.
// En este caso, construiremos un campo BARCODE que representa un código postal de EE. UU.,
// y luego lo insertaremos delante de un Run.
auto fieldBuilder = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldBarcode);
fieldBuilder->AddArgument(u"90210");
fieldBuilder->AddSwitch(u"\\f", u"A");
fieldBuilder->AddSwitch(u"\\u");

fieldBuilder->BuildAndInsert(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0));

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.CreateWithFieldBuilder.docx");
```

## Ver también

* Enum [FieldType](../../fieldtype/)
* Class [FieldBuilder](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
