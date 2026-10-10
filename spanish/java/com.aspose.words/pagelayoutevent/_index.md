---
title: "PageLayoutEvent"
linktitle: "PageLayoutEvent"
second_title: "Aspose.Words para Java"
description: "Un código de evento generado durante la construcción y renderizado del modelo de diseño de página en Java."
type: docs
weight: 515
url: /es/java/com.aspose.words/pagelayoutevent/
---

**Inheritance:**
java.lang.Object
```
public class PageLayoutEvent
```

Un código de evento generado durante la construcción y renderizado del modelo de diseño de página.

El modelo de diseño de página se construye en dos pasos. Primero, "paso de conversión", que es cuando el diseño de página extrae el contenido del documento y crea el grafo de objetos. Segundo, "paso de reflujo", que es cuando las estructuras se dividen, se combinan y se organizan en páginas.

Dependiendo de la operación que desencadenó la construcción, el modelo de diseño de página puede o no ser renderizado posteriormente en un formato de página fija. Por ejemplo, calcular el número de páginas del documento o actualizar campos no requiere renderizado, mientras que la exportación a PDF sí lo requiere.

 **Examples:** 

Muestra cómo rastrear cambios de diseño con una callback de diseño.

```

 public void pageLayoutCallback() throws Exception {
     Document doc = new Document();
     doc.getBuiltInDocumentProperties().setTitle("My Document");

     DocumentBuilder builder = new DocumentBuilder(doc);
     builder.writeln("Hello world!");

     doc.getLayoutOptions().setCallback(new RenderPageLayoutCallback());
     doc.updatePageLayout();

     doc.save(getArtifactsDir() + "Layout.PageLayoutCallback.pdf");
 }

 /// 
 /// Notifies us when we save the document to a fixed page format
 /// and renders a page that we perform a page reflow on to an image in the local file system.
 /// 
 private static class RenderPageLayoutCallback implements IPageLayoutCallback {
     public void notify(PageLayoutCallbackArgs a) throws Exception {
         switch (a.getEvent()) {
             case PageLayoutEvent.PART_REFLOW_FINISHED:
                 notifyPartFinished(a);
                 break;
             case PageLayoutEvent.CONVERSION_FINISHED:
                 notifyConversionFinished(a);
                 break;
         }
     }

     private void notifyPartFinished(PageLayoutCallbackArgs a) throws Exception {
         System.out.println(MessageFormat.format("Part at page {0} reflow.", a.getPageIndex() + 1));
         renderPage(a, a.getPageIndex());
     }

     private void notifyConversionFinished(PageLayoutCallbackArgs a) {
         System.out.println(MessageFormat.format("Document \"{0}\" converted to page format.", a.getDocument().getBuiltInDocumentProperties().getTitle()));
     }

     private void renderPage(PageLayoutCallbackArgs a, int pageIndex) throws Exception {
         ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.PNG);
         {
             saveOptions.setPageSet(new PageSet(pageIndex));
         }

         try (FileOutputStream stream = new FileOutputStream(getArtifactsDir() + MessageFormat.format("PageLayoutCallback.page-{0} {1}.png", pageIndex + 1, ++mNum))) {
             a.getDocument().save(stream, saveOptions);
         }
     }

     private int mNum;
 }
 
```
## Campos

