---
title: XmlDataSource
linktitle: XmlDataSource
articleTitle: XmlDataSource
second_title: Aspose.Words para .NET
description: Cree una fuente de datos potente sin esfuerzo con el constructor XmlDataSource, cargando datos XML utilizando opciones predeterminadas optimizadas para una integración perfecta.
type: docs
weight: 10
url: /es/net/aspose.words.reporting/xmldatasource/xmldatasource/
---
## XmlDataSource(*string*) {#constructor_4}

Crea una nueva fuente de datos con datos de un archivo XML utilizando las opciones predeterminadas para la carga de datos XML.

```csharp
public XmlDataSource(string xmlPath)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| xmlPath | String | La ruta al archivo XML que se utilizará como fuente de datos. |

## Ejemplos

Muestra cómo utilizar XML como fuente de datos (cadena).

```csharp
Document doc = new Document(MyDir + "Reporting engine template - XML data destination.docx");

XmlDataSource dataSource = new XmlDataSource(MyDir + "List of people.xml");
BuildReport(doc, dataSource, "persons");

doc.Save(ArtifactsDir + "ReportingEngine.XmlDataString.docx");
```

### Ver también

* class [XmlDataSource](../)
* espacio de nombres [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* asamblea [Aspose.Words](../../../)

---

## XmlDataSource(*Stream*) {#constructor}

Crea una nueva fuente de datos con datos de un flujo XML utilizando las opciones predeterminadas para la carga de datos XML.

```csharp
public XmlDataSource(Stream xmlStream)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| xmlStream | Stream | El flujo de datos XML que se utilizará como fuente de datos. |

## Ejemplos

Muestra cómo utilizar XML como fuente de datos (flujo).

```csharp
Document doc = new Document(MyDir + "Reporting engine template - XML data destination.docx");

using (FileStream stream = File.OpenRead(MyDir + "List of people.xml"))
{
    XmlDataSource dataSource = new XmlDataSource(stream);
    BuildReport(doc, dataSource, "persons");
}

doc.Save(ArtifactsDir + "ReportingEngine.XmlDataStream.docx");
```

### Ver también

* class [XmlDataSource](../)
* espacio de nombres [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* asamblea [Aspose.Words](../../../)

---

## XmlDataSource(*string, string*) {#constructor_6}

Crea una nueva fuente de datos con datos de un archivo XML mediante un archivo de definición de esquema XML. Las opciones predeterminadas se utilizan para la carga de datos XML.

```csharp
public XmlDataSource(string xmlPath, string xmlSchemaPath)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| xmlPath | String | La ruta al archivo XML que se utilizará como fuente de datos. |
| xmlSchemaPath | String | La ruta al archivo de definición de esquema XML que proporciona el esquema para el archivo XML . |

### Ver también

* class [XmlDataSource](../)
* espacio de nombres [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* asamblea [Aspose.Words](../../../)

---

## XmlDataSource(*Stream, Stream*) {#constructor_2}

Crea una nueva fuente de datos con datos de un flujo XML mediante un flujo de definición de esquema XML. Las opciones predeterminadas se utilizan para la carga de datos XML.

```csharp
public XmlDataSource(Stream xmlStream, Stream xmlSchemaStream)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| xmlStream | Stream | El flujo de datos XML que se utilizará como fuente de datos. |
| xmlSchemaStream | Stream | La secuencia de definición de esquema XML que proporciona el esquema para los datos XML. |

### Ver también

* class [XmlDataSource](../)
* espacio de nombres [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* asamblea [Aspose.Words](../../../)

---

## XmlDataSource(*string, [XmlDataLoadOptions](../../xmldataloadoptions/)*) {#constructor_5}

Crea una nueva fuente de datos con datos de un archivo XML utilizando las opciones especificadas para la carga de datos XML.

```csharp
public XmlDataSource(string xmlPath, XmlDataLoadOptions options)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| xmlPath | String | La ruta al archivo XML que se utilizará como fuente de datos. |
| options | XmlDataLoadOptions | Opciones para la carga de datos XML. |

### Ver también

* class [XmlDataLoadOptions](../../xmldataloadoptions/)
* class [XmlDataSource](../)
* espacio de nombres [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* asamblea [Aspose.Words](../../../)

---

## XmlDataSource(*Stream, [XmlDataLoadOptions](../../xmldataloadoptions/)*) {#constructor_1}

Crea una nueva fuente de datos con datos de una secuencia XML utilizando las opciones especificadas para la carga de datos XML.

```csharp
public XmlDataSource(Stream xmlStream, XmlDataLoadOptions options)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| xmlStream | Stream | El flujo de datos XML que se utilizará como fuente de datos. |
| options | XmlDataLoadOptions | Opciones para la carga de datos XML. |

### Ver también

* class [XmlDataLoadOptions](../../xmldataloadoptions/)
* class [XmlDataSource](../)
* espacio de nombres [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* asamblea [Aspose.Words](../../../)

---

## XmlDataSource(*string, string, [XmlDataLoadOptions](../../xmldataloadoptions/)*) {#constructor_7}

Crea una nueva fuente de datos con datos de un archivo XML mediante un archivo de definición de esquema XML. Las opciones especificadas se utilizan para la carga de datos XML.

```csharp
public XmlDataSource(string xmlPath, string xmlSchemaPath, XmlDataLoadOptions options)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| xmlPath | String | La ruta al archivo XML que se utilizará como fuente de datos. |
| xmlSchemaPath | String | La ruta al archivo de definición de esquema XML que proporciona el esquema para el archivo XML . |
| options | XmlDataLoadOptions | Opciones para la carga de datos XML. |

### Ver también

* class [XmlDataLoadOptions](../../xmldataloadoptions/)
* class [XmlDataSource](../)
* espacio de nombres [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* asamblea [Aspose.Words](../../../)

---

## XmlDataSource(*Stream, Stream, [XmlDataLoadOptions](../../xmldataloadoptions/)*) {#constructor_3}

Crea una nueva fuente de datos con datos de una secuencia XML mediante una secuencia de definición de esquema XML. Las opciones especificadas se utilizan para la carga de datos XML.

```csharp
public XmlDataSource(Stream xmlStream, Stream xmlSchemaStream, XmlDataLoadOptions options)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| xmlStream | Stream | El flujo de datos XML que se utilizará como fuente de datos. |
| xmlSchemaStream | Stream | La secuencia de definición de esquema XML que proporciona el esquema para los datos XML. |
| options | XmlDataLoadOptions | Opciones para la carga de datos XML. |

### Ver también

* class [XmlDataLoadOptions](../../xmldataloadoptions/)
* class [XmlDataSource](../)
* espacio de nombres [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* asamblea [Aspose.Words](../../../)
