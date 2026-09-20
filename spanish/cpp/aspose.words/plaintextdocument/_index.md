---
title: "Clase Aspose::Words::PlainTextDocument"
linktitle: "PlainTextDocument"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Clase Aspose::Words::PlainTextDocument. Permite extraer la representación de texto sin formato del contenido del documento. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 50000
url: /es/cpp/aspose.words/plaintextdocument/
---
## PlainTextDocument class


Permite extraer una representación de texto sin formato del contenido del documento. Para obtener más información, visite el artículo de documentación [Working with Text Document](https://docs.aspose.com/words/cpp/working-with-text-document/).

```cpp
class PlainTextDocument : public System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| [get_BuiltInDocumentProperties](./get_builtindocumentproperties/)() const | Obtiene [BuiltInDocumentProperties](./get_builtindocumentproperties/) del documento. |
| [get_CustomDocumentProperties](./get_customdocumentproperties/)() const | Obtiene [CustomDocumentProperties](./get_customdocumentproperties/) del documento. |
| [get_Text](./get_text/)() const | Obtiene el contenido textual del documento concatenado como una cadena. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [PlainTextDocument](./plaintextdocument/)(const System::String\&) | Crea un documento de texto sin formato a partir de un archivo. Detecta automáticamente el formato del archivo. |
| [PlainTextDocument](./plaintextdocument/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | Crea un documento de texto sin formato a partir de un archivo. Permite especificar opciones adicionales, como una contraseña de cifrado. |
| [PlainTextDocument](./plaintextdocument/)(const System::SharedPtr\<System::IO::Stream\>\&) | Crea un documento de texto sin formato a partir de un flujo. Detecta automáticamente el formato del archivo. |
| [PlainTextDocument](./plaintextdocument/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | Crea un documento de texto sin formato a partir de un flujo. Permite especificar opciones adicionales, como una contraseña de cifrado. |
| [PlainTextDocument](./plaintextdocument/)(std::istream\&) |  |
| [PlainTextDocument](./plaintextdocument/)(std::istream\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) |  |
| static [Type](./type/)() |  |

## Ejemplos



Muestra cómo cargar el contenido de un documento Microsoft Word en texto sin formato.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

doc->Save(get_ArtifactsDir() + u"PlainTextDocument.Load.docx");

auto plaintext = System::MakeObject<Aspose::Words::PlainTextDocument>(get_ArtifactsDir() + u"PlainTextDocument.Load.docx");

ASSERT_EQ(u"Hello world!", plaintext->get_Text().Trim());
```

## Ver también

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
