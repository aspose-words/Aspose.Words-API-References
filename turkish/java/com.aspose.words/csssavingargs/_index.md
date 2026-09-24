---
title: "CssSavingArgs"
linktitle: "CssSavingArgs"
second_title: "Aspose.Words Java için"
description: "Java'da ICssSavingCallback.cssSavingcom.aspose.words.CssSavingArgs olayı için veri sağlar."
type: docs
weight: 135
url: /tr/java/com.aspose.words/csssavingargs/
---

**Inheritance:**
java.lang.Object
```
public class CssSavingArgs
```

Belirtilen [ICssSavingCallback.cssSaving(com.aspose.words.CssSavingArgs)](../../com.aspose.words/icsssavingcallback/\#cssSaving-com.aspose.words.CssSavingArgs) olayı için veri sağlar.

Daha fazla bilgi edinmek için [ Save a Document ][Save a Document] dokümantasyon makalesini ziyaret edin.

 **Remarks:** 

Varsayılan olarak, Aspose.Words bir belgeyi HTML'ye kaydettiğinde, CSS bilgilerini satır içi olarak (her öğenin **style** özniteliğinin değeri olarak) kaydeder.

[CssSavingArgs](../../com.aspose.words/csssavingargs/) allows to save CSS information into file by providing your own stream object.

CSS'i akışa kaydetmek için **P:Aspose.Words.Saving.CssSavingArgs.CssStream** özelliğini kullanın.

CSS'in bir dosyaya kaydedilmesini ve HTML belgesine gömülmesini engellemek için [isExportNeeded()](../../com.aspose.words/csssavingargs/\#isExportNeeded) / [isExportNeeded(boolean)](../../com.aspose.words/csssavingargs/\#isExportNeeded-boolean) özelliğini kullanın.

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


[Save a Document]: https://docs.aspose.com/words/java/save-a-document/
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [getCssStream()](#getCssStream) |  |
| [getDocument()](#getDocument) | Şu anda kaydedilen belge nesnesini alır. |
| [getKeepCssStreamOpen()](#getKeepCssStreamOpen) | Aspose.Words'in akışı açık tutup tutmayacağını veya CSS bilgisi kaydedildikten sonra kapatıp kapatmayacağını belirtir. |
| [isExportNeeded()](#isExportNeeded) | CSS'in dosyaya dışa aktarılıp HTML belgesine gömülüp gömülmeyeceğini belirtmeye izin verir. |
| [isExportNeeded(boolean value)](#isExportNeeded-boolean) | CSS'in dosyaya dışa aktarılıp HTML belgesine gömülüp gömülmeyeceğini belirtmeye izin verir. |
| [setCssStream(OutputStream value)](#setCssStream-java.io.OutputStream) |  |
| [setKeepCssStreamOpen(boolean value)](#setKeepCssStreamOpen-boolean) | Aspose.Words'in akışı açık tutup tutmayacağını veya CSS bilgisi kaydedildikten sonra kapatıp kapatmayacağını belirtir. |
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


Şu anda kaydedilen belge nesnesini alır.

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

**Returns:**
[Document](../../com.aspose.words/document/) - The document object that is currently being saved.
### getKeepCssStreamOpen() {#getKeepCssStreamOpen}
```
public boolean getKeepCssStreamOpen()
```


Aspose.Words'in akışı açık tutup tutmayacağını veya CSS bilgisi kaydedildikten sonra kapatıp kapatmayacağını belirtir.

 **Remarks:** 

Varsayılan değer false'tur ve Aspose.Words, **P:Aspose.Words.Saving.CssSavingArgs.CssStream** özelliğinde sağladığınız akışı, içine bir CSS bilgisi yazıldıktan sonra kapatır. Akışı açık tutmak için true belirtin.

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

**P:Aspose.Words.Saving.CssSavingArgs.CssStream**

**Returns:**
boolean - İlgili  boolean  değeri.
### isExportNeeded() {#isExportNeeded}
```
public boolean isExportNeeded()
```


CSS'in dosyaya dışa aktarılıp HTML belgesine gömülüp gömülmeyeceğini belirtmeye izin verir. Varsayılan değer true'dur. Bu özellik false olduğunda, CSS bilgisi bir CSS dosyasına kaydedilmez ve HTML belgesine gömülmez.

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

**Returns:**
boolean - İlgili  boolean  değeri.
### isExportNeeded(boolean value) {#isExportNeeded-boolean}
```
public void isExportNeeded(boolean value)
```


CSS'in dosyaya dışa aktarılıp HTML belgesine gömülüp gömülmeyeceğini belirtmeye izin verir. Varsayılan değer true'dur. Bu özellik false olduğunda, CSS bilgisi bir CSS dosyasına kaydedilmez ve HTML belgesine gömülmez.

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

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### setCssStream(OutputStream value) {#setCssStream-java.io.OutputStream}
```
public void setCssStream(OutputStream value)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.io.OutputStream |  |

### setKeepCssStreamOpen(boolean value) {#setKeepCssStreamOpen-boolean}
```
public void setKeepCssStreamOpen(boolean value)
```


Aspose.Words'in akışı açık tutup tutmayacağını veya CSS bilgisi kaydedildikten sonra kapatıp kapatmayacağını belirtir.

 **Remarks:** 

Varsayılan değer false'tur ve Aspose.Words, **P:Aspose.Words.Saving.CssSavingArgs.CssStream** özelliğinde sağladığınız akışı, içine bir CSS bilgisi yazıldıktan sonra kapatır. Akışı açık tutmak için true belirtin.

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

**P:Aspose.Words.Saving.CssSavingArgs.CssStream**

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

