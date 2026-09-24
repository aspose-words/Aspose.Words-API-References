---
title: "CssStyleSheetType"
linktitle: "CssStyleSheetType"
second_title: "Aspose.Words para Java"
description: "Especifica cómo se exportan los estilos CSS Cascading Style Sheet a HTML en Java."
type: docs
weight: 136
url: /es/java/com.aspose.words/cssstylesheettype/
---

**Inheritance:**
java.lang.Object
```
public class CssStyleSheetType
```

Especifica cómo se exportan los estilos CSS (Cascading Style Sheet) a HTML.

 **Examples:** 

Muestra cómo trabajar con las hojas de estilo CSS que crea una conversión a HTML.

```

 public void externalCssFilenames() throws Exception {
     Document doc = new Document(getMyDir() + "Rendering.docx");

     // Create an "HtmlFixedSaveOptions" object, which we can pass to the document's "Save" method
     // to modify how we convert the document to HTML.
     HtmlSaveOptions options = new HtmlSaveOptions();

     // Set the "CssStylesheetType" property to "CssStyleSheetType.External" to
     // accompany a saved HTML document with an external CSS stylesheet file.
     options.setCssStyleSheetType(CssStyleSheetType.EXTERNAL);

     // Below are two ways of specifying directories and filenames for output CSS stylesheets.
     // 1 -  Use the "CssStyleSheetFileName" property to assign a filename to our stylesheet:
     options.setCssStyleSheetFileName(getArtifactsDir() + "SavingCallback.ExternalCssFilenames.css");

     // 2 -  Use a custom callback to name our stylesheet:
     options.setCssSavingCallback(new CustomCssSavingCallback(getArtifactsDir() + "SavingCallback.ExternalCssFilenames.css", true, false));

     doc.save(getArtifactsDir() + "SavingCallback.ExternalCssFilenames.html", options);
 }

 /// 
 /// Sets a custom filename, along with other parameters for an external CSS stylesheet.
 /// 
 private static class CustomCssSavingCallback implements ICssSavingCallback {
     public CustomCssSavingCallback(String cssDocFilename, boolean isExportNeeded, boolean keepCssStreamOpen) {
         mCssTextFileName = cssDocFilename;
         mIsExportNeeded = isExportNeeded;
         mKeepCssStreamOpen = keepCssStreamOpen;
     }

     public void cssSaving(CssSavingArgs args) throws Exception {
         // We can access the entire source document via the "Document" property.
         Assert.assertTrue(args.getDocument().getOriginalFileName().endsWith("Rendering.docx"));

         args.setCssStream(new FileOutputStream(mCssTextFileName));
         args.isExportNeeded(mIsExportNeeded);
         args.setKeepCssStreamOpen(mKeepCssStreamOpen);
     }

     private final String mCssTextFileName;
     private final boolean mIsExportNeeded;
     private final boolean mKeepCssStreamOpen;
 }
 
```
## Campos

| Campo | Descripción |
| --- | --- |
| [EMBEDDED](#EMBEDDED) | Los estilos CSS se escriben por separado del contenido en una hoja de estilo incrustada en el archivo HTML. |
| [EXTERNAL](#EXTERNAL) | Los estilos CSS se escriben por separado del contenido en una hoja de estilo en un archivo externo. |
| [INLINE](#INLINE) | Los estilos CSS se escriben en línea (como valor del atributo **style** en cada elemento). |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String cssStyleSheetTypeName)](#fromName-java.lang.String) |  |
| [getName(int cssStyleSheetType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int cssStyleSheetType)](#toString-int) |  |
### EMBEDDED {#EMBEDDED}
```
public static int EMBEDDED
```


Los estilos CSS se escriben por separado del contenido en una hoja de estilo incrustada en el archivo HTML.

### EXTERNAL {#EXTERNAL}
```
public static int EXTERNAL
```


Los estilos CSS se escriben por separado del contenido en una hoja de estilo en un archivo externo. El archivo HTML enlaza la hoja de estilo.

### INLINE {#INLINE}
```
public static int INLINE
```


Los estilos CSS se escriben en línea (como valor del atributo **style** en cada elemento).

### length {#length}
```
public static int length
```


### fromName(String cssStyleSheetTypeName) {#fromName-java.lang.String}
```
public static int fromName(String cssStyleSheetTypeName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| cssStyleSheetTypeName | java.lang.String |  |

**Returns:**
int
### getName(int cssStyleSheetType) {#getName-int}
```
public static String getName(int cssStyleSheetType)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| cssStyleSheetType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int cssStyleSheetType) {#toString-int}
```
public static String toString(int cssStyleSheetType)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| cssStyleSheetType | int |  |

**Returns:**
java.lang.String
