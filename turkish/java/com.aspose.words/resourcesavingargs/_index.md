---
title: "ResourceSavingArgs"
linktitle: "ResourceSavingArgs"
second_title: "Aspose.Words Java için"
description: "Java'da IResourceSavingCallback.resourceSavingcom.aspose.words.ResourceSavingArgs olayı için veri sağlar."
type: docs
weight: 577
url: /tr/java/com.aspose.words/resourcesavingargs/
---

**Inheritance:**
java.lang.Object
```
public class ResourceSavingArgs
```

Veri sağlar [IResourceSavingCallback.resourceSaving(com.aspose.words.ResourceSavingArgs)](../../com.aspose.words/iresourcesavingcallback/\#resourceSaving-com.aspose.words.ResourceSavingArgs) olayına.

Daha fazla bilgi edinmek için [ Save a Document ][Save a Document] dokümantasyon makalesini ziyaret edin.

 **Remarks:** 

Varsayılan olarak, Aspose.Words bir belgeyi sabit sayfa HTML, SVG veya Markdown olarak kaydettiğinde, her kaynağı ayrı bir dosyaya kaydeder. Aspose.Words belge dosya adını ve benzersiz bir numarayı kullanarak belgede bulunan her kaynak için benzersiz bir dosya adı oluşturur.

[ResourceSavingArgs](../../com.aspose.words/resourcesavingargs/) allows to redefine how resource file names are generated or to completely circumvent saving of resources into files by providing your own stream objects.

Kaynak dosya adlarını oluşturmak için kendi mantığınızı uygulamak istiyorsanız, [getResourceFileName()](../../com.aspose.words/resourcesavingargs/\#getResourceFileName) / [setResourceFileName(java.lang.String)](../../com.aspose.words/resourcesavingargs/\#setResourceFileName-java.lang.String) özelliğini kullanın.

Kaynakları dosyalar yerine akışlara kaydetmek için **P:Aspose.Words.Saving.ResourceSavingArgs.ResourceStream** özelliğini kullanın.

 **Examples:** 

Bir belgeyi HTML'ye dönüştürürken oluşturulan dış kaynakları izlemek için bir geri çağırma (callback) nasıl kullanılacağını gösterir.

```

 public void resourceSavingCallback() throws Exception {
     Document doc = new Document(getMyDir() + "Bullet points with alternative font.docx");

     FontSavingCallback callback = new FontSavingCallback();

     HtmlFixedSaveOptions saveOptions = new HtmlFixedSaveOptions();
     {
         saveOptions.setResourceSavingCallback(callback);
     }

     doc.save(getArtifactsDir() + "HtmlFixedSaveOptions.UsingMachineFonts.html", saveOptions);

     System.out.println(callback.getText());
 }

 private static class FontSavingCallback implements IResourceSavingCallback {
     /// 
     /// Called when Aspose.Words saves an external resource to fixed page HTML or SVG.
     /// 
     public void resourceSaving(ResourceSavingArgs args) {
         mText.append(MessageFormat.format("Original document URI:\t{0}", args.getDocument().getOriginalFileName()));
         mText.append(MessageFormat.format("Resource being saved:\t{0}", args.getResourceFileName()));
         mText.append(MessageFormat.format("Full uri after saving:\t{0}\n", args.getResourceFileUri()));
     }

     public String getText() {
         return mText.toString();
     }

     private final StringBuilder mText = new StringBuilder();
 }
 
```


[Save a Document]: https://docs.aspose.com/words/java/save-a-document/
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [getDocument()](#getDocument) | Şu anda kaydedilen belge nesnesini alır. |
| [getKeepResourceStreamOpen()](#getKeepResourceStreamOpen) | Aspose.Words'in akışı açık tutup tutmayacağını veya bir kaynağı kaydettikten sonra kapatıp kapatmayacağını belirtir. |
| [getResourceFileName()](#getResourceFileName) | Kaynağın kaydedileceği dosya adını (yol olmadan) alır. |
| [getResourceFileUri()](#getResourceFileUri) | Belgeden kaynak dosyasına referans vermek için kullanılan tekdüzen kaynak tanımlayıcısını (URI) alır. |
| [getResourceStream()](#getResourceStream) |  |
| [setKeepResourceStreamOpen(boolean value)](#setKeepResourceStreamOpen-boolean) | Aspose.Words'in akışı açık tutup tutmayacağını veya bir kaynağı kaydettikten sonra kapatıp kapatmayacağını belirtir. |
| [setResourceFileName(String value)](#setResourceFileName-java.lang.String) | Kaynağın kaydedileceği dosya adını (yol olmadan) ayarlar. |
| [setResourceFileUri(String value)](#setResourceFileUri-java.lang.String) | Belgeden kaynak dosyasına referans vermek için kullanılan tekdüzen kaynak tanımlayıcısını (URI) ayarlar. |
| [setResourceStream(OutputStream value)](#setResourceStream-java.io.OutputStream) |  |
### getDocument() {#getDocument}
```
public Document getDocument()
```


Şu anda kaydedilen belge nesnesini alır.

 **Examples:** 

Bir belgeyi HTML'ye dönüştürürken oluşturulan dış kaynakları izlemek için bir geri çağırma (callback) nasıl kullanılacağını gösterir.

```

 public void resourceSavingCallback() throws Exception {
     Document doc = new Document(getMyDir() + "Bullet points with alternative font.docx");

     FontSavingCallback callback = new FontSavingCallback();

     HtmlFixedSaveOptions saveOptions = new HtmlFixedSaveOptions();
     {
         saveOptions.setResourceSavingCallback(callback);
     }

     doc.save(getArtifactsDir() + "HtmlFixedSaveOptions.UsingMachineFonts.html", saveOptions);

     System.out.println(callback.getText());
 }

 private static class FontSavingCallback implements IResourceSavingCallback {
     /// 
     /// Called when Aspose.Words saves an external resource to fixed page HTML or SVG.
     /// 
     public void resourceSaving(ResourceSavingArgs args) {
         mText.append(MessageFormat.format("Original document URI:\t{0}", args.getDocument().getOriginalFileName()));
         mText.append(MessageFormat.format("Resource being saved:\t{0}", args.getResourceFileName()));
         mText.append(MessageFormat.format("Full uri after saving:\t{0}\n", args.getResourceFileUri()));
     }

     public String getText() {
         return mText.toString();
     }

     private final StringBuilder mText = new StringBuilder();
 }
 
```

**Returns:**
[Document](../../com.aspose.words/document/) - The document object that is currently being saved.
### getKeepResourceStreamOpen() {#getKeepResourceStreamOpen}
```
public boolean getKeepResourceStreamOpen()
```


Aspose.Words'in akışı açık tutup tutmayacağını veya bir kaynağı kaydettikten sonra kapatıp kapatmayacağını belirtir.

 **Remarks:** 

Varsayılan false ve Aspose.Words, **P:Aspose.Words.Saving.ResourceSavingArgs.ResourceStream** özelliğinde sağladığınız akışı, bir kaynağı içine yazdıktan sonra kapatır. Akışı açık tutmak için true belirtin.

 **Examples:** 

Bir belgeyi HTML'ye dönüştürürken oluşturulan dış kaynakların URI'lerini yazdırmak için bir geri çağırma (callback) nasıl kullanılacağını gösterir.

```

 public void htmlFixedResourceFolder() throws Exception {
     Document doc = new Document(getMyDir() + "Rendering.docx");

     ResourceUriPrinter callback = new ResourceUriPrinter();

     HtmlFixedSaveOptions options = new HtmlFixedSaveOptions();
     {
         options.setSaveFormat(SaveFormat.HTML_FIXED);
         options.setExportEmbeddedImages(false);
         options.setResourcesFolder(getArtifactsDir() + "HtmlFixedResourceFolder");
         options.setResourcesFolderAlias(getArtifactsDir() + "HtmlFixedResourceFolderAlias");
         options.setShowPageBorder(false);
         options.setResourceSavingCallback(callback);
     }

     // A folder specified by ResourcesFolderAlias will contain the resources instead of ResourcesFolder.
     // We must ensure the folder exists before the streams can put their resources into it.
     new File(options.getResourcesFolderAlias()).mkdir();

     doc.save(getArtifactsDir() + "HtmlFixedSaveOptions.HtmlFixedResourceFolder.html", options);

     System.out.println(callback.getText());

     String[] resourceFiles = new File(getArtifactsDir() + "HtmlFixedResourceFolderAlias").list();

     Assert.assertFalse(new File(getArtifactsDir() + "HtmlFixedResourceFolder").exists());
     Assert.assertEquals(6, IterableUtils.countMatches(Arrays.asList(resourceFiles),
             f -> f.endsWith(".jpeg") || f.endsWith(".png") || f.endsWith(".css")));
 }

 /// 
 /// Counts and prints URIs of resources contained by as they are converted to fixed HTML.
 /// 
 private static class ResourceUriPrinter implements IResourceSavingCallback {
     public void resourceSaving(ResourceSavingArgs args) throws Exception {
         // If we set a folder alias in the SaveOptions object, we will be able to print it from here.
         mText.append(MessageFormat.format("Resource #{0} \"{1}\"", ++mSavedResourceCount, args.getResourceFileName()));

         String extension = FilenameUtils.getExtension(args.getResourceFileName());
         switch (extension) {
             case "ttf":
             case "woff": {
                 // By default, 'ResourceFileUri' uses system folder for fonts.
                 // To avoid problems in other platforms you must explicitly specify the path for the fonts.
                 args.setResourceFileUri(getArtifactsDir() + File.separatorChar + args.getResourceFileName());
                 break;
             }
         }

         mText.append("\t" + args.getResourceFileUri());

         // If we have specified a folder in the "ResourcesFolderAlias" property,
         // we will also need to redirect each stream to put its resource in that folder.
         args.setResourceStream(new FileOutputStream(args.getResourceFileUri()));
         args.setKeepResourceStreamOpen(false);
     }

     public String getText() {
         return mText.toString();
     }

     private int mSavedResourceCount;
     private final  StringBuilder mText = new StringBuilder();
 }
 
```

**P:Aspose.Words.Saving.ResourceSavingArgs.ResourceStream**

**Returns:**
boolean - İlgili  boolean  değeri.
### getResourceFileName() {#getResourceFileName}
```
public String getResourceFileName()
```


Kaynağın kaydedileceği dosya adını (yol olmadan) alır.

 **Remarks:** 

Bu özellik, sabit sayfa HTML, SVG veya Markdown dışa aktarımı sırasında kaynak dosya adlarının nasıl oluşturulduğunu yeniden tanımlamanıza olanak tanır.

Olay tetiklendiğinde, bu özellik Aspose.Words tarafından oluşturulan dosya adını içerir. Kaynağı farklı bir dosyaya kaydetmek için bu özelliğin değerini değiştirebilirsiniz. Dosya adlarının benzersiz olması gerektiğini unutmayın.

Aspose.Words, sabit sayfa HTML, SVG veya Markdown formatına dışa aktarırken her kaynak için otomatik olarak benzersiz bir dosya adı oluşturur. Kaynak dosya adının nasıl oluşturulacağı, belgeyi bir dosyaya mı yoksa bir akışa mı kaydettiğinize bağlıdır.

Bir belgeyi dosyaya kaydederken, oluşturulan kaynak dosya adı *.![Image 1][].* şeklinde görünür.

Bir belgeyi akışa kaydederken, oluşturulan kaynak dosya adı *Aspose.Words..![Image 1][].* şeklinde görünür.

[getResourceFileName()](../../com.aspose.words/resourcesavingargs/\#getResourceFileName) / [setResourceFileName(java.lang.String)](../../com.aspose.words/resourcesavingargs/\#setResourceFileName-java.lang.String) must contain only the file name without the path. Aspose.Words determines the path for saving and the value of the  src  attribute for writing to fixed page HTML, SVG or Markdown using the document file name, the [HtmlFixedSaveOptions.getResourcesFolder()](../../com.aspose.words/htmlfixedsaveoptions/\#getResourcesFolder) / [HtmlFixedSaveOptions.setResourcesFolder(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions/\#setResourcesFolder-java.lang.String) or [SvgSaveOptions.getResourcesFolder()](../../com.aspose.words/svgsaveoptions/\#getResourcesFolder) / [SvgSaveOptions.setResourcesFolder(java.lang.String)](../../com.aspose.words/svgsaveoptions/\#setResourcesFolder-java.lang.String) and [HtmlFixedSaveOptions.getResourcesFolderAlias()](../../com.aspose.words/htmlfixedsaveoptions/\#getResourcesFolderAlias) / [HtmlFixedSaveOptions.setResourcesFolderAlias(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions/\#setResourcesFolderAlias-java.lang.String) or [SvgSaveOptions.getResourcesFolderAlias()](../../com.aspose.words/svgsaveoptions/\#getResourcesFolderAlias) / [SvgSaveOptions.setResourcesFolderAlias(java.lang.String)](../../com.aspose.words/svgsaveoptions/\#setResourcesFolderAlias-java.lang.String) or [MarkdownSaveOptions.getImagesFolder()](../../com.aspose.words/markdownsaveoptions/\#getImagesFolder) / [MarkdownSaveOptions.setImagesFolder(java.lang.String)](../../com.aspose.words/markdownsaveoptions/\#setImagesFolder-java.lang.String) or [MarkdownSaveOptions.getImagesFolderAlias()](../../com.aspose.words/markdownsaveoptions/\#getImagesFolderAlias) / [MarkdownSaveOptions.setImagesFolderAlias(java.lang.String)](../../com.aspose.words/markdownsaveoptions/\#setImagesFolderAlias-java.lang.String) properties.

[HtmlFixedSaveOptions.getResourcesFolder()](../../com.aspose.words/htmlfixedsaveoptions/\#getResourcesFolder) / [HtmlFixedSaveOptions.setResourcesFolder(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions/\#setResourcesFolder-java.lang.String) [SvgSaveOptions.getResourcesFolder()](../../com.aspose.words/svgsaveoptions/\#getResourcesFolder) / [SvgSaveOptions.setResourcesFolder(java.lang.String)](../../com.aspose.words/svgsaveoptions/\#setResourcesFolder-java.lang.String) [HtmlFixedSaveOptions.getResourcesFolderAlias()](../../com.aspose.words/htmlfixedsaveoptions/\#getResourcesFolderAlias) / [HtmlFixedSaveOptions.setResourcesFolderAlias(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions/\#setResourcesFolderAlias-java.lang.String) [SvgSaveOptions.getResourcesFolderAlias()](../../com.aspose.words/svgsaveoptions/\#getResourcesFolderAlias) / [SvgSaveOptions.setResourcesFolderAlias(java.lang.String)](../../com.aspose.words/svgsaveoptions/\#setResourcesFolderAlias-java.lang.String)

 **Examples:** 

Bir belgeyi HTML'ye dönüştürürken oluşturulan dış kaynakları izlemek için bir geri çağırma (callback) nasıl kullanılacağını gösterir.

```

 public void resourceSavingCallback() throws Exception {
     Document doc = new Document(getMyDir() + "Bullet points with alternative font.docx");

     FontSavingCallback callback = new FontSavingCallback();

     HtmlFixedSaveOptions saveOptions = new HtmlFixedSaveOptions();
     {
         saveOptions.setResourceSavingCallback(callback);
     }

     doc.save(getArtifactsDir() + "HtmlFixedSaveOptions.UsingMachineFonts.html", saveOptions);

     System.out.println(callback.getText());
 }

 private static class FontSavingCallback implements IResourceSavingCallback {
     /// 
     /// Called when Aspose.Words saves an external resource to fixed page HTML or SVG.
     /// 
     public void resourceSaving(ResourceSavingArgs args) {
         mText.append(MessageFormat.format("Original document URI:\t{0}", args.getDocument().getOriginalFileName()));
         mText.append(MessageFormat.format("Resource being saved:\t{0}", args.getResourceFileName()));
         mText.append(MessageFormat.format("Full uri after saving:\t{0}\n", args.getResourceFileUri()));
     }

     public String getText() {
         return mText.toString();
     }

     private final StringBuilder mText = new StringBuilder();
 }
 
```

**P:Aspose.Words.Saving.ResourceSavingArgs.ResourceStream**


[Image 1]: 

**Returns:**
java.lang.String - Kaynağın kaydedileceği dosya adı (yol olmadan).
### getResourceFileUri() {#getResourceFileUri}
```
public String getResourceFileUri()
```


Belgeden kaynak dosyasına referans vermek için kullanılan tekdüzen kaynak tanımlayıcısını (URI) alır.

 **Remarks:** 

Bu özellik, sabit sayfa HTML, SVG veya Markdown belgelerine dışa aktarılan kaynak dosyalarının URI'lerini değiştirmenize olanak tanır.

Aspose.Words, sabit sayfa HTML, SVG veya Markdown formatına dışa aktarırken her kaynak dosya için otomatik olarak bir URI oluşturur. Oluşturulan URI'ler, Aspose.Words tarafından kaydedilen kaynak dosyalara referans verir. Ancak, kaynak dosyalar başka bir konuma taşınacaksa veya akışlara kaydedilecekse URI'ler hatalı olabilir. Bu özellik, bu durumlarda URI'leri düzeltmenizi sağlar.

Olay tetiklendiğinde, bu özellik Aspose.Words tarafından oluşturulan URI'yi içerir. Kaynak dosya için özel bir URI sağlamak amacıyla bu özelliğin değerini değiştirebilirsiniz.

[HtmlFixedSaveOptions.getResourcesFolder()](../../com.aspose.words/htmlfixedsaveoptions/\#getResourcesFolder) / [HtmlFixedSaveOptions.setResourcesFolder(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions/\#setResourcesFolder-java.lang.String) [SvgSaveOptions.getResourcesFolder()](../../com.aspose.words/svgsaveoptions/\#getResourcesFolder) / [SvgSaveOptions.setResourcesFolder(java.lang.String)](../../com.aspose.words/svgsaveoptions/\#setResourcesFolder-java.lang.String) [MarkdownSaveOptions.getImagesFolder()](../../com.aspose.words/markdownsaveoptions/\#getImagesFolder) / [MarkdownSaveOptions.setImagesFolder(java.lang.String)](../../com.aspose.words/markdownsaveoptions/\#setImagesFolder-java.lang.String) [HtmlFixedSaveOptions.getResourcesFolderAlias()](../../com.aspose.words/htmlfixedsaveoptions/\#getResourcesFolderAlias) / [HtmlFixedSaveOptions.setResourcesFolderAlias(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions/\#setResourcesFolderAlias-java.lang.String) [SvgSaveOptions.getResourcesFolderAlias()](../../com.aspose.words/svgsaveoptions/\#getResourcesFolderAlias) / [SvgSaveOptions.setResourcesFolderAlias(java.lang.String)](../../com.aspose.words/svgsaveoptions/\#setResourcesFolderAlias-java.lang.String) [MarkdownSaveOptions.getImagesFolderAlias()](../../com.aspose.words/markdownsaveoptions/\#getImagesFolderAlias) / [MarkdownSaveOptions.setImagesFolderAlias(java.lang.String)](../../com.aspose.words/markdownsaveoptions/\#setImagesFolderAlias-java.lang.String)

 **Examples:** 

Bir belgeyi HTML'ye dönüştürürken oluşturulan dış kaynakları izlemek için bir geri çağırma (callback) nasıl kullanılacağını gösterir.

```

 public void resourceSavingCallback() throws Exception {
     Document doc = new Document(getMyDir() + "Bullet points with alternative font.docx");

     FontSavingCallback callback = new FontSavingCallback();

     HtmlFixedSaveOptions saveOptions = new HtmlFixedSaveOptions();
     {
         saveOptions.setResourceSavingCallback(callback);
     }

     doc.save(getArtifactsDir() + "HtmlFixedSaveOptions.UsingMachineFonts.html", saveOptions);

     System.out.println(callback.getText());
 }

 private static class FontSavingCallback implements IResourceSavingCallback {
     /// 
     /// Called when Aspose.Words saves an external resource to fixed page HTML or SVG.
     /// 
     public void resourceSaving(ResourceSavingArgs args) {
         mText.append(MessageFormat.format("Original document URI:\t{0}", args.getDocument().getOriginalFileName()));
         mText.append(MessageFormat.format("Resource being saved:\t{0}", args.getResourceFileName()));
         mText.append(MessageFormat.format("Full uri after saving:\t{0}\n", args.getResourceFileUri()));
     }

     public String getText() {
         return mText.toString();
     }

     private final StringBuilder mText = new StringBuilder();
 }
 
```

**Returns:**
java.lang.String - Belgeden kaynak dosyasına referans vermek için kullanılan tekdüzen kaynak tanımlayıcısı (URI).
### getResourceStream() {#getResourceStream}
```
public OutputStream getResourceStream()
```




**Returns:**
java.io.OutputStream
### setKeepResourceStreamOpen(boolean value) {#setKeepResourceStreamOpen-boolean}
```
public void setKeepResourceStreamOpen(boolean value)
```


Aspose.Words'in akışı açık tutup tutmayacağını veya bir kaynağı kaydettikten sonra kapatıp kapatmayacağını belirtir.

 **Remarks:** 

Varsayılan false ve Aspose.Words, **P:Aspose.Words.Saving.ResourceSavingArgs.ResourceStream** özelliğinde sağladığınız akışı, bir kaynağı içine yazdıktan sonra kapatır. Akışı açık tutmak için true belirtin.

 **Examples:** 

Bir belgeyi HTML'ye dönüştürürken oluşturulan dış kaynakların URI'lerini yazdırmak için bir geri çağırma (callback) nasıl kullanılacağını gösterir.

```

 public void htmlFixedResourceFolder() throws Exception {
     Document doc = new Document(getMyDir() + "Rendering.docx");

     ResourceUriPrinter callback = new ResourceUriPrinter();

     HtmlFixedSaveOptions options = new HtmlFixedSaveOptions();
     {
         options.setSaveFormat(SaveFormat.HTML_FIXED);
         options.setExportEmbeddedImages(false);
         options.setResourcesFolder(getArtifactsDir() + "HtmlFixedResourceFolder");
         options.setResourcesFolderAlias(getArtifactsDir() + "HtmlFixedResourceFolderAlias");
         options.setShowPageBorder(false);
         options.setResourceSavingCallback(callback);
     }

     // A folder specified by ResourcesFolderAlias will contain the resources instead of ResourcesFolder.
     // We must ensure the folder exists before the streams can put their resources into it.
     new File(options.getResourcesFolderAlias()).mkdir();

     doc.save(getArtifactsDir() + "HtmlFixedSaveOptions.HtmlFixedResourceFolder.html", options);

     System.out.println(callback.getText());

     String[] resourceFiles = new File(getArtifactsDir() + "HtmlFixedResourceFolderAlias").list();

     Assert.assertFalse(new File(getArtifactsDir() + "HtmlFixedResourceFolder").exists());
     Assert.assertEquals(6, IterableUtils.countMatches(Arrays.asList(resourceFiles),
             f -> f.endsWith(".jpeg") || f.endsWith(".png") || f.endsWith(".css")));
 }

 /// 
 /// Counts and prints URIs of resources contained by as they are converted to fixed HTML.
 /// 
 private static class ResourceUriPrinter implements IResourceSavingCallback {
     public void resourceSaving(ResourceSavingArgs args) throws Exception {
         // If we set a folder alias in the SaveOptions object, we will be able to print it from here.
         mText.append(MessageFormat.format("Resource #{0} \"{1}\"", ++mSavedResourceCount, args.getResourceFileName()));

         String extension = FilenameUtils.getExtension(args.getResourceFileName());
         switch (extension) {
             case "ttf":
             case "woff": {
                 // By default, 'ResourceFileUri' uses system folder for fonts.
                 // To avoid problems in other platforms you must explicitly specify the path for the fonts.
                 args.setResourceFileUri(getArtifactsDir() + File.separatorChar + args.getResourceFileName());
                 break;
             }
         }

         mText.append("\t" + args.getResourceFileUri());

         // If we have specified a folder in the "ResourcesFolderAlias" property,
         // we will also need to redirect each stream to put its resource in that folder.
         args.setResourceStream(new FileOutputStream(args.getResourceFileUri()));
         args.setKeepResourceStreamOpen(false);
     }

     public String getText() {
         return mText.toString();
     }

     private int mSavedResourceCount;
     private final  StringBuilder mText = new StringBuilder();
 }
 
```

**P:Aspose.Words.Saving.ResourceSavingArgs.ResourceStream**

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### setResourceFileName(String value) {#setResourceFileName-java.lang.String}
```
public void setResourceFileName(String value)
```


Kaynağın kaydedileceği dosya adını (yol olmadan) ayarlar.

 **Remarks:** 

Bu özellik, sabit sayfa HTML, SVG veya Markdown dışa aktarımı sırasında kaynak dosya adlarının nasıl oluşturulduğunu yeniden tanımlamanıza olanak tanır.

Olay tetiklendiğinde, bu özellik Aspose.Words tarafından oluşturulan dosya adını içerir. Kaynağı farklı bir dosyaya kaydetmek için bu özelliğin değerini değiştirebilirsiniz. Dosya adlarının benzersiz olması gerektiğini unutmayın.

Aspose.Words, sabit sayfa HTML, SVG veya Markdown formatına dışa aktarırken her kaynak için otomatik olarak benzersiz bir dosya adı oluşturur. Kaynak dosya adının nasıl oluşturulacağı, belgeyi bir dosyaya mı yoksa bir akışa mı kaydettiğinize bağlıdır.

Bir belgeyi dosyaya kaydederken, oluşturulan kaynak dosya adı *.![Image 1][].* şeklinde görünür.

Bir belgeyi akışa kaydederken, oluşturulan kaynak dosya adı *Aspose.Words..![Image 1][].* şeklinde görünür.

[getResourceFileName()](../../com.aspose.words/resourcesavingargs/\#getResourceFileName) / [setResourceFileName(java.lang.String)](../../com.aspose.words/resourcesavingargs/\#setResourceFileName-java.lang.String) must contain only the file name without the path. Aspose.Words determines the path for saving and the value of the  src  attribute for writing to fixed page HTML, SVG or Markdown using the document file name, the [HtmlFixedSaveOptions.getResourcesFolder()](../../com.aspose.words/htmlfixedsaveoptions/\#getResourcesFolder) / [HtmlFixedSaveOptions.setResourcesFolder(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions/\#setResourcesFolder-java.lang.String) or [SvgSaveOptions.getResourcesFolder()](../../com.aspose.words/svgsaveoptions/\#getResourcesFolder) / [SvgSaveOptions.setResourcesFolder(java.lang.String)](../../com.aspose.words/svgsaveoptions/\#setResourcesFolder-java.lang.String) and [HtmlFixedSaveOptions.getResourcesFolderAlias()](../../com.aspose.words/htmlfixedsaveoptions/\#getResourcesFolderAlias) / [HtmlFixedSaveOptions.setResourcesFolderAlias(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions/\#setResourcesFolderAlias-java.lang.String) or [SvgSaveOptions.getResourcesFolderAlias()](../../com.aspose.words/svgsaveoptions/\#getResourcesFolderAlias) / [SvgSaveOptions.setResourcesFolderAlias(java.lang.String)](../../com.aspose.words/svgsaveoptions/\#setResourcesFolderAlias-java.lang.String) or [MarkdownSaveOptions.getImagesFolder()](../../com.aspose.words/markdownsaveoptions/\#getImagesFolder) / [MarkdownSaveOptions.setImagesFolder(java.lang.String)](../../com.aspose.words/markdownsaveoptions/\#setImagesFolder-java.lang.String) or [MarkdownSaveOptions.getImagesFolderAlias()](../../com.aspose.words/markdownsaveoptions/\#getImagesFolderAlias) / [MarkdownSaveOptions.setImagesFolderAlias(java.lang.String)](../../com.aspose.words/markdownsaveoptions/\#setImagesFolderAlias-java.lang.String) properties.

[HtmlFixedSaveOptions.getResourcesFolder()](../../com.aspose.words/htmlfixedsaveoptions/\#getResourcesFolder) / [HtmlFixedSaveOptions.setResourcesFolder(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions/\#setResourcesFolder-java.lang.String) [SvgSaveOptions.getResourcesFolder()](../../com.aspose.words/svgsaveoptions/\#getResourcesFolder) / [SvgSaveOptions.setResourcesFolder(java.lang.String)](../../com.aspose.words/svgsaveoptions/\#setResourcesFolder-java.lang.String) [HtmlFixedSaveOptions.getResourcesFolderAlias()](../../com.aspose.words/htmlfixedsaveoptions/\#getResourcesFolderAlias) / [HtmlFixedSaveOptions.setResourcesFolderAlias(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions/\#setResourcesFolderAlias-java.lang.String) [SvgSaveOptions.getResourcesFolderAlias()](../../com.aspose.words/svgsaveoptions/\#getResourcesFolderAlias) / [SvgSaveOptions.setResourcesFolderAlias(java.lang.String)](../../com.aspose.words/svgsaveoptions/\#setResourcesFolderAlias-java.lang.String)

 **Examples:** 

Bir belgeyi HTML'ye dönüştürürken oluşturulan dış kaynakları izlemek için bir geri çağırma (callback) nasıl kullanılacağını gösterir.

```

 public void resourceSavingCallback() throws Exception {
     Document doc = new Document(getMyDir() + "Bullet points with alternative font.docx");

     FontSavingCallback callback = new FontSavingCallback();

     HtmlFixedSaveOptions saveOptions = new HtmlFixedSaveOptions();
     {
         saveOptions.setResourceSavingCallback(callback);
     }

     doc.save(getArtifactsDir() + "HtmlFixedSaveOptions.UsingMachineFonts.html", saveOptions);

     System.out.println(callback.getText());
 }

 private static class FontSavingCallback implements IResourceSavingCallback {
     /// 
     /// Called when Aspose.Words saves an external resource to fixed page HTML or SVG.
     /// 
     public void resourceSaving(ResourceSavingArgs args) {
         mText.append(MessageFormat.format("Original document URI:\t{0}", args.getDocument().getOriginalFileName()));
         mText.append(MessageFormat.format("Resource being saved:\t{0}", args.getResourceFileName()));
         mText.append(MessageFormat.format("Full uri after saving:\t{0}\n", args.getResourceFileUri()));
     }

     public String getText() {
         return mText.toString();
     }

     private final StringBuilder mText = new StringBuilder();
 }
 
```

**P:Aspose.Words.Saving.ResourceSavingArgs.ResourceStream**


[Image 1]: 

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | Kaynağın kaydedileceği dosya adı (yol olmadan). |

### setResourceFileUri(String value) {#setResourceFileUri-java.lang.String}
```
public void setResourceFileUri(String value)
```


Belgeden kaynak dosyasına referans vermek için kullanılan tekdüzen kaynak tanımlayıcısını (URI) ayarlar.

 **Remarks:** 

Bu özellik, sabit sayfa HTML, SVG veya Markdown belgelerine dışa aktarılan kaynak dosyalarının URI'lerini değiştirmenize olanak tanır.

Aspose.Words, sabit sayfa HTML, SVG veya Markdown formatına dışa aktarırken her kaynak dosya için otomatik olarak bir URI oluşturur. Oluşturulan URI'ler, Aspose.Words tarafından kaydedilen kaynak dosyalara referans verir. Ancak, kaynak dosyalar başka bir konuma taşınacaksa veya akışlara kaydedilecekse URI'ler hatalı olabilir. Bu özellik, bu durumlarda URI'leri düzeltmenizi sağlar.

Olay tetiklendiğinde, bu özellik Aspose.Words tarafından oluşturulan URI'yi içerir. Kaynak dosya için özel bir URI sağlamak amacıyla bu özelliğin değerini değiştirebilirsiniz.

[HtmlFixedSaveOptions.getResourcesFolder()](../../com.aspose.words/htmlfixedsaveoptions/\#getResourcesFolder) / [HtmlFixedSaveOptions.setResourcesFolder(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions/\#setResourcesFolder-java.lang.String) [SvgSaveOptions.getResourcesFolder()](../../com.aspose.words/svgsaveoptions/\#getResourcesFolder) / [SvgSaveOptions.setResourcesFolder(java.lang.String)](../../com.aspose.words/svgsaveoptions/\#setResourcesFolder-java.lang.String) [MarkdownSaveOptions.getImagesFolder()](../../com.aspose.words/markdownsaveoptions/\#getImagesFolder) / [MarkdownSaveOptions.setImagesFolder(java.lang.String)](../../com.aspose.words/markdownsaveoptions/\#setImagesFolder-java.lang.String) [HtmlFixedSaveOptions.getResourcesFolderAlias()](../../com.aspose.words/htmlfixedsaveoptions/\#getResourcesFolderAlias) / [HtmlFixedSaveOptions.setResourcesFolderAlias(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions/\#setResourcesFolderAlias-java.lang.String) [SvgSaveOptions.getResourcesFolderAlias()](../../com.aspose.words/svgsaveoptions/\#getResourcesFolderAlias) / [SvgSaveOptions.setResourcesFolderAlias(java.lang.String)](../../com.aspose.words/svgsaveoptions/\#setResourcesFolderAlias-java.lang.String) [MarkdownSaveOptions.getImagesFolderAlias()](../../com.aspose.words/markdownsaveoptions/\#getImagesFolderAlias) / [MarkdownSaveOptions.setImagesFolderAlias(java.lang.String)](../../com.aspose.words/markdownsaveoptions/\#setImagesFolderAlias-java.lang.String)

 **Examples:** 

Bir belgeyi HTML'ye dönüştürürken oluşturulan dış kaynakları izlemek için bir geri çağırma (callback) nasıl kullanılacağını gösterir.

```

 public void resourceSavingCallback() throws Exception {
     Document doc = new Document(getMyDir() + "Bullet points with alternative font.docx");

     FontSavingCallback callback = new FontSavingCallback();

     HtmlFixedSaveOptions saveOptions = new HtmlFixedSaveOptions();
     {
         saveOptions.setResourceSavingCallback(callback);
     }

     doc.save(getArtifactsDir() + "HtmlFixedSaveOptions.UsingMachineFonts.html", saveOptions);

     System.out.println(callback.getText());
 }

 private static class FontSavingCallback implements IResourceSavingCallback {
     /// 
     /// Called when Aspose.Words saves an external resource to fixed page HTML or SVG.
     /// 
     public void resourceSaving(ResourceSavingArgs args) {
         mText.append(MessageFormat.format("Original document URI:\t{0}", args.getDocument().getOriginalFileName()));
         mText.append(MessageFormat.format("Resource being saved:\t{0}", args.getResourceFileName()));
         mText.append(MessageFormat.format("Full uri after saving:\t{0}\n", args.getResourceFileUri()));
     }

     public String getText() {
         return mText.toString();
     }

     private final StringBuilder mText = new StringBuilder();
 }
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | Belgeden kaynak dosyasına referans vermek için kullanılan tekdüzen kaynak tanımlayıcısı (URI). |

### setResourceStream(OutputStream value) {#setResourceStream-java.io.OutputStream}
```
public void setResourceStream(OutputStream value)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.io.OutputStream |  |

