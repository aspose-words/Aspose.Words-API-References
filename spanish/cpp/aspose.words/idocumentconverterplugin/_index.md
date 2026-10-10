---
title: "interfaz Aspose::Words::IDocumentConverterPlugin"
linktitle: "IDocumentConverterPlugin"
second_title: "Referencia de API de Aspose.Words para C++"
description: "interfaz Aspose::Words::IDocumentConverterPlugin. Define una interfaz para un complemento de conversor externo en C++."
type: docs
weight: 76250
url: /es/cpp/aspose.words/idocumentconverterplugin/
---
## IDocumentConverterPlugin interface


Define una interfaz para un complemento de convertidor externo.

```cpp
class IDocumentConverterPlugin : public virtual System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| virtual [Convert](./convert/)(System::SharedPtr\<System::IO::Stream\>, System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>, System::SharedPtr\<System::IO::Stream\>, System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>) | Convierte el documento usando los flujos de entrada y salida especificados y las opciones de guardado. |
| virtual [ConvertToImages](./converttoimages/)(System::SharedPtr\<System::IO::Stream\>, System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>, System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>) | Convierte páginas del documento desde el flujo de entrada a una matriz de imágenes. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Ver también

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
