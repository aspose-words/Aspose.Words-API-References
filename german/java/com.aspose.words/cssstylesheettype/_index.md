---
title: "CssStyleSheetType"
linktitle: "CssStyleSheetType"
second_title: "Aspose.Words für Java"
description: "Gibt an, wie CSS Cascading Style Sheet‑Stile in Java nach HTML exportiert werden."
type: docs
weight: 136
url: /de/java/com.aspose.words/cssstylesheettype/
---

**Inheritance:**
java.lang.Object
```
public class CssStyleSheetType
```

Gibt an, wie CSS‑ (Cascading Style Sheet)‑Stile nach HTML exportiert werden.

 **Examples:** 

Zeigt, wie man mit CSS‑Stylesheets arbeitet, die eine HTML‑Konvertierung erstellt.

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
## Felder

| Feld | Beschreibung |
| --- | --- |
| [EMBEDDED](#EMBEDDED) | CSS‑Stile werden getrennt vom Inhalt in einem im HTML‑Datei eingebetteten Stylesheet geschrieben. |
| [EXTERNAL](#EXTERNAL) | CSS‑Stile werden getrennt vom Inhalt in einem Stylesheet in einer externen Datei geschrieben. |
| [INLINE](#INLINE) | CSS‑Stile werden inline geschrieben (als Wert des **style**‑Attributs jedes Elements). |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String cssStyleSheetTypeName)](#fromName-java.lang.String) |  |
| [getName(int cssStyleSheetType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int cssStyleSheetType)](#toString-int) |  |
### EMBEDDED {#EMBEDDED}
```
public static int EMBEDDED
```


CSS‑Stile werden getrennt vom Inhalt in einem im HTML‑Datei eingebetteten Stylesheet geschrieben.

### EXTERNAL {#EXTERNAL}
```
public static int EXTERNAL
```


CSS‑Stile werden getrennt vom Inhalt in einem Stylesheet in einer externen Datei geschrieben. Die HTML‑Datei verlinkt das Stylesheet.

### INLINE {#INLINE}
```
public static int INLINE
```


CSS‑Stile werden inline geschrieben (als Wert des **style**‑Attributs jedes Elements).

### length {#length}
```
public static int length
```


### fromName(String cssStyleSheetTypeName) {#fromName-java.lang.String}
```
public static int fromName(String cssStyleSheetTypeName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| cssStyleSheetTypeName | java.lang.String |  |

**Returns:**
int
### getName(int cssStyleSheetType) {#getName-int}
```
public static String getName(int cssStyleSheetType)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| cssStyleSheetType | int |  |

**Returns:**
java.lang.String
