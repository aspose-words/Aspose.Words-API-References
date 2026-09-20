---
title: "Método Aspose::Words::MailMerging::MailMerge::ExecuteWithRegions"
linktitle: "ExecuteWithRegions"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::MailMerging::MailMerge::ExecuteWithRegions. Realiza una combinación de correspondencia a partir de una fuente de datos personalizada con regiones de combinación de correspondencia en C++."
type: docs
weight: 4000
url: /es/cpp/aspose.words.mailmerging/mailmerge/executewithregions/
---
## MailMerge::ExecuteWithRegions(const System::SharedPtr\<Aspose::Words::MailMerging::IMailMergeDataSource\>\&) method


Realiza una combinación de correspondencia a partir de una fuente de datos personalizada con regiones de combinación de correspondencia.

```cpp
void Aspose::Words::MailMerging::MailMerge::ExecuteWithRegions(const System::SharedPtr<Aspose::Words::MailMerging::IMailMergeDataSource> &dataSource)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| dataSource | const System::SharedPtr\<Aspose::Words::MailMerging::IMailMergeDataSource\>\& | Un objeto que implementa la interfaz personalizada de fuente de datos de combinación de correspondencia. |
## Observaciones


Utilice este método para rellenar los campos de combinación de correspondencia en el documento con valores de cualquier fuente de datos personalizada, como un archivo XML o colecciones de objetos de negocio. Necesita escribir su propia clase que implemente la interfaz [IMailMergeDataSource](../../imailmergedatasource/).

Puede usar este método solo cuando [IsBidiTextSupportedOnUpdate](../../../aspose.words.fields/fieldoptions/get_isbiditextsupportedonupdate/) es **false**, es decir, no necesita compatibilidad con idiomas de derecha a izquierda (como árabe o hebreo).

## Ver también

* Interface [IMailMergeDataSource](../../imailmergedatasource/)
* Class [MailMerge](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
## MailMerge::ExecuteWithRegions(const System::SharedPtr\<Aspose::Words::MailMerging::IMailMergeDataSourceRoot\>\&) method


Realiza una combinación de correspondencia a partir de una fuente de datos personalizada con regiones de combinación de correspondencia.

```cpp
void Aspose::Words::MailMerging::MailMerge::ExecuteWithRegions(const System::SharedPtr<Aspose::Words::MailMerging::IMailMergeDataSourceRoot> &dataSourceRoot)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| dataSourceRoot | const System::SharedPtr\<Aspose::Words::MailMerging::IMailMergeDataSourceRoot\>\& | Un objeto que implementa la interfaz raíz de fuente de datos personalizada para combinación de correspondencia. |
## Observaciones


Utilice este método para rellenar los campos de combinación de correspondencia en el documento con valores de cualquier fuente de datos personalizada, como un archivo XML o colecciones de objetos de negocio. Necesita escribir sus propias clases que implementen las interfaces [IMailMergeDataSourceRoot](../../imailmergedatasourceroot/) y [IMailMergeDataSource](../../imailmergedatasource/).

Puede usar este método solo cuando [IsBidiTextSupportedOnUpdate](../../../aspose.words.fields/fieldoptions/get_isbiditextsupportedonupdate/) es **false**, es decir, no necesita compatibilidad con idiomas de derecha a izquierda (como árabe o hebreo).

## Ver también

* Interface [IMailMergeDataSourceRoot](../../imailmergedatasourceroot/)
* Class [MailMerge](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
