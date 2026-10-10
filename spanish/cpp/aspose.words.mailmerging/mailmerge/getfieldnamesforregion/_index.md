---
title: "Método Aspose::Words::MailMerging::MailMerge::GetFieldNamesForRegion"
linktitle: "GetFieldNamesForRegion"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::MailMerging::MailMerge::GetFieldNamesForRegion. Devuelve una colección de nombres de campos de combinación de correspondencia disponibles en la región en C++."
type: docs
weight: 22000
url: /es/cpp/aspose.words.mailmerging/mailmerge/getfieldnamesforregion/
---
## MailMerge::GetFieldNamesForRegion(const System::String\&) method


Devuelve una colección de nombres de campos de combinación de correspondencia disponibles en la región.

```cpp
System::ArrayPtr<System::String> Aspose::Words::MailMerging::MailMerge::GetFieldNamesForRegion(const System::String &regionName)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| regionName | const System::String\& | Nombre de la región (sin distinción de mayúsculas/minúsculas). |
## Observaciones


Devuelve los nombres completos de los campos de combinación, incluido el prefijo opcional. No elimina los nombres de campo duplicados.

Si el documento contiene varias regiones con el mismo nombre, se procesa la primera región.

Se crea una nueva matriz de cadenas en cada llamada.

## Ver también

* Class [MailMerge](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
## MailMerge::GetFieldNamesForRegion(const System::String\&, int32_t) method


Devuelve una colección de nombres de campos de combinación de correspondencia disponibles en la región.

```cpp
System::ArrayPtr<System::String> Aspose::Words::MailMerging::MailMerge::GetFieldNamesForRegion(const System::String &regionName, int32_t regionIndex)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| regionName | const System::String\& | Nombre de la región (sin distinción de mayúsculas/minúsculas). |
| regionIndex | int32_t | Índice de la región (basado en cero). |
## Observaciones


Devuelve los nombres completos de los campos de combinación, incluido el prefijo opcional. No elimina los nombres de campo duplicados.

Si el documento contiene varias regiones con el mismo nombre, se procesa la N‑ésima región (basada en cero).

Se crea una nueva matriz de cadenas en cada llamada.

## Ver también

* Class [MailMerge](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
