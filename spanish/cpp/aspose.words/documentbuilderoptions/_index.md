---
title: "Clase Aspose::Words::DocumentBuilderOptions"
linktitle: "DocumentBuilderOptions"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Clase Aspose::Words::DocumentBuilderOptions. Permite especificar opciones adicionales para el proceso de construcción del documento en C++."
type: docs
weight: 22500
url: /es/cpp/aspose.words/documentbuilderoptions/
---
## DocumentBuilderOptions class


Permite especificar opciones adicionales para el proceso de creación del documento.

```cpp
class DocumentBuilderOptions : public System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| [DocumentBuilderOptions](./documentbuilderoptions/)() |  |
| [get_ContextTableFormatting](./get_contexttableformatting/)() const | Verdadero si el formato aplicado al contenido de la tabla no afecta al formato del contenido que le sigue. El valor predeterminado es **true**. |
| [get_DesignMode](./get_designmode/)() const | Corresponde al Modo de diseño en Microsoft Word. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_ContextTableFormatting](./set_contexttableformatting/)(bool) | Método setter para [Aspose::Words::DocumentBuilderOptions::get_ContextTableFormatting](./get_contexttableformatting/). |
| [set_DesignMode](./set_designmode/)(bool) | Corresponde al Modo de diseño en Microsoft Word. |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
