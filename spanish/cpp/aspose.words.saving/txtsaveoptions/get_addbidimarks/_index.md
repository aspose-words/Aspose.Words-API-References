---
title: "Aspose::Words::Saving::TxtSaveOptions::get_AddBidiMarks método"
linktitle: "get_AddBidiMarks"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::TxtSaveOptions::get_AddBidiMarks método. Especifica si se deben agregar marcas bidireccionales antes de cada ejecución BiDi al exportar en formato de texto plano. El valor predeterminado es false en C++."
type: docs
weight: 3000
url: /es/cpp/aspose.words.saving/txtsaveoptions/get_addbidimarks/
---
## TxtSaveOptions::get_AddBidiMarks method


Especifica si se deben agregar marcas bidireccionales antes de cada ejecución BiDi al exportar en formato de texto plano. El valor predeterminado es **false**.

```cpp
bool Aspose::Words::Saving::TxtSaveOptions::get_AddBidiMarks() const
```


## Ejemplos



Muestra cómo insertar el carácter Unicode 'RIGHT-TO-LEFT MARK' (U+200F) antes de cada [Run](../../../aspose.words/run/) bidireccional en el texto.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Hello world!");
builder->get_ParagraphFormat()->set_Bidi(true);
builder->Writeln(u"שלום עולם!");
builder->Writeln(u"مرحبا بالعالم!");

// Cree un objeto "TxtSaveOptions", que podemos pasar al método "Save" del documento
// para modificar cómo guardamos el documento en texto plano.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::TxtSaveOptions>();
saveOptions->set_Encoding(System::Text::Encoding::get_Unicode());

// Establezca la propiedad "AddBidiMarks" en "true" para agregar marcas antes de las ejecuciones
// con texto de derecha a izquierda para indicar el hecho.
// Establezca la propiedad "AddBidiMarks" en "false" para escribir todo de izquierda a derecha
// y ejecuciones de derecha a izquierda por igual sin nada que indique cuál es cuál.
saveOptions->set_AddBidiMarks(addBidiMarks);

doc->Save(get_ArtifactsDir() + u"TxtSaveOptions.AddBidiMarks.txt", saveOptions);

System::String docText = System::Text::Encoding::get_Unicode()->GetString(System::IO::File::ReadAllBytes(get_ArtifactsDir() + u"TxtSaveOptions.AddBidiMarks.txt"));

if (addBidiMarks)
{
    ASSERT_EQ(u"\ufeffHello world!‎\r\nשלום עולם!‏\r\nمرحبا بالعالم!‏\r\n\r\n", docText);
    ASSERT_TRUE(docText.Contains(u"\u200f"));
}
else
{
    ASSERT_EQ(u"\ufeffHello world!\r\nשלום עולם!\r\nمرحبا بالعالم!\r\n\r\n", docText);
    ASSERT_FALSE(docText.Contains(u"\u200f"));
}
```

## Ver también

* Class [TxtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