| Campo | Descripción |
| --- | --- |
| [BUILD_FINISHED](#BUILD-FINISHED) | La construcción del diseño de página ha finalizado. |
| [BUILD_STARTED](#BUILD-STARTED) | La construcción del diseño de página ha comenzado. |
| [CONVERSION_FINISHED](#CONVERSION-FINISHED) | La conversión del modelo de documento al diseño de página ha finalizado. |
| [CONVERSION_STARTED](#CONVERSION-STARTED) | La conversión del modelo de documento al diseño de página ha comenzado. |
| [NONE](#NONE) | Valor predeterminado |
| [PART_REFLOW_FINISHED](#PART-REFLOW-FINISHED) | El reflujo de la página ha finalizado. |
| [PART_REFLOW_STARTED](#PART-REFLOW-STARTED) | El reflujo de la página ha comenzado. |
| [PART_RENDERING_FINISHED](#PART-RENDERING-FINISHED) | El renderizado de la página ha finalizado. |
| [PART_RENDERING_STARTED](#PART-RENDERING-STARTED) | El renderizado de la página ha comenzado. |
| [REFLOW_FINISHED](#REFLOW-FINISHED) | El reflujo del diseño de la página ha finalizado. |
| [REFLOW_STARTED](#REFLOW-STARTED) | El reflujo del diseño de la página ha comenzado. |
| [WATCH_DOG](#WATCH-DOG) | Corresponde a un punto de control en el código que se visita con frecuencia y que es adecuado para abortar el proceso. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String pageLayoutEventName)](#fromName-java.lang.String) |  |
| [getName(int pageLayoutEvent)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int pageLayoutEvent)](#toString-int) |  |
### BUILD_FINISHED {#BUILD-FINISHED}
```
public static int BUILD_FINISHED
```


Construcción del diseño de la página ha finalizado. Disparado una vez. Este es el último evento que ocurre cuando se llama a [Document.updatePageLayout()](../../com.aspose.words/document/\#updatePageLayout).

### BUILD_STARTED {#BUILD-STARTED}
```
public static int BUILD_STARTED
```


Construcción del diseño de la página ha comenzado. Disparado una vez. Este es el primer evento que ocurre cuando se llama a [Document.updatePageLayout()](../../com.aspose.words/document/\#updatePageLayout).

### CONVERSION_FINISHED {#CONVERSION-FINISHED}
```
public static int CONVERSION_FINISHED
```


Conversión del modelo de documento al diseño de página ha finalizado. Disparado una vez. Esto ocurre cuando el modelo de diseño deja de extraer el contenido del documento.

### CONVERSION_STARTED {#CONVERSION-STARTED}
```
public static int CONVERSION_STARTED
```


Conversión del modelo de documento al diseño de página ha comenzado. Disparado una vez. Esto ocurre cuando el modelo de diseño comienza a extraer el contenido del documento.

### NONE {#NONE}
```
public static int NONE
```


Valor predeterminado

### PART_REFLOW_FINISHED {#PART-REFLOW-FINISHED}
```
public static int PART_REFLOW_FINISHED
```


El reflujo de la página ha finalizado. Observe que la página puede reflujo varias veces y que el reflujo puede reiniciarse antes de que termine.

### PART_REFLOW_STARTED {#PART-REFLOW-STARTED}
```
public static int PART_REFLOW_STARTED
```


El reflujo de la página ha comenzado. Observe que la página puede reflujo varias veces y que el reflujo puede reiniciarse antes de que termine.

### PART_RENDERING_FINISHED {#PART-RENDERING-FINISHED}
```
public static int PART_RENDERING_FINISHED
```


El renderizado de la página ha finalizado. Esto se dispara una vez por página.

### PART_RENDERING_STARTED {#PART-RENDERING-STARTED}
```
public static int PART_RENDERING_STARTED
```


El renderizado de la página ha comenzado. Esto se dispara una vez por página.

### REFLOW_FINISHED {#REFLOW-FINISHED}
```
public static int REFLOW_FINISHED
```


El reflujo del diseño de la página ha finalizado. Disparado una vez. Esto ocurre cuando el modelo de diseño deja de reflujo del contenido del documento.

### REFLOW_STARTED {#REFLOW-STARTED}
```
public static int REFLOW_STARTED
```


El reflujo del diseño de la página ha comenzado. Disparado una vez. Esto ocurre cuando el modelo de diseño comienza a reflujo del contenido del documento.

### WATCH_DOG {#WATCH-DOG}
```
public static int WATCH_DOG
```


Corresponde a un punto de control en el código que se visita con frecuencia y que es adecuado para abortar el proceso.

Mientras esté dentro de [IPageLayoutCallback.notify(com.aspose.words.PageLayoutCallbackArgs)](../../com.aspose.words/ipagelayoutcallback/\#notify-com.aspose.words.PageLayoutCallbackArgs) lance una excepción personalizada para abortar el proceso.

Puede lanzar una excepción al manejar cualquier evento de devolución de llamada para abortar el proceso.

Tenga en cuenta que si el proceso se aborta, el modelo de diseño de página permanece en un estado indefinido. Sin embargo, si el proceso se aborta durante el reflujo de una página completa, debería ser posible usar el modelo de diseño hasta el final de esa página.

### length {#length}
```
public static int length
```


### fromName(String pageLayoutEventName) {#fromName-java.lang.String}
```
public static int fromName(String pageLayoutEventName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| pageLayoutEventName | java.lang.String |  |

**Returns:**
int
### getName(int pageLayoutEvent) {#getName-int}
```
public static String getName(int pageLayoutEvent)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| pageLayoutEvent | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int pageLayoutEvent) {#toString-int}
```
public static String toString(int pageLayoutEvent)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| pageLayoutEvent | int |  |

**Returns:**
java.lang.String
