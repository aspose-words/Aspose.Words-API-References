---
title: Aspose.Words.Markup
linktitle: Aspose.Words.Markup
articleTitle: Aspose.Words.Markup
second_title: Aspose.Words para .NET
description: Descubra el espacio de nombres Aspose.Words.Markup, que incluye clases personalizables para etiquetas inteligentes, XML y controles de contenido para mejorar la gestión de sus documentos.
type: docs
weight: 180
url: /es/net/aspose.words.markup/
---
El**Aspose.Words.Marcado** El espacio de nombres contiene clases que representan la semántica definida por el cliente en un documento: etiquetas inteligentes, XML personalizado y etiquetas de documentos estructurados (controles de contenido).

## Clases

| Clase | Descripción |
| --- | --- |
| [CustomPart](./custompart/) | Representa una parte personalizada (contenido arbitrario), que no está definida por el estándar ISO/IEC 29500. |
| [CustomPartCollection](./custompartcollection/) | Representa una colección de[`CustomPart`](../aspose.words.markup/custompart/) objetos. |
| [CustomXmlPart](./customxmlpart/) | Representa una parte de almacenamiento de datos XML personalizados (datos XML personalizados dentro de un paquete). |
| [CustomXmlPartCollection](./customxmlpartcollection/) | Representa una colección de componentes XML personalizados. Los elementos son[`CustomXmlPart`](../aspose.words.markup/customxmlpart/) objetos. |
| [CustomXmlProperty](./customxmlproperty/) | Representa un único atributo XML personalizado o una propiedad de etiqueta inteligente. |
| [CustomXmlPropertyCollection](./customxmlpropertycollection/) | Representa una colección de atributos XML personalizados o propiedades de etiquetas inteligentes. |
| [CustomXmlSchemaCollection](./customxmlschemacollection/) | Una colección de cadenas que representan esquemas XML asociados con una parte XML personalizada. |
| [SdtListItem](./sdtlistitem/) | Este elemento especifica un solo elemento de lista dentro de una lista padreComboBox oDropDownList etiqueta de documento estructurado. |
| [SdtListItemCollection](./sdtlistitemcollection/) | Proporciona acceso a[`SdtListItem`](../aspose.words.markup/sdtlistitem/) elementos de una etiqueta de documento estructurado. |
| [SmartTag](./smarttag/) | Este elemento especifica la presencia de una etiqueta inteligente alrededor de una o más estructuras en línea (ejecuciones, imágenes, campos, etc.) dentro de un párrafo. |
| [StructuredDocumentTag](./structureddocumenttag/) | Representa una etiqueta de documento estructurado (SDT o control de contenido) en un documento. |
| [StructuredDocumentTagCollection](./structureddocumenttagcollection/) | Una colección de[`IStructuredDocumentTag`](../aspose.words.markup/istructureddocumenttag/) instancias que representan las etiquetas de documento estructurado en el rango especificado. |
| [StructuredDocumentTagRangeEnd](./structureddocumenttagrangeend/) | Representa un final de**a distancia** Etiqueta de documento estructurado que acepta contenido de varias secciones. Véase también[`StructuredDocumentTagRangeStart`](../aspose.words.markup/structureddocumenttagrangestart/) nodo. |
| [StructuredDocumentTagRangeStart](./structureddocumenttagrangestart/) | Representa un inicio de**a distancia** Etiqueta de documento estructurado que acepta contenido de varias secciones. Véase también[`StructuredDocumentTagRangeEnd`](../aspose.words.markup/structureddocumenttagrangeend/) . |
| [XmlMapping](./xmlmapping/) | Especifica la información que se utiliza para establecer una asignación entre la etiqueta de documento estructurado parent y un elemento XML almacenado dentro de una parte de datos XML personalizada en el documento. |
## Interfaces

| Interfaz | Descripción |
| --- | --- |
| [IStructuredDocumentTag](./istructureddocumenttag/) | Interfaz para definir datos comunes para[`StructuredDocumentTag`](../aspose.words.markup/structureddocumenttag/) y[`StructuredDocumentTagRangeStart`](../aspose.words.markup/structureddocumenttagrangestart/) . |
## Enumeración

| Enumeración | Descripción |
| --- | --- |
| [MarkupLevel](./markuplevel/) | Especifica el nivel en el árbol del documento donde se encuentra un documento en particular.[`StructuredDocumentTag`](../aspose.words.markup/structureddocumenttag/) puede ocurrir. |
| [SdtAppearance](./sdtappearance/) | Especifica la apariencia de una etiqueta de documento estructurado. |
| [SdtCalendarType](./sdtcalendartype/) | Especifica los posibles tipos de calendarios que se pueden utilizar para especificar[`CalendarType`](../aspose.words.markup/structureddocumenttag/calendartype/) en un documento Office Open XML. |
| [SdtDateStorageFormat](./sdtdatestorageformat/) | Especifica cómo se almacena/recupera la fecha de un SDT de fecha cuando el SDT está vinculado a un nodo XML en el almacén de datos del documento. |
| [SdtType](./sdttype/) | Especifica el tipo de un nodo de etiqueta de documento estructurado (SDT). |
