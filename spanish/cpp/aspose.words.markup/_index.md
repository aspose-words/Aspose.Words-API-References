---
title: "Espacio de nombres Aspose::Words::Markup"
linktitle: "Aspose::Words::Markup"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Espacio de nombres Aspose::Words::Markup. El espacio de nombres Aspose.Words.Markup contiene clases que representan semánticas definidas por el cliente en un documento: etiquetas inteligentes, XML personalizado y etiquetas estructuradas de documento (controles de contenido) en C++."
type: docs
weight: 14000
url: /es/cpp/aspose.words.markup/
---

El espacio de nombres **Aspose.Words.Markup** contiene clases que representan semánticas definidas por el cliente en un documento: etiquetas inteligentes, XML personalizado y etiquetas estructuradas de documento (controles de contenido).

## Clases

| Clase | Descripción |
| --- | --- |
| [CustomPart](./custompart/) | Representa una parte personalizada (contenido arbitrario) que no está definida por la norma ISO/IEC 29500. Para obtener más información, visite el artículo de documentación [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/). |
| [CustomPartCollection](./custompartcollection/) | Representa una colección de objetos [CustomPart](./custompart/). Para obtener más información, visite el artículo de documentación [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/). |
| [CustomXmlPart](./customxmlpart/) | Representa una parte de almacenamiento de datos XML personalizados (datos XML personalizados dentro de un paquete). Para obtener más información, visite el artículo de documentación [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/). |
| [CustomXmlPartCollection](./customxmlpartcollection/) | Representa una colección de partes XML personalizadas. Los elementos son objetos [CustomXmlPart](./customxmlpart/). Para obtener más información, visite el artículo de documentación [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/). |
| [CustomXmlProperty](./customxmlproperty/) | Representa un único atributo XML personalizado o una propiedad de etiqueta inteligente. Para obtener más información, visite el artículo de documentación [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/). |
| [CustomXmlPropertyCollection](./customxmlpropertycollection/) | Representa una colección de atributos XML personalizados o propiedades de etiqueta inteligente. Para obtener más información, visite el artículo de documentación [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/). |
| [CustomXmlSchemaCollection](./customxmlschemacollection/) | Una colección de cadenas que representan esquemas XML asociados a una parte XML personalizada. Para obtener más información, visite el artículo de documentación [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/). |
| [SdtListItem](./sdtlistitem/) | Este elemento especifica un único elemento de lista dentro de una etiqueta de documento estructurado padre [ComboBox](./sdttype/) o [DropDownList](./sdttype/). Para obtener más información, visite el artículo de documentación [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/). |
| [SdtListItemCollection](./sdtlistitemcollection/) | Proporciona acceso a los elementos [SdtListItem](./sdtlistitem/) de una etiqueta de documento estructurado. Para obtener más información, visite el artículo de documentación [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/). |
| [SmartTag](./smarttag/) | Este elemento especifica la presencia de una etiqueta inteligente alrededor de una o más estructuras en línea (runs, images, fields, etc.) dentro de un párrafo. Para obtener más información, visite el artículo de documentación [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/). |
| [StructuredDocumentTag](./structureddocumenttag/) | Representa una etiqueta de documento estructurado (SDT o control de contenido) en un documento. Para obtener más información, visite el artículo de documentación [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/). |
| [StructuredDocumentTagCollection](./structureddocumenttagcollection/) | Una colección de instancias [IStructuredDocumentTag](./istructureddocumenttag/) que representan las etiquetas de documento estructurado en el rango especificado. Para obtener más información, visite el artículo de documentación [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/). |
| [StructuredDocumentTagRangeEnd](./structureddocumenttagrangeend/) | Representa el final de una etiqueta de documento estructurado **ranged** que acepta contenido de múltiples secciones. Vea también el nodo [StructuredDocumentTagRangeStart](./structureddocumenttagrangestart/). Para obtener más información, visite el artículo de documentación [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/). |
| [StructuredDocumentTagRangeStart](./structureddocumenttagrangestart/) | Representa el inicio de una etiqueta de documento estructurado **ranged** que acepta contenido de múltiples secciones. Vea también [StructuredDocumentTagRangeEnd](./structureddocumenttagrangeend/). Para obtener más información, visite el artículo de documentación [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/). |
| [XmlMapping](./xmlmapping/) | Especifica la información que se utiliza para establecer un mapeo entre la etiqueta de documento estructurado padre y un elemento XML almacenado dentro de una parte de datos XML personalizada en el documento. Para obtener más información, visite el artículo de documentación [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/). |
## Interfaces

| Interfaz | Descripción |
| --- | --- |
| [IStructuredDocumentTag](./istructureddocumenttag/) | Interfaz para definir datos comunes para [StructuredDocumentTag](./structureddocumenttag/) y [StructuredDocumentTagRangeStart](./structureddocumenttagrangestart/). |
## Enums

| Enumeración | Descripción |
| --- | --- |
| [MarkupLevel](./markuplevel/) | Especifica el nivel en el árbol del documento donde puede aparecer un [StructuredDocumentTag](./structureddocumenttag/) particular. |
| [SdtAppearance](./sdtappearance/) | Especifica la apariencia de una etiqueta de documento estructurado. |
| [SdtCalendarType](./sdtcalendartype/) | Especifica los tipos posibles de calendarios que pueden usarse para especificar [CalendarType](./structureddocumenttag/get_calendartype/) en un documento Office Open XML. |
| [SdtDateStorageFormat](./sdtdatestorageformat/) | Especifica cómo se almacena/recupera la fecha de un SDT de fecha cuando el SDT está vinculado a un nodo XML en el almacén de datos del documento. |
| [SdtType](./sdttype/) | Especifica el tipo de un nodo de etiqueta de documento estructurado (SDT). |
