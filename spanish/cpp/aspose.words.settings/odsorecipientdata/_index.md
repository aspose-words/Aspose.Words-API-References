---
title: "Aspose::Words::Settings::OdsoRecipientData clase"
linktitle: "OdsoRecipientData"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Settings::OdsoRecipientData clase. Representa información sobre un único registro dentro de una fuente de datos externa que debe excluirse de la combinación de correspondencia. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 7000
url: /es/cpp/aspose.words.settings/odsorecipientdata/
---
## OdsoRecipientData class


Representa información sobre un único registro dentro de una fuente de datos externa que debe excluirse de la combinación de correspondencia. Para obtener más información, visite el artículo de documentación [Mail Merge and Reporting](https://docs.aspose.com/words/cpp/mail-merge-and-reporting/).

```cpp
class OdsoRecipientData : public System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| [Clone](./clone/)() | Devuelve una clonación profunda de este objeto. |
| [get_Active](./get_active/)() const | Especifica si el registro de la fuente de datos debe importarse a un documento cuando se realiza la combinación de correspondencia. El valor predeterminado es **true**. |
| [get_Column](./get_column/)() const | Especifica la columna dentro de la fuente de datos que contiene datos únicos para el registro actual. El valor predeterminado es 0. |
| [get_Hash](./get_hash/)() const | Representa el código hash de este registro. A veces Microsoft Word utiliza [Hash](./get_hash/) de un registro completo en lugar de un valor [UniqueTag](./get_uniquetag/). El valor predeterminado es 0. |
| [get_UniqueTag](./get_uniquetag/)() const | Especifica el contenido de un registro dado en la columna que contiene datos únicos. El valor predeterminado es **null**. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [OdsoRecipientData](./odsorecipientdata/)() |  |
| [set_Active](./set_active/)(bool) | Especifica si el registro de la fuente de datos debe importarse a un documento cuando se realiza la combinación de correspondencia. El valor predeterminado es **true**. |
| [set_Column](./set_column/)(int32_t) | Especifica la columna dentro de la fuente de datos que contiene datos únicos para el registro actual. El valor predeterminado es 0. |
| [set_Hash](./set_hash/)(int32_t) | Representa el código hash de este registro. A veces Microsoft Word utiliza [Hash](./get_hash/) de un registro completo en lugar de un valor [UniqueTag](./get_uniquetag/). El valor predeterminado es 0. |
| [set_UniqueTag](./set_uniquetag/)(const System::ArrayPtr\<uint8_t\>\&) | Especifica el contenido de un registro dado en la columna que contiene datos únicos. El valor predeterminado es **null**. |
| static [Type](./type/)() |  |
## Observaciones


Si un registro debe fusionarse en un documento combinado, no se necesita información sobre ese registro. Sin embargo, si un registro dado no debe fusionarse en un documento combinado, entonces el valor de la clave única para ese registro debe almacenarse en la propiedad [UniqueTag](./get_uniquetag/) de este objeto para indicar esta exclusión.
## Ver también

* Namespace [Aspose::Words::Settings](../)
* Library [Aspose.Words for C++](../../)
