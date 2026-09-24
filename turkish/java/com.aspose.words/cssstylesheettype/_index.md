---
title: "CssStyleSheetType"
linktitle: "CssStyleSheetType"
second_title: "Aspose.Words Java için"
description: "Java'da CSS Cascading Style Sheet stillerinin HTML'ye nasıl dışa aktarıldığını belirtir."
type: docs
weight: 136
url: /tr/java/com.aspose.words/cssstylesheettype/
---

**Inheritance:**
java.lang.Object
```
public class CssStyleSheetType
```

CSS (Cascading Style Sheet) stillerinin HTML'ye nasıl dışa aktarıldığını belirtir.

 **Examples:** 

HTML dönüşümünün oluşturduğu CSS stil sayfalarıyla nasıl çalışılacağını gösterir.

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
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [EMBEDDED](#EMBEDDED) | CSS stilleri, HTML dosyasına gömülü bir stil sayfasında içerikten ayrı olarak yazılır. |
| [EXTERNAL](#EXTERNAL) | CSS stilleri, harici bir dosyadaki stil sayfasında içerikten ayrı olarak yazılır. |
| [INLINE](#INLINE) | CSS stilleri satır içi olarak (her öğenin **style** özniteliğinin bir değeri olarak) yazılır. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String cssStyleSheetTypeName)](#fromName-java.lang.String) |  |
| [getName(int cssStyleSheetType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int cssStyleSheetType)](#toString-int) |  |
### EMBEDDED {#EMBEDDED}
```
public static int EMBEDDED
```


CSS stilleri, HTML dosyasına gömülü bir stil sayfasında içerikten ayrı olarak yazılır.

### EXTERNAL {#EXTERNAL}
```
public static int EXTERNAL
```


CSS stilleri, harici bir dosyadaki stil sayfasında içerikten ayrı olarak yazılır. HTML dosyası stil sayfasına bağlanır.

### INLINE {#INLINE}
```
public static int INLINE
```


CSS stilleri satır içi olarak (her öğenin **style** özniteliğinin bir değeri olarak) yazılır.

### length {#length}
```
public static int length
```


### fromName(String cssStyleSheetTypeName) {#fromName-java.lang.String}
```
public static int fromName(String cssStyleSheetTypeName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| cssStyleSheetTypeName | java.lang.String |  |

**Returns:**
int
### getName(int cssStyleSheetType) {#getName-int}
```
public static String getName(int cssStyleSheetType)
```




**Parameters:**
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| cssStyleSheetType | int |  |

**Returns:**
java.lang.String
