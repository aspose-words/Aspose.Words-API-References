---
title: "Método Aspose::Words::Fields::FieldPrint::get_PostScriptGroup"
linktitle: "get_PostScriptGroup"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Fields::FieldPrint::get_PostScriptGroup. Obtiene o establece el rectángulo de dibujo en el que operan las instrucciones PostScript en C++."
type: docs
weight: 2000
url: /es/cpp/aspose.words.fields/fieldprint/get_postscriptgroup/
---
## FieldPrint::get_PostScriptGroup method


Obtiene o establece el rectángulo de dibujo en el que operan las instrucciones PostScript.

```cpp
System::String Aspose::Words::Fields::FieldPrint::get_PostScriptGroup()
```


## Ejemplos



Muestra cómo insertar un campo PRINT.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"My paragraph");

// El campo PRINT puede enviar instrucciones a la impresora.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldPrint>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldPrint, true));

// Establezca el área sobre la que la impresora ejecutará las instrucciones.
// En este caso, será el párrafo que contiene nuestro campo PRINT.
field->set_PostScriptGroup(u"para");

// Cuando usamos una impresora que soporta PostScript para imprimir nuestro documento,
// este comando volverá blanca toda el área que especificamos en "field.PostScriptGroup".
field->set_PrinterInstructions(u"erasepage");

ASSERT_EQ(u" PRINT  erasepage \\p para", field->GetFieldCode());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.PRINT.docx");
```

## Ver también

* Class [FieldPrint](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
