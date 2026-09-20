---
title: "Espacio de nombres Aspose::Words::Layout"
linktitle: "Aspose::Words::Layout"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Espacio de nombres Aspose::Words::Layout. El espacio de nombres Aspose.Words.Layout proporciona clases que permiten acceder a información como en qué página y dónde en una página se encuentran posicionados elementos particulares del documento, cuando el documento se formatea en páginas en C++."
type: docs
weight: 10000
url: /es/cpp/aspose.words.layout/
---

El espacio de nombres **Aspose.Words.Layout** proporciona clases que permiten acceder a información como en qué página y dónde en una página se encuentran posicionados ciertos elementos del documento, cuando el documento se formatea en páginas.

## Clases

| Clase | Descripción |
| --- | --- |
| [LayoutCollector](./layoutcollector/) | Esta clase permite calcular los números de página de los nodos del documento. Para obtener más información, visite el artículo de documentación [Converting to Fixed-page Format](https://docs.aspose.com/words/cpp/converting-to-fixed-page-format/). |
| [LayoutEnumerator](./layoutenumerator/) | Enumera las entidades de diseño de página de un documento. Puede usar esta clase para recorrer el modelo de diseño de página. Las propiedades disponibles son tipo, geometría, texto e índice de página donde se renderiza la entidad, así como la estructura general y las relaciones. Use la combinación de [GetEntity()](../) y [Current](./layoutenumerator/get_current/) para moverse a la entidad que corresponde a un nodo del documento. Para obtener más información, visite el artículo de documentación [Converting to Fixed-page Format](https://docs.aspose.com/words/cpp/converting-to-fixed-page-format/). |
| [LayoutOptions](./layoutoptions/) | Contiene las opciones que permiten controlar el proceso de diseño del documento. Para obtener más información, visite el artículo de documentación [Converting to Fixed-page Format](https://docs.aspose.com/words/cpp/converting-to-fixed-page-format/). |
| [PageLayoutCallbackArgs](./pagelayoutcallbackargs/) | Un argumento pasado a [Notify()](./ipagelayoutcallback/notify/). Para obtener más información, visite el artículo de documentación [Converting to Fixed-page Format](https://docs.aspose.com/words/cpp/converting-to-fixed-page-format/). |
| [RevisionOptions](./revisionoptions/) | Permite controlar cómo se manejan las revisiones del documento durante el proceso de diseño. Para obtener más información, visite el artículo de documentación [Converting to Fixed-page Format](https://docs.aspose.com/words/cpp/converting-to-fixed-page-format/). |
## Interfaces

| Interfaz | Descripción |
| --- | --- |
| [IPageLayoutCallback](./ipagelayoutcallback/) | Implemente esta interfaz si desea tener su propio método personalizado llamado durante la construcción y renderizado del modelo de diseño de página. |
## Enums

| Enumeración | Descripción |
| --- | --- |
| [CommentDisplayMode](./commentdisplaymode/) | Especifica el modo de renderizado para los comentarios del documento. |
| [ContinuousSectionRestart](./continuoussectionrestart/) | Representa diferentes comportamientos al calcular los números de página en una sección continua que reinicia la numeración de páginas. |
| [LayoutEntityType](./layoutentitytype/) | Tipos de las entidades de diseño. |
| [PageLayoutEvent](./pagelayoutevent/) | Código del evento generado durante la construcción y renderizado del modelo de diseño de página. El modelo de diseño de página se construye en dos pasos. Primero, "paso de conversión", que es cuando el diseño de página extrae el contenido del documento y crea el grafo de objetos. Segundo, "paso de reflujo", que es cuando las estructuras se dividen, fusionan y organizan en páginas. Dependiendo de la operación que desencadenó la construcción, el modelo de diseño de página puede o no renderizarse posteriormente en formato de página fija. Por ejemplo, calcular el número de páginas del documento o actualizar campos no requiere renderizado, mientras que la exportación a PDF sí lo requiere. |
| [RevisionColor](./revisioncolor/) | Permite especificar el color de las revisiones del documento. |
| [RevisionTextEffect](./revisiontexteffect/) | Permite especificar el efecto de decoración para las revisiones del texto del documento. |
| [ShowInBalloons](./showinballoons/) | Especifica qué revisiones se renderizan en globos. |
