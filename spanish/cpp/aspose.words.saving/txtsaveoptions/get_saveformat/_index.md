---
title: "Aspose::Words::Saving::TxtSaveOptions::get_SaveFormat método"
linktitle: "get_SaveFormat"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::TxtSaveOptions::get_SaveFormat método. Especifica el formato en el que se guardará el documento si se utiliza este objeto de opciones de guardado. Sólo puede ser Text en C++."
type: docs
weight: 7000
url: /es/cpp/aspose.words.saving/txtsaveoptions/get_saveformat/
---
## TxtSaveOptions::get_SaveFormat method


Especifica el formato en el que se guardará el documento si se utiliza este objeto de opciones de guardado. Sólo puede ser [Text](../../../aspose.words/saveformat/).

```cpp
Aspose::Words::SaveFormat Aspose::Words::Saving::TxtSaveOptions::get_SaveFormat() override
```


## Ejemplos



Muestra cómo guardar un documento .txt con un salto de párrafo personalizado.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Paragraph 1.");
builder->Writeln(u"Paragraph 2.");
builder->Write(u"Paragraph 3.");

// Cree un objeto "TxtSaveOptions", que podemos pasar al método "Save" del documento
// para modificar cómo guardamos el documento en texto plano.
auto txtSaveOptions = System::MakeObject<Aspose::Words::Saving::TxtSaveOptions>();

ASSERT_EQ(Aspose::Words::SaveFormat::Text, txtSaveOptions->get_SaveFormat());

// Establezca "ParagraphBreak" a un valor personalizado que deseamos colocar al final de cada párrafo.
txtSaveOptions->set_ParagraphBreak(u" End of paragraph.\n\n\t");

doc->Save(get_ArtifactsDir() + u"TxtSaveOptions.ParagraphBreak.txt", txtSaveOptions);

System::String docText = System::IO::File::ReadAllText(get_ArtifactsDir() + u"TxtSaveOptions.ParagraphBreak.txt");

ASSERT_EQ(System::String(u"Paragraph 1. End of paragraph.\n\n\t") + u"Paragraph 2. End of paragraph.\n\n\t" + u"Paragraph 3. End of paragraph.\n\n\t", docText);
```

## Ver también

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [TxtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
