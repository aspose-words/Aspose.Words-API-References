---
title: "Interfaz Aspose::Words::MailMerging::IMailMergeDataSource"
linktitle: "IMailMergeDataSource"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Interfaz Aspose::Words::MailMerging::IMailMergeDataSource. Implemente esta interfaz para permitir la combinación de correspondencia desde una fuente de datos personalizada, como una lista de objetos. Los datos maestro‑detalle también son compatibles en C++."
type: docs
weight: 9000
url: /es/cpp/aspose.words.mailmerging/imailmergedatasource/
---
## IMailMergeDataSource interface


Implemente esta interfaz para permitir la combinación de correspondencia desde una fuente de datos personalizada, como una lista de objetos. También se admite datos maestro‑detalle.

```cpp
class IMailMergeDataSource : public virtual System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| virtual [get_TableName](./get_tablename/)() | Devuelve el nombre de la fuente de datos. |
| virtual [GetChildDataSource](./getchilddatasource/)(System::String) | El motor de combinación de correspondencia Aspose.Words invoca este método cuando encuentra el inicio de una región de combinación de correspondencia anidada. |
| [GetType](./gettype/)() const override |  |
| virtual [GetValue](./getvalue/)(System::String, System::SharedPtr\<System::Object\>\&) |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [MoveNext](./movenext/)() | Avanza al siguiente registro en la fuente de datos. |
| static [Type](./type/)() |  |
## Observaciones


Cuando se crea una fuente de datos, debe inicializarse para apuntar a BOF (antes del primer registro). El motor de combinación de correspondencia Aspose.Words invocará [MoveNext](./movenext/) para avanzar al siguiente registro y luego invocará [GetValue()](./getvalue/) para cada campo de combinación que encuentre en el documento o en la región de combinación actual.

## Ver también

* Namespace [Aspose::Words::MailMerging](../)
* Library [Aspose.Words for C++](../../)
