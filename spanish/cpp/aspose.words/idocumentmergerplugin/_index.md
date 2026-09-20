---
title: "interfaz Aspose::Words::IDocumentMergerPlugin"
linktitle: "IDocumentMergerPlugin"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::IDocumentMergerPlugin interface. Define una interfaz para complementos externos de fusión que pueden combinar documentos PDF en C++."
type: docs
weight: 76500
url: /es/cpp/aspose.words/idocumentmergerplugin/
---
## IDocumentMergerPlugin interface


Define una interfaz para un complemento de fusión externo que puede combinar documentos PDF.

```cpp
class IDocumentMergerPlugin : public virtual System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Merge](./merge/)(System::SharedPtr\<System::IO::Stream\>, System::ArrayPtr\<System::SharedPtr\<System::IO::Stream\>\>, System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\>) | Combina los documentos PDF de entrada proporcionados en un único documento PDF de salida utilizando los flujos de entrada y salida especificados. |
| static [Type](./type/)() |  |
## Ver también

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
