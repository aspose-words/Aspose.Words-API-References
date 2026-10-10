---
title: "Interfaz Aspose::Words::IDocumentProcessorPlugin"
linktitle: "IDocumentProcessorPlugin"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Interfaz Aspose::Words::IDocumentProcessorPlugin. Define una interfaz para un complemento externo de procesador de documentos en C++."
type: docs
weight: 76750
url: /es/cpp/aspose.words/idocumentprocessorplugin/
---
## IDocumentProcessorPlugin interface


Define una interfaz para un complemento de procesador de documentos externo.

```cpp
class IDocumentProcessorPlugin : public virtual System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| virtual [Append](./append/)(System::SharedPtr\<System::IO::Stream\>, System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>) | Adjunte el documento cargándolo con las opciones de carga especificadas. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Load](./load/)(System::SharedPtr\<System::IO::Stream\>, System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>) | Cargue el documento usando las opciones de carga especificadas. |
| virtual [Save](./save/)(System::SharedPtr\<System::IO::Stream\>, System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>) | Guarde el documento cargado mediante el método [Load()](./load/) en el flujo de salida usando las opciones de guardado especificadas. |
| virtual [SetImageWatermark](./setimagewatermark/)(System::SharedPtr\<System::IO::Stream\>, System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>) | Agrega una marca de agua de imagen en cada página del documento cargado mediante el método [Load()](./load/). |
| virtual [SetTextWatermark](./settextwatermark/)(System::String, System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>) | Agrega una marca de agua de texto en cada página del documento cargado mediante el método [Load()](./load/). |
| virtual [ToDocument](./todocument/)() | Analiza el documento cargado mediante el método [Load()](./load/) en un objeto [Document](../document/). |
| virtual [ToPages](./topages/)(System::SharedPtr\<Aspose::Words::Saving::FixedPageSaveOptions\>) | Guarda cada página del documento cargado mediante el método [Load()](./load/) usando las opciones de guardado de página fija especificadas. |
| static [Type](./type/)() |  |
## Ver también

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
