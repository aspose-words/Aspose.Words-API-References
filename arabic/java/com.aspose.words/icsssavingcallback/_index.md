---
title: "ICssSavingCallback"
linktitle: "ICssSavingCallback"
second_title: "Aspose.Words لـ Java"
description: "نفّذ هذه الواجهة إذا كنت تريد التحكم في طريقة حفظ Aspose.Words لملف CSS Cascading Style Sheet عند حفظ مستند إلى HTML في Java."
type: docs
weight: 756
url: /ar/java/com.aspose.words/icsssavingcallback/
---
```
public interface ICssSavingCallback
```

نفّذ هذه الواجهة إذا كنت تريد التحكم في كيفية حفظ Aspose.Words لملف CSS (Cascading Style Sheet) عند حفظ مستند إلى HTML.

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
## الطرق

| طريقة | الوصف |
| --- | --- |
| [cssSaving(CssSavingArgs args)](#cssSaving-com.aspose.words.CssSavingArgs) | يتم استدعاؤه عندما يقوم Aspose.Words بحفظ ملف CSS (ورقة الأنماط المتتالية). |
### cssSaving(CssSavingArgs args) {#cssSaving-com.aspose.words.CssSavingArgs}
```
public abstract void cssSaving(CssSavingArgs args)
```


يتم استدعاؤه عندما يقوم Aspose.Words بحفظ ملف CSS (ورقة الأنماط المتتالية).

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
| args | [CssSavingArgs](../../com.aspose.words/csssavingargs/) |  |

