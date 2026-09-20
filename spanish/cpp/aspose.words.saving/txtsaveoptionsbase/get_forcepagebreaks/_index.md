---
title: "Aspose::Words::Saving::TxtSaveOptionsBase::get_ForcePageBreaks método"
linktitle: "get_ForcePageBreaks"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::TxtSaveOptionsBase::get_ForcePageBreaks método. Permite especificar si los saltos de página deben preservarse durante la exportación. El valor predeterminado es false en C++."
type: docs
weight: 5000
url: /es/cpp/aspose.words.saving/txtsaveoptionsbase/get_forcepagebreaks/
---
## TxtSaveOptionsBase::get_ForcePageBreaks method


Permite especificar si los saltos de página deben preservarse durante la exportación. El valor predeterminado es **false**.

```cpp
bool Aspose::Words::Saving::TxtSaveOptionsBase::get_ForcePageBreaks() const
```


## Ejemplos



Muestra cómo especificar si se deben preservar los saltos de página al exportar un documento a texto sin formato.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Page 1");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 2");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 3");

// Cree un objeto "TxtSaveOptions", que podemos pasar al método "Save" del documento
// método para modificar cómo guardamos el documento en texto sin formato.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::TxtSaveOptions>();

// Los objetos "Document" de Aspose.Words tienen saltos de página, al igual que los documentos de Microsoft Word.
// Los formatos de guardado como ".txt" son un cuerpo continuo de texto sin saltos de página.
// Establezca la propiedad "ForcePageBreaks" a "true" para preservar todos los saltos de página en forma de caracteres '\\f'.
// Establezca la propiedad "ForcePageBreaks" a "false" para descartar todos los saltos de página.
saveOptions->set_ForcePageBreaks(forcePageBreaks);

doc->Save(get_ArtifactsDir() + u"TxtSaveOptions.PageBreaks.txt", saveOptions);

// Si cargamos un documento de texto sin formato con saltos de página,
// el objeto "Document" los usará para dividir el cuerpo en páginas.
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"TxtSaveOptions.PageBreaks.txt");

ASSERT_EQ(forcePageBreaks ? 3 : 1, doc->get_PageCount());
```

## Ver también

* Class [TxtSaveOptionsBase](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
