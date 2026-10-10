---
title: "Aspose::Words::MailMerging::MailMerge::Execute método"
linktitle: "Ejecutar"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::MailMerging::MailMerge::Execute método. Realiza una operación de combinación de correspondencia para un solo registro en C++."
type: docs
weight: 3000
url: /es/cpp/aspose.words.mailmerging/mailmerge/execute/
---
## MailMerge::Execute(const System::ArrayPtr\<System::String\>\&, const System::ArrayPtr\<System::SharedPtr\<System::Object\>\>\&) method


Realiza una operación de combinación de correspondencia para un solo registro.

```cpp
void Aspose::Words::MailMerging::MailMerge::Execute(const System::ArrayPtr<System::String> &fieldNames, const System::ArrayPtr<System::SharedPtr<System::Object>> &values)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| fieldNames | const System::ArrayPtr\<System::String\>\& | Arreglo de nombres de campos de combinación. Los nombres de campo no distinguen entre mayúsculas y minúsculas. Si se encuentra un nombre de campo que no está presente en el documento, se ignora. |
| values | const System::ArrayPtr\\<System::SharedPtr\\<System::Object\\>\\>\\& | Arreglo de valores a insertar en los campos de combinación. El número de elementos en este arreglo debe ser el mismo que el número de elementos en *fieldNames*. |
## Observaciones


Utilice este método para rellenar los campos de combinación en el documento con valores de un arreglo de objetos.

Este método combina datos solo para un registro. El arreglo de nombres de campo y el arreglo de valores representan los datos de un único registro.

Este método no utiliza regiones de combinación de correspondencia.

Este método ignora la opción [RemoveUnusedRegions](../../mailmergecleanupoptions/).

## Ejemplos



Muestra cómo combinar una imagen desde una URI como datos de combinación de correspondencia en un MERGEFIELD.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Los MERGEFIELDs con etiquetas \"Image:\" recibirán una imagen durante una combinación de correspondencia.
// La cadena después de los dos puntos en la etiqueta \"Image:\" corresponde a un nombre de columna
// en la fuente de datos cuyas celdas contienen URIs de archivos de imagen.
builder->InsertField(u"MERGEFIELD  Image:logo_FromWeb ");
builder->InsertField(u"MERGEFIELD  Image:logo_FromFileSystem ");

// Cree una fuente de datos que contenga URIs de imágenes que vamos a combinar.
// Una URI puede ser una URL web que apunta a una imagen, o el nombre de archivo en el sistema de archivos local de un archivo de imagen.
System::ArrayPtr<System::String> columns = System::MakeArray<System::String>({u"logo_FromWeb", u"logo_FromFileSystem"});
System::ArrayPtr<System::SharedPtr<System::Object>> URIs = System::MakeArray<System::SharedPtr<System::Object>>({System::ExplicitCast<System::Object>(get_ImageUrl()), System::ExplicitCast<System::Object>(get_ImageDir() + u"Logo.jpg")});

// Ejecute una combinación de correspondencia en una fuente de datos con una fila.
doc->get_MailMerge()->Execute(columns, URIs);

doc->Save(get_ArtifactsDir() + u"MailMergeEvent.ImageFromUrl.docx");
```

## Ver también

* Class [MailMerge](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
## MailMerge::Execute(const System::SharedPtr\<Aspose::Words::MailMerging::IMailMergeDataSource\>\&) method


Realiza una combinación de correspondencia a partir de una fuente de datos personalizada.

```cpp
void Aspose::Words::MailMerging::MailMerge::Execute(const System::SharedPtr<Aspose::Words::MailMerging::IMailMergeDataSource> &dataSource)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| dataSource | const System::SharedPtr\<Aspose::Words::MailMerging::IMailMergeDataSource\>\& | Un objeto que implementa la interfaz personalizada de fuente de datos de combinación de correspondencia. |
## Observaciones


Utilice este método para rellenar los campos de combinación de correspondencia en el documento con valores de cualquier fuente de datos, como una lista, una tabla hash o objetos. Necesita escribir su propia clase que implemente la interfaz [IMailMergeDataSource](../../imailmergedatasource/).

Puede usar este método solo cuando [IsBidiTextSupportedOnUpdate](../../../aspose.words.fields/fieldoptions/get_isbiditextsupportedonupdate/) es **false**, es decir, no necesita compatibilidad con idiomas de derecha a izquierda (como árabe o hebreo).

Este método ignora la opción [RemoveUnusedRegions](../../mailmergecleanupoptions/).

## Ver también

* Interface [IMailMergeDataSource](../../imailmergedatasource/)
* Class [MailMerge](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
