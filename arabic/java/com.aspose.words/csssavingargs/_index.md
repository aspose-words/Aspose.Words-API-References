---
title: "CssSavingArgs"
linktitle: "CssSavingArgs"
second_title: "Aspose.Words لـ Java"
description: "يوفر البيانات لحدث ICssSavingCallback.cssSavingcom.aspose.words.CssSavingArgs في Java."
type: docs
weight: 135
url: /ar/java/com.aspose.words/csssavingargs/
---

**Inheritance:**
java.lang.Object
```
public class CssSavingArgs
```

يوفر بيانات لحدث [ICssSavingCallback.cssSaving(com.aspose.words.CssSavingArgs)](../../com.aspose.words/icsssavingcallback/\#cssSaving-com.aspose.words.CssSavingArgs).

للتعرف على المزيد، زر [ Save a Document ][Save a Document] مقالة الوثائق.

 **Remarks:** 

افتراضيًا، عندما تقوم Aspose.Words بحفظ مستند إلى HTML، فإنها تحفظ معلومات CSS مضمَّنة (كقيمة لخاصية **style** على كل عنصر).

[CssSavingArgs](../../com.aspose.words/csssavingargs/) allows to save CSS information into file by providing your own stream object.

لحفظ CSS في تدفق، استخدم الخاصية **P:Aspose.Words.Saving.CssSavingArgs.CssStream**.

لقمع حفظ CSS في ملف وتضمينه في مستند HTML استخدم الخاصية [isExportNeeded()](../../com.aspose.words/csssavingargs/\#isExportNeeded) / [isExportNeeded(boolean)](../../com.aspose.words/csssavingargs/\#isExportNeeded-boolean).

 **Examples:** 

يظهر كيفية العمل مع أوراق أنماط CSS التي ينشئها تحويل HTML.

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


[Save a Document]: https://docs.aspose.com/words/java/save-a-document/
## الطرق

| طريقة | الوصف |
| --- | --- |
| [getCssStream()](#getCssStream) |  |
| [getDocument()](#getDocument) | يحصل على كائن المستند الذي يتم حفظه حالياً. |
| [getKeepCssStreamOpen()](#getKeepCssStreamOpen) | يحدد ما إذا كان يجب على Aspose.Words إبقاء التدفق مفتوحًا أو إغلاقه بعد حفظ معلومات CSS. |
| [isExportNeeded()](#isExportNeeded) | يسمح بتحديد ما إذا كان سيتم تصدير CSS إلى ملف وتضمينه في مستند HTML. |
| [isExportNeeded(boolean value)](#isExportNeeded-boolean) | يسمح بتحديد ما إذا كان سيتم تصدير CSS إلى ملف وتضمينه في مستند HTML. |
| [setCssStream(OutputStream value)](#setCssStream-java.io.OutputStream) |  |
| [setKeepCssStreamOpen(boolean value)](#setKeepCssStreamOpen-boolean) | يحدد ما إذا كان يجب على Aspose.Words إبقاء التدفق مفتوحًا أو إغلاقه بعد حفظ معلومات CSS. |
### getCssStream() {#getCssStream}
```
public OutputStream getCssStream()
```




**Returns:**
java.io.OutputStream
### getDocument() {#getDocument}
```
public Document getDocument()
```


يحصل على كائن المستند الذي يتم حفظه حالياً.

 **Examples:** 

يظهر كيفية العمل مع أوراق أنماط CSS التي ينشئها تحويل HTML.

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

**Returns:**
[Document](../../com.aspose.words/document/) - The document object that is currently being saved.
### getKeepCssStreamOpen() {#getKeepCssStreamOpen}
```
public boolean getKeepCssStreamOpen()
```


يحدد ما إذا كان يجب على Aspose.Words إبقاء التدفق مفتوحًا أو إغلاقه بعد حفظ معلومات CSS.

 **Remarks:** 

القيمة الافتراضية هي  false  وستقوم Aspose.Words بإغلاق التدفق الذي قدمته في الخاصية **P:Aspose.Words.Saving.CssSavingArgs.CssStream** بعد كتابة معلومات CSS فيه. حدد  true  لإبقاء التدفق مفتوحًا.

 **Examples:** 

يظهر كيفية العمل مع أوراق أنماط CSS التي ينشئها تحويل HTML.

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

**P:Aspose.Words.Saving.CssSavingArgs.CssStream**

**Returns:**
boolean - القيمة المنطقية المقابلة.
### isExportNeeded() {#isExportNeeded}
```
public boolean isExportNeeded()
```


يسمح بتحديد ما إذا كان سيتم تصدير CSS إلى ملف وتضمينه في مستند HTML. القيمة الافتراضية هي  true . عندما تكون هذه الخاصية  false ، لن يتم حفظ معلومات CSS في ملف CSS ولن يتم تضمينه في مستند HTML.

 **Examples:** 

يظهر كيفية العمل مع أوراق أنماط CSS التي ينشئها تحويل HTML.

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

**Returns:**
boolean - القيمة المنطقية المقابلة.
### isExportNeeded(boolean value) {#isExportNeeded-boolean}
```
public void isExportNeeded(boolean value)
```


يسمح بتحديد ما إذا كان سيتم تصدير CSS إلى ملف وتضمينه في مستند HTML. القيمة الافتراضية هي  true . عندما تكون هذه الخاصية  false ، لن يتم حفظ معلومات CSS في ملف CSS ولن يتم تضمينه في مستند HTML.

 **Examples:** 

يظهر كيفية العمل مع أوراق أنماط CSS التي ينشئها تحويل HTML.

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

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

### setCssStream(OutputStream value) {#setCssStream-java.io.OutputStream}
```
public void setCssStream(OutputStream value)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.io.OutputStream |  |

### setKeepCssStreamOpen(boolean value) {#setKeepCssStreamOpen-boolean}
```
public void setKeepCssStreamOpen(boolean value)
```


يحدد ما إذا كان يجب على Aspose.Words إبقاء التدفق مفتوحًا أو إغلاقه بعد حفظ معلومات CSS.

 **Remarks:** 

القيمة الافتراضية هي  false  وستقوم Aspose.Words بإغلاق التدفق الذي قدمته في الخاصية **P:Aspose.Words.Saving.CssSavingArgs.CssStream** بعد كتابة معلومات CSS فيه. حدد  true  لإبقاء التدفق مفتوحًا.

 **Examples:** 

يظهر كيفية العمل مع أوراق أنماط CSS التي ينشئها تحويل HTML.

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

**P:Aspose.Words.Saving.CssSavingArgs.CssStream**

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

