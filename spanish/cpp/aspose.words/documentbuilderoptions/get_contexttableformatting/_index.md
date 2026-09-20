---
title: "Aspose::Words::DocumentBuilderOptions::get_ContextTableFormatting método"
linktitle: "get_ContextTableFormatting"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::DocumentBuilderOptions::get_ContextTableFormatting método. True si el formato aplicado al contenido de la tabla no afecta al formato del contenido que le sigue. El valor predeterminado es true en C++."
type: docs
weight: 3000
url: /es/cpp/aspose.words/documentbuilderoptions/get_contexttableformatting/
---
## DocumentBuilderOptions::get_ContextTableFormatting method


Verdadero si el formato aplicado al contenido de la tabla no afecta al formato del contenido que le sigue. El valor predeterminado es **true**.

```cpp
bool Aspose::Words::DocumentBuilderOptions::get_ContextTableFormatting() const
```


## Ejemplos



Muestra cómo ignorar el formato de tabla para el contenido posterior.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builderOptions = System::MakeObject<Aspose::Words::DocumentBuilderOptions>();
builderOptions->set_ContextTableFormatting(true);
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc, builderOptions);

// Agrega contenido antes de la tabla.
// El tamaño de fuente predeterminado es 12.
builder->Writeln(u"Font size 12 here.");
builder->StartTable();
builder->InsertCell();
// Cambia el tamaño de fuente dentro de la tabla.
builder->get_Font()->set_Size(5);
builder->Write(u"Font size 5 here");
builder->InsertCell();
builder->Write(u"Font size 5 here");
builder->EndRow();
builder->EndTable();

// Si ContextTableFormatting es verdadero, entonces el formato de la tabla no se aplica al contenido posterior.
// Si ContextTableFormatting es falso, entonces el formato de la tabla se aplica al contenido posterior.
builder->Writeln(u"Font size 12 here.");

doc->Save(get_ArtifactsDir() + u"Table.ContextTableFormatting.docx");
```

## Ver también

* Class [DocumentBuilderOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
