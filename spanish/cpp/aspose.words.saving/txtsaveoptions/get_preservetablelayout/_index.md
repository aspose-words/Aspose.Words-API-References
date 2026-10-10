---
title: "Método Aspose::Words::Saving::TxtSaveOptions::get_PreserveTableLayout"
linktitle: "get_PreserveTableLayout"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Saving::TxtSaveOptions::get_PreserveTableLayout. Especifica si el programa debe intentar preservar el diseño de las tablas al guardar en formato de texto plano. El valor predeterminado es false en C++."
type: docs
weight: 6000
url: /es/cpp/aspose.words.saving/txtsaveoptions/get_preservetablelayout/
---
## TxtSaveOptions::get_PreserveTableLayout method


Especifica si el programa debe intentar preservar el diseño de las tablas al guardar en formato de texto plano. El valor predeterminado es **false**.

```cpp
bool Aspose::Words::Saving::TxtSaveOptions::get_PreserveTableLayout() const
```


## Ejemplos



Muestra cómo preservar el diseño de las tablas al convertir a texto plano.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->StartTable();
builder->InsertCell();
builder->Write(u"Row 1, cell 1");
builder->InsertCell();
builder->Write(u"Row 1, cell 2");
builder->EndRow();
builder->InsertCell();
builder->Write(u"Row 2, cell 1");
builder->InsertCell();
builder->Write(u"Row 2, cell 2");
builder->EndTable();

// Cree un objeto "TxtSaveOptions", que podemos pasar al método "Save" del documento
// para modificar cómo guardamos el documento en texto plano.
auto txtSaveOptions = System::MakeObject<Aspose::Words::Saving::TxtSaveOptions>();

// Establezca la propiedad "PreserveTableLayout" a "true" para aplicar relleno de espacios en blanco al contenido
// del documento de texto plano de salida para preservar tanto como sea posible el diseño de la tabla.
// Establezca la propiedad "PreserveTableLayout" a "false" para guardar el contenido de todas las tablas
// como un cuerpo continuo de texto, con solo una nueva línea por cada fila.
txtSaveOptions->set_PreserveTableLayout(preserveTableLayout);

doc->Save(get_ArtifactsDir() + u"TxtSaveOptions.PreserveTableLayout.txt", txtSaveOptions);

System::String docText = System::IO::File::ReadAllText(get_ArtifactsDir() + u"TxtSaveOptions.PreserveTableLayout.txt");

if (preserveTableLayout)
{
    ASSERT_EQ(System::String(u"Row 1, cell 1                                            Row 1, cell 2\r\n") + u"Row 2, cell 1                                            Row 2, cell 2\r\n\r\n", docText);
}
else
{
    ASSERT_EQ(System::String(u"Row 1, cell 1\r") + u"Row 1, cell 2\r" + u"Row 2, cell 1\r" + u"Row 2, cell 2\r\r\n", docText);
}
```

## Ver también

* Class [TxtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
