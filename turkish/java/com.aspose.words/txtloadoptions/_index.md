---
title: "TxtLoadOptions"
linktitle: "TxtLoadOptions"
second_title: "Aspose.Words Java için"
description: "Java'da LoadFormat.TEXT belgesini bir Document nesnesine yüklerken ek seçenekler belirtmeye izin verir."
type: docs
weight: 693
url: /tr/java/com.aspose.words/txtloadoptions/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.LoadOptions](../../com.aspose.words/loadoptions/)
```
public class TxtLoadOptions extends LoadOptions
```

Belgeyi bir [Document](../../com.aspose.words/document/) nesnesine yüklerken [LoadFormat.TEXT](../../com.aspose.words/loadformat/\#TEXT) belgesi için ek seçenekler belirtmeye izin verir.

Daha fazla bilgi edinmek için, [ Specify Load Options ][Specify Load Options] dokümantasyon makalesini ziyaret edin.

 **Examples:** 

Köprüleri okuma ve görüntüleme yöntemini gösterir.

```

 final String INPUT_TEXT = "Some links in TXT:\n" +
         "https://www.aspose.com/\n" +
         "https://docs.aspose.com/words/net/\n";

 try (ByteArrayInputStream stream = new ByteArrayInputStream(INPUT_TEXT.getBytes(StandardCharsets.US_ASCII)))
 {
     // Load document with hyperlinks.
     TxtLoadOptions loadOptions = new TxtLoadOptions();
     loadOptions.setDetectHyperlinks(true);
     Document doc = new Document(stream, loadOptions);

     // Print hyperlinks text.
     for (Field field : doc.getRange().getFields())
         System.out.println(field.getResult());

     Assert.assertEquals(doc.getRange().getFields().get(0).getResult().trim(), "https://www.aspose.com/");
     Assert.assertEquals(doc.getRange().getFields().get(1).getResult().trim(), "https://docs.aspose.com/words/net/");
 }
 
```


[Specify Load Options]: https://docs.aspose.com/words/java/specify-load-options/
## Yapıcılar

| Yapıcı | Açıklama |
| --- | --- |
| [TxtLoadOptions()](#TxtLoadOptions) | Bu sınıfın yeni bir örneğini varsayılan değerlerle başlatır. |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [equals(Object obj)](#equals-java.lang.Object) | Belirtilen nesnenin, mevcut nesneyle değer olarak eşit olup olmadığını belirler. |
| [getAutoNumberingDetection()](#getAutoNumberingDetection) | Bir belge yüklenirken otomatik numaralandırma algılamasının yapılacağını belirten bir boolean değer alır. |
| [getBaseUri()](#getBaseUri) | Gerekli olduğunda belgede bulunan göreli URI'leri mutlak URI'lere dönüştürmek için kullanılacak dizeyi alır. |
| [getConvertMetafilesToPng()](#getConvertMetafilesToPng) | Metafile (**F:Aspose.FileFormat.Wmf** veya **F:Aspose.FileFormat.Emf**) görüntülerini **F:Aspose.FileFormat.Png** görüntü formatına dönüştürülüp dönüştürülmeyeceğini alır. |
| [getConvertShapeToOfficeMath()](#getConvertShapeToOfficeMath) | EquationXML içeren şekilleri Office Math nesnelerine dönüştürülüp dönüştürülmeyeceğini alır. |
| [getDetectHyperlinks()](#getDetectHyperlinks) | Metindeki köprüleri algılamayı belirtir. |
| [getDetectNumberingWithWhitespaces()](#getDetectNumberingWithWhitespaces) | Belge düz metin formatından içe aktarıldığında numaralı liste öğelerinin nasıl tanındığını belirtmeye izin verir. |
| [getDocumentDirection()](#getDocumentDirection) | Bir belge yönünü alır. |
| [getEncoding()](#getEncoding) | Belge içinde kodlama belirtilmemişse, bir HTML, TXT veya CHM belgesini yüklemek için kullanılacak kodlamayı alır. |
| [getFontSettings()](#getFontSettings) | Belge yazı tipi ayarlarını belirtmeye izin verir. |
| [getIgnoreOleData()](#getIgnoreOleData) | OLE verilerinin göz ardı edilip edilmeyeceğini belirtir. |
| [getLanguagePreferences()](#getLanguagePreferences) | Belge yüklenirken kullanılacak dil tercihlerini alır. |
| [getLeadingSpacesOptions()](#getLeadingSpacesOptions) | Başta gelen boşluk işleme için tercih edilen seçeneği alır. |
| [getLoadFormat()](#getLoadFormat) | Yüklenecek belgenin formatını belirtir. |
| [getMswVersion()](#getMswVersion) | Belge yükleme işleminin belirli bir MS Word sürümüyle eşleşmesi gerektiğini belirtmeye izin verir. |
| [getPassword()](#getPassword) | Şifreli bir belgeyi açmak için parolayı alır. |
| [getPreserveIncludePictureField()](#getPreserveIncludePictureField) | Microsoft Word formatlarını okurken INCLUDEPICTURE alanının korunup korunmayacağını alır. |
| [getProgressCallback()](#getProgressCallback) | Bir belge yüklenirken çağrılır ve yükleme ilerlemesiyle ilgili verileri kabul eder. |
| [getRecoveryMode()](#getRecoveryMode) | Yükleme sırasında hatalar oluşursa belgenin nasıl işleneceğini tanımlar. |
| [getResourceLoadingCallback()](#getResourceLoadingCallback) | Bir belge HTML veya MHTML'den içe aktarıldığında dış kaynakların (görüntüler, stil sayfaları) nasıl yükleneceğini kontrol etmeye izin verir. |
| [getTempFolder()](#getTempFolder) | Belge okunurken geçici dosyaların kullanılmasına izin verir. |
| [getTrailingSpacesOptions()](#getTrailingSpacesOptions) | Sondaki boşluk işleme için tercih edilen seçeneği alır. |
| [getUpdateDirtyFields()](#getUpdateDirtyFields) | Alanları  dirty  özniteliğiyle güncelleyip güncellemeyeceğini belirtir. |
| [getUseSystemLcid()](#getUseSystemLcid) | Sayfa ayarı varsayılan kenar boşluklarını belirlemek için Windows kayıt defterinden alınan LCID değerinin kullanılıp kullanılmayacağını alır. |
| [getWarningCallback()](#getWarningCallback) | Veri veya biçimlendirme doğruluğunun kaybolmasına neden olabilecek bir sorun tespit edildiğinde, yükleme işlemi sırasında çağrılır. |
| [setAutoNumberingDetection(boolean value)](#setAutoNumberingDetection-boolean) | Bir belge yüklenirken otomatik numaralandırma algılamasının yapılacağını belirten bir boolean değer ayarlar. |
| [setBaseUri(String value)](#setBaseUri-java.lang.String) | Gerekli olduğunda belgede bulunan göreli URI'leri mutlak URI'lere dönüştürmek için kullanılacak dizeyi ayarlar. |
| [setConvertMetafilesToPng(boolean value)](#setConvertMetafilesToPng-boolean) | Metafile ( **F:Aspose.FileFormat.Wmf** veya **F:Aspose.FileFormat.Emf**) görüntülerinin **F:Aspose.FileFormat.Png** görüntü formatına dönüştürülüp dönüştürülmeyeceğini ayarlar. |
| [setConvertShapeToOfficeMath(boolean value)](#setConvertShapeToOfficeMath-boolean) | EquationXML içeren şekillerin Office Math nesnelerine dönüştürülüp dönüştürülmeyeceğini ayarlar. |
| [setDetectHyperlinks(boolean value)](#setDetectHyperlinks-boolean) | Metindeki köprüleri algılamayı belirtir. |
| [setDetectNumberingWithWhitespaces(boolean value)](#setDetectNumberingWithWhitespaces-boolean) | Belge düz metin formatından içe aktarıldığında numaralı liste öğelerinin nasıl tanındığını belirtmeye izin verir. |
| [setDocumentDirection(int value)](#setDocumentDirection-int) | Bir belge yönünü ayarlar. |
| [setEncoding(Charset value)](#setEncoding-java.nio.charset.Charset) | Belge içinde kodlama belirtilmemişse bir HTML, TXT veya CHM belgesini yüklemek için kullanılacak kodlamayı ayarlar. |
| [setFontSettings(FontSettings value)](#setFontSettings-com.aspose.words.FontSettings) | Belge yazı tipi ayarlarını belirtmeye izin verir. |
| [setIgnoreOleData(boolean value)](#setIgnoreOleData-boolean) | OLE verilerinin göz ardı edilip edilmeyeceğini belirtir. |
| [setLeadingSpacesOptions(int value)](#setLeadingSpacesOptions-int) | Başta gelen boşluk işleme için tercih edilen seçeneği ayarlar. |
| [setLoadFormat(int value)](#setLoadFormat-int) | Yüklenecek belgenin formatını belirtir. |
| [setMswVersion(int value)](#setMswVersion-int) | Belge yükleme işleminin belirli bir MS Word sürümüyle eşleşmesi gerektiğini belirtmeye izin verir. |
| [setPassword(String value)](#setPassword-java.lang.String) | Şifreli bir belgeyi açmak için şifreyi ayarlar. |
| [setPreserveIncludePictureField(boolean value)](#setPreserveIncludePictureField-boolean) | Microsoft Word formatlarını okurken INCLUDEPICTURE alanının korunup korunmayacağını ayarlar. |
| [setProgressCallback(IDocumentLoadingCallback value)](#setProgressCallback-com.aspose.words.IDocumentLoadingCallback) | Bir belge yüklenirken çağrılır ve yükleme ilerlemesiyle ilgili verileri kabul eder. |
| [setRecoveryMode(int value)](#setRecoveryMode-int) | Yükleme sırasında hatalar oluşursa belgenin nasıl işleneceğini tanımlar. |
| [setResourceLoadingCallback(IResourceLoadingCallback value)](#setResourceLoadingCallback-com.aspose.words.IResourceLoadingCallback) | Bir belge HTML veya MHTML'den içe aktarıldığında dış kaynakların (görüntüler, stil sayfaları) nasıl yükleneceğini kontrol etmeye izin verir. |
| [setTempFolder(String value)](#setTempFolder-java.lang.String) | Belge okunurken geçici dosyaların kullanılmasına izin verir. |
| [setTrailingSpacesOptions(int value)](#setTrailingSpacesOptions-int) | Sondaki boşluk işleme için tercih edilen seçeneği ayarlar. |
| [setUpdateDirtyFields(boolean value)](#setUpdateDirtyFields-boolean) | Alanları  dirty  özniteliğiyle güncelleyip güncellemeyeceğini belirtir. |
| [setUseSystemLcid(boolean value)](#setUseSystemLcid-boolean) | Sayfa ayarı varsayılan kenar boşluklarını belirlemek için Windows kayıt defterinden alınan LCID değerinin kullanılıp kullanılmayacağını ayarlar. |
| [setWarningCallback(IWarningCallback value)](#setWarningCallback-com.aspose.words.IWarningCallback) | Veri veya biçimlendirme doğruluğunun kaybolmasına neden olabilecek bir sorun tespit edildiğinde, yükleme işlemi sırasında çağrılır. |
### TxtLoadOptions() {#TxtLoadOptions}
```
public TxtLoadOptions()
```


Bu sınıfın yeni bir örneğini varsayılan değerlerle başlatır.

 **Examples:** 

Köprüleri okuma ve görüntüleme yöntemini gösterir.

```

 final String INPUT_TEXT = "Some links in TXT:\n" +
         "https://www.aspose.com/\n" +
         "https://docs.aspose.com/words/net/\n";

 try (ByteArrayInputStream stream = new ByteArrayInputStream(INPUT_TEXT.getBytes(StandardCharsets.US_ASCII)))
 {
     // Load document with hyperlinks.
     TxtLoadOptions loadOptions = new TxtLoadOptions();
     loadOptions.setDetectHyperlinks(true);
     Document doc = new Document(stream, loadOptions);

     // Print hyperlinks text.
     for (Field field : doc.getRange().getFields())
         System.out.println(field.getResult());

     Assert.assertEquals(doc.getRange().getFields().get(0).getResult().trim(), "https://www.aspose.com/");
     Assert.assertEquals(doc.getRange().getFields().get(1).getResult().trim(), "https://docs.aspose.com/words/net/");
 }
 
```

### equals(Object obj) {#equals-java.lang.Object}
```
public boolean equals(Object obj)
```


Belirtilen nesnenin, mevcut nesneyle değer olarak eşit olup olmadığını belirler.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| obj | java.lang.Object |  |

**Returns:**
boolean
### getAutoNumberingDetection() {#getAutoNumberingDetection}
```
public boolean getAutoNumberingDetection()
```


Bir belge yüklenirken otomatik numaralandırma algılamasının yapılacağını belirten bir boolean değer alır. Varsayılan değer true.

 **Examples:** 

Otomatik numaralandırma algılamasını devre dışı bırakmanın nasıl yapılacağını gösterir.

```

 TxtLoadOptions options = new TxtLoadOptions(); { options.setAutoNumberingDetection(false); }
 Document doc = new Document(getMyDir() + "Number detection.txt", options);
 
```

**Returns:**
boolean - Bir belge yüklenirken otomatik numaralandırma algılamasının gerçekleştirileceğini belirten boolean değer.
### getBaseUri() {#getBaseUri}
```
public String getBaseUri()
```


Belge içinde bulunan göreli URI'leri gerektiğinde mutlak URI'lere dönüştürmek için kullanılacak dizeyi alır. Boş  null  veya boş dize olabilir. Varsayılan  null  .

 **Remarks:** 

Bu özellik, göreli URI'leri mutlak URI'lere dönüştürmek için aşağıdaki durumlarda kullanılır:

1.  Bir akıştan HTML belgesi yüklenirken ve belge göreli URI'li görseller içerdiğinde ve BASE HTML öğesinde bir temel URI belirtilmemişse.
2.  Bir belge PDF ve diğer formatlara kaydedilirken, göreli URI'ler kullanılarak bağlanan görselleri alarak bu görsellerin çıktı belgesine kaydedilmesini sağlamak için.

 **Examples:** 

Bir akıştan temel URI kullanarak görseller içeren bir HTML belgesinin nasıl açılacağını gösterir.

```

 InputStream stream = new FileInputStream(getMyDir() + "Document.html");
 try  {
     // Pass the URI of the base folder while loading it
     // so that any images with relative URIs in the HTML document can be found.
     LoadOptions loadOptions = new LoadOptions();
     loadOptions.setBaseUri(getImageDir());

     Document doc = new Document(stream, loadOptions);

     // Verify that the first shape of the document contains a valid image.
     Shape shape = (Shape) doc.getChild(NodeType.SHAPE, 0, true);

     Assert.assertTrue(shape.isImage());
     Assert.assertNotNull(shape.getImageData().getImageBytes());
     Assert.assertEquals(32.0, ConvertUtil.pointToPixel(shape.getWidth()), 0.01);
     Assert.assertEquals(32.0, ConvertUtil.pointToPixel(shape.getHeight()), 0.01);
 } finally {
     if (stream != null) stream.close();
 }
 
```

**Returns:**
java.lang.String - Belge içinde bulunan göreli URI'leri gerektiğinde mutlak URI'lere dönüştürmek için kullanılacak dize.
### getConvertMetafilesToPng() {#getConvertMetafilesToPng}
```
public boolean getConvertMetafilesToPng()
```


Metafile (**F:Aspose.FileFormat.Wmf** veya **F:Aspose.FileFormat.Emf**) görüntülerini **F:Aspose.FileFormat.Png** görüntü formatına dönüştürülüp dönüştürülmeyeceğini alır.

 **Remarks:** 

Metafile'lar ( **F:Aspose.FileFormat.Wmf** veya **F:Aspose.FileFormat.Emf**) sıkıştırılmamış bir görüntü formatıdır ve bazen belgeyi tutmak ve işlemek için çok fazla RAM gerektirir. Bu seçenek, belge yüklenirken tüm metafile görüntülerini **F:Aspose.FileFormat.Png**'ye dönüştürmeye olanak tanır. Lütfen unutmayın - vektör grafikleri rastere dönüştürmek görüntü kalitesini düşürür.

 **Examples:** 

Belge yüklenirken WMF/EMF'nin PNG'ye nasıl dönüştürüleceğini gösterir.

```

 Document doc = new Document();

 Shape shape = new Shape(doc, ShapeType.IMAGE);
 shape.getImageData().setImage(getImageDir() + "Windows MetaFile.wmf");
 shape.setWidth(100.0);
 shape.setHeight(100.0);

 doc.getFirstSection().getBody().getFirstParagraph().appendChild(shape);

 doc.save(getArtifactsDir() + "Image.CreateImageDirectly.docx");

 shape = (Shape) doc.getChild(NodeType.SHAPE, 0, true);

 TestUtil.verifyImageInShape(1600, 1600, ImageType.WMF, shape);

 LoadOptions loadOptions = new LoadOptions();
 loadOptions.setConvertMetafilesToPng(true);

 doc = new Document(getArtifactsDir() + "Image.CreateImageDirectly.docx", loadOptions);
 shape = (Shape) doc.getChild(NodeType.SHAPE, 0, true);

 TestUtil.verifyImageInShape(1600, 1600, ImageType.PNG, shape);
 
```

**Returns:**
boolean - Metafile ( **F:Aspose.FileFormat.Wmf** veya **F:Aspose.FileFormat.Emf**) görüntülerinin **F:Aspose.FileFormat.Png** görüntü formatına dönüştürülüp dönüştürülmeyeceği.
### getConvertShapeToOfficeMath() {#getConvertShapeToOfficeMath}
```
public boolean getConvertShapeToOfficeMath()
```


EquationXML içeren şekilleri Office Math nesnelerine dönüştürülüp dönüştürülmeyeceğini alır.

 **Examples:** 

EquationXML şekillerinin Office Math nesnelerine nasıl dönüştürüleceğini gösterir.

```

 LoadOptions loadOptions = new LoadOptions();

 // Use this flag to specify whether to convert the shapes with EquationXML attributes
 // to Office Math objects and then load the document.
 loadOptions.setConvertShapeToOfficeMath(isConvertShapeToOfficeMath);

 Document doc = new Document(getMyDir() + "Math shapes.docx", loadOptions);

 if (isConvertShapeToOfficeMath) {
     Assert.assertEquals(16, doc.getChildNodes(NodeType.SHAPE, true).getCount());
     Assert.assertEquals(34, doc.getChildNodes(NodeType.OFFICE_MATH, true).getCount());
 } else {
     Assert.assertEquals(24, doc.getChildNodes(NodeType.SHAPE, true).getCount());
     Assert.assertEquals(0, doc.getChildNodes(NodeType.OFFICE_MATH, true).getCount());
 }
 
```

**Returns:**
boolean - EquationXML içeren şekillerin Office Math nesnelerine dönüştürülüp dönüştürülmeyeceği.
### getDetectHyperlinks() {#getDetectHyperlinks}
```
public boolean getDetectHyperlinks()
```


Metinde hiperlinklerin algılanıp algılanmayacağını belirtir. Varsayılan değer false'tur.

 **Examples:** 

Köprüleri okuma ve görüntüleme yöntemini gösterir.

```

 final String INPUT_TEXT = "Some links in TXT:\n" +
         "https://www.aspose.com/\n" +
         "https://docs.aspose.com/words/net/\n";

 try (ByteArrayInputStream stream = new ByteArrayInputStream(INPUT_TEXT.getBytes(StandardCharsets.US_ASCII)))
 {
     // Load document with hyperlinks.
     TxtLoadOptions loadOptions = new TxtLoadOptions();
     loadOptions.setDetectHyperlinks(true);
     Document doc = new Document(stream, loadOptions);

     // Print hyperlinks text.
     for (Field field : doc.getRange().getFields())
         System.out.println(field.getResult());

     Assert.assertEquals(doc.getRange().getFields().get(0).getResult().trim(), "https://www.aspose.com/");
     Assert.assertEquals(doc.getRange().getFields().get(1).getResult().trim(), "https://docs.aspose.com/words/net/");
 }
 
```

**Returns:**
boolean - İlgili  boolean  değeri.
### getDetectNumberingWithWhitespaces() {#getDetectNumberingWithWhitespaces}
```
public boolean getDetectNumberingWithWhitespaces()
```


Belge düz metin formatından içe aktarıldığında numaralı liste öğelerinin nasıl tanınacağını belirtmeye olanak tanır. Varsayılan değer true'tur.

 **Remarks:** 

Bu seçenek false olarak ayarlanırsa, liste tanıma algoritması, liste numaraları nokta, sağ köşeli parantez veya madde işareti (örneğin "\\u2022", "*", "-" veya "o") ile bittiğinde liste paragraflarını algılar.

Bu seçenek true olarak ayarlanırsa, boşluk karakterleri de liste numarası ayırıcıları olarak kullanılır: Arapça stil numaralandırma (1., 1.1.2.) için liste tanıma algoritması hem boşlukları hem de nokta (".") sembollerini kullanır.

 **Examples:** 

Düz metin belgeleri yüklenirken listelerin nasıl algılanacağını gösterir.

```

 // Create a plaintext document in a string with four separate parts that we may interpret as lists,
 // with different delimiters. Upon loading the plaintext document into a "Document" object,
 // Aspose.Words will always detect the first three lists and will add a "List" object
 // for each to the document's "Lists" property.
 final String TEXT_DOC = "Full stop delimiters:\n" +
         "1. First list item 1\n" +
         "2. First list item 2\n" +
         "3. First list item 3\n\n" +
         "Right bracket delimiters:\n" +
         "1) Second list item 1\n" +
         "2) Second list item 2\n" +
         "3) Second list item 3\n\n" +
         "Bullet delimiters:\n" +
         "\u2022 Third list item 1\n" +
         "\u2022 Third list item 2\n" +
         "\u2022 Third list item 3\n\n" +
         "Whitespace delimiters:\n" +
         "1 Fourth list item 1\n" +
         "2 Fourth list item 2\n" +
         "3 Fourth list item 3";

 // Create a "TxtLoadOptions" object, which we can pass to a document's constructor
 // to modify how we load a plaintext document.
 TxtLoadOptions loadOptions = new TxtLoadOptions();

 // Set the "DetectNumberingWithWhitespaces" property to "true" to detect numbered items
 // with whitespace delimiters, such as the fourth list in our document, as lists.
 // This may also falsely detect paragraphs that begin with numbers as lists.
 // Set the "DetectNumberingWithWhitespaces" property to "false"
 // to not create lists from numbered items with whitespace delimiters.
 loadOptions.setDetectNumberingWithWhitespaces(detectNumberingWithWhitespaces);

 Document doc = new Document(new ByteArrayInputStream(TEXT_DOC.getBytes()), loadOptions);

 List paragraphList = Arrays.stream(doc.getFirstSection().getBody().getParagraphs().toArray())
         .filter(Paragraph.class::isInstance)
         .map(Paragraph.class::cast)
         .collect(Collectors.toList());

 if (detectNumberingWithWhitespaces) {
     Assert.assertEquals(4, doc.getLists().getCount());
     Assert.assertTrue(IterableUtils.matchesAny(paragraphList, s -> s.getText().contains("Fourth list") && s.isListItem()));
 } else {
     Assert.assertEquals(3, doc.getLists().getCount());
     Assert.assertFalse(IterableUtils.matchesAny(paragraphList, s -> s.getText().contains("Fourth list") && s.isListItem()));
 }
 
```

**Returns:**
boolean - İlgili  boolean  değeri.
### getDocumentDirection() {#getDocumentDirection}
```
public int getDocumentDirection()
```


Bir belge yönünü alır. Varsayılan değer [DocumentDirection.LEFT\_TO\_RIGHT](../../com.aspose.words/documentdirection/\#LEFT-TO-RIGHT) dir.

 **Examples:** 

Düz metin belge metin yönünün nasıl algılanacağını gösterir.

```

 // Create a "TxtLoadOptions" object, which we can pass to a document's constructor
 // to modify how we load a plaintext document.
 TxtLoadOptions loadOptions = new TxtLoadOptions();

 // Set the "DocumentDirection" property to "DocumentDirection.Auto" automatically detects
 // the direction of every paragraph of text that Aspose.Words loads from plaintext.
 // Each paragraph's "Bidi" property will store its direction.
 loadOptions.setDocumentDirection(DocumentDirection.AUTO);

 // Detect Hebrew text as right-to-left.
 Document doc = new Document(getMyDir() + "Hebrew text.txt", loadOptions);

 Assert.assertTrue(doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat().getBidi());

 // Detect English text as right-to-left.
 doc = new Document(getMyDir() + "English text.txt", loadOptions);

 Assert.assertFalse(doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat().getBidi());
 
```

**Returns:**
int - Bir belge yönü. Döndürülen değer [DocumentDirection](../../com.aspose.words/documentdirection/) sabitlerinden biridir.
### getEncoding() {#getEncoding}
```
public Charset getEncoding()
```


Belge içinde kodlama belirtilmemişse bir HTML, TXT veya CHM belgesini yüklemek için kullanılacak kodlamayı alır.  null  olabilir. Varsayılan  null  .

 **Remarks:** 

Bu özellik yalnızca HTML, TXT veya CHM belgeleri yüklenirken kullanılır.

Kodlama belge içinde belirtilmemişse ve bu özellik  null  ise, sistem kodlamayı otomatik olarak tespit etmeye çalışır.

 **Examples:** 

Bir belgeyi açmak için kullanılacak kodlamanın nasıl ayarlanacağını gösterir.

```

 LoadOptions loadOptions = new LoadOptions();
 {
     loadOptions.setEncoding(StandardCharsets.US_ASCII);
 }

 // Load the document while passing the LoadOptions object, then verify the document's contents.
 Document doc = new Document(getMyDir() + "English text.txt", loadOptions);

 Assert.assertTrue(doc.toString(SaveFormat.TEXT).contains("This is a sample text in English."));
 
```

**Returns:**
java.nio.charset.Charset - Belge içinde kodlama belirtilmemişse bir HTML, TXT veya CHM belgesini yüklemek için kullanılacak kodlama.
### getFontSettings() {#getFontSettings}
```
public FontSettings getFontSettings()
```


Belge yazı tipi ayarlarını belirtmeye izin verir.

 **Remarks:** 

Bazı formatlar yüklenirken Aspose.Words yazı tiplerini çözümlemek zorunda kalabilir. Örneğin, HTML belgeleri yüklenirken Aspose.Words yazı tiplerini çözerek font geri dönüşümünü gerçekleştirebilir.

null  olarak ayarlanırsa, varsayılan statik yazı tipi ayarları [FontSettings.getDefaultInstance()](../../com.aspose.words/fontsettings/\#getDefaultInstance) kullanılacaktır.

Varsayılan değer  null  dır.

 **Examples:** 

Yükleme sırasında yazı tipi ikamelerini nasıl belirleyeceğinizi gösterir.

```

 LoadOptions loadOptions = new LoadOptions();
 loadOptions.setFontSettings(new FontSettings());

 // Set a font substitution rule for a LoadOptions object.
 // If the document we are loading uses a font which we do not have,
 // this rule will substitute the unavailable font with one that does exist.
 // In this case, all uses of the "MissingFont" will convert to "Comic Sans MS".
 TableSubstitutionRule substitutionRule = loadOptions.getFontSettings().getSubstitutionSettings().getTableSubstitution();
 substitutionRule.addSubstitutes("MissingFont", "Comic Sans MS");

 Document doc = new Document(getMyDir() + "Missing font.html", loadOptions);

 // At this point such text will still be in "MissingFont".
 // Font substitution will take place when we render the document.
 Assert.assertEquals("MissingFont", doc.getFirstSection().getBody().getFirstParagraph().getRuns().get(0).getFont().getName());

 doc.save(getArtifactsDir() + "FontSettings.ResolveFontsBeforeLoadingDocument.pdf");
 
```

Bir belgeyi yüklerken yazı tipi ikame ayarlarını nasıl uygulayacağınızı gösterir.

```

 // Create a FontSettings object that will substitute the "Times New Roman" font
 // with the font "Arvo" from our "MyFonts" folder.
 FontSettings fontSettings = new FontSettings();
 fontSettings.setFontsFolder(getFontsDir(), false);
 fontSettings.getSubstitutionSettings().getTableSubstitution().addSubstitutes("Times New Roman", "Arvo");

 // Set that FontSettings object as a property of a newly created LoadOptions object.
 LoadOptions loadOptions = new LoadOptions();
 loadOptions.setFontSettings(fontSettings);

 // Load the document, then render it as a PDF with the font substitution.
 Document doc = new Document(getMyDir() + "Document.docx", loadOptions);

 doc.save(getArtifactsDir() + "LoadOptions.FontSettings.pdf");
 
```

**Returns:**
[FontSettings](../../com.aspose.words/fontsettings/) - The corresponding [FontSettings](../../com.aspose.words/fontsettings/) value.
### getIgnoreOleData() {#getIgnoreOleData}
```
public boolean getIgnoreOleData()
```


OLE verilerinin göz ardı edilip edilmeyeceğini belirtir.

 **Remarks:** 

OLE verisinin yok sayılması, hedef format OLE nesnelerini desteklemediğinde veri kaybı olmadan bellek tüketimini azaltabilir ve performansı artırabilir.

Varsayılan değer  false  dır.

 **Examples:** 

Yükleme sırasında OLE verisinin yok sayılmasını gösterir.

```

 // Ignoring OLE data may reduce memory consumption and increase performance
 // without data lost in a case when destination format does not support OLE objects.
 LoadOptions loadOptions = new LoadOptions();
 loadOptions.setIgnoreOleData(true);
 Document doc = new Document(getMyDir() + "OLE objects.docx", loadOptions);

 doc.save(getArtifactsDir() + "LoadOptions.IgnoreOleData.docx");
 
```

**Returns:**
boolean - İlgili  boolean  değeri.
### getLanguagePreferences() {#getLanguagePreferences}
```
public LanguagePreferences getLanguagePreferences()
```


Belge yüklenirken kullanılacak dil tercihlerini alır.

 **Examples:** 

Bir belgeyi yüklerken dil tercihlerini nasıl uygulayacağınızı gösterir.

```

 LoadOptions loadOptions = new LoadOptions();
 loadOptions.getLanguagePreferences().addEditingLanguage(EditingLanguage.JAPANESE);

 Document doc = new Document(getMyDir() + "No default editing language.docx", loadOptions);

 int localeIdFarEast = doc.getStyles().getDefaultFont().getLocaleIdFarEast();
 System.out.println(localeIdFarEast == EditingLanguage.JAPANESE
         ? "The document either has no any FarEast language set in defaults or it was set to Japanese originally."
         : "The document default FarEast language was set to another than Japanese language originally, so it is not overridden.");
 
```

**Returns:**
[LanguagePreferences](../../com.aspose.words/languagepreferences/) - Language preferences that will be used when document is loading.
### getLeadingSpacesOptions() {#getLeadingSpacesOptions}
```
public int getLeadingSpacesOptions()
```


Ön boşluk işleme için tercih edilen seçeneği alır. Varsayılan değer [TxtLeadingSpacesOptions.CONVERT\_TO\_INDENT](../../com.aspose.words/txtleadingspacesoptions/\#CONVERT-TO-INDENT) dir.

 **Examples:** 

Düz metin belgeleri yüklenirken boşlukların nasıl kırpılacağını gösterir.

```

 String textDoc = "      Line 1 \n" +
         "    Line 2   \n" +
         " Line 3       ";

 // Create a "TxtLoadOptions" object, which we can pass to a document's constructor
 // to modify how we load a plaintext document.
 TxtLoadOptions loadOptions = new TxtLoadOptions();

 // Set the "LeadingSpacesOptions" property to "TxtLeadingSpacesOptions.Preserve"
 // to preserve all whitespace characters at the start of every line.
 // Set the "LeadingSpacesOptions" property to "TxtLeadingSpacesOptions.ConvertToIndent"
 // to remove all whitespace characters from the start of every line,
 // and then apply a left first line indent to the paragraph to simulate the effect of the whitespaces.
 // Set the "LeadingSpacesOptions" property to "TxtLeadingSpacesOptions.Trim"
 // to remove all whitespace characters from every line's start.
 loadOptions.setLeadingSpacesOptions(txtLeadingSpacesOptions);

 // Set the "TrailingSpacesOptions" property to "TxtTrailingSpacesOptions.Preserve"
 // to preserve all whitespace characters at the end of every line.
 // Set the "TrailingSpacesOptions" property to "TxtTrailingSpacesOptions.Trim" to
 // remove all whitespace characters from the end of every line.
 loadOptions.setTrailingSpacesOptions(txtTrailingSpacesOptions);

 Document doc = new Document(new ByteArrayInputStream(textDoc.getBytes()), loadOptions);
 ParagraphCollection paragraphs = doc.getFirstSection().getBody().getParagraphs();

 switch (txtLeadingSpacesOptions) {
     case TxtLeadingSpacesOptions.CONVERT_TO_INDENT:
         Assert.assertEquals(37.8d, paragraphs.get(0).getParagraphFormat().getFirstLineIndent());
         Assert.assertEquals(25.2d, paragraphs.get(1).getParagraphFormat().getFirstLineIndent());
         Assert.assertEquals(6.3d, paragraphs.get(2).getParagraphFormat().getFirstLineIndent());

         Assert.assertTrue(paragraphs.get(0).getText().startsWith("Line 1"));
         Assert.assertTrue(paragraphs.get(1).getText().startsWith("Line 2"));
         Assert.assertTrue(paragraphs.get(2).getText().startsWith("Line 3"));
         break;
     case TxtLeadingSpacesOptions.PRESERVE:
         Assert.assertTrue(IterableUtils.matchesAll(paragraphs, s -> s.getParagraphFormat().getFirstLineIndent() == 0.0d));

         Assert.assertTrue(paragraphs.get(0).getText().startsWith("      Line 1"));
         Assert.assertTrue(paragraphs.get(1).getText().startsWith("    Line 2"));
         Assert.assertTrue(paragraphs.get(2).getText().startsWith(" Line 3"));
         break;
     case TxtLeadingSpacesOptions.TRIM:
         Assert.assertTrue(IterableUtils.matchesAll(paragraphs, s -> s.getParagraphFormat().getFirstLineIndent() == 0.0d));

         Assert.assertTrue(paragraphs.get(0).getText().startsWith("Line 1"));
         Assert.assertTrue(paragraphs.get(1).getText().startsWith("Line 2"));
         Assert.assertTrue(paragraphs.get(2).getText().startsWith("Line 3"));
         break;
 }

 switch (txtTrailingSpacesOptions) {
     case TxtTrailingSpacesOptions.PRESERVE:
         Assert.assertTrue(paragraphs.get(0).getText().endsWith("Line 1 \r"));
         Assert.assertTrue(paragraphs.get(1).getText().endsWith("Line 2   \r"));
         Assert.assertTrue(paragraphs.get(2).getText().endsWith("Line 3       \f"));
         break;
     case TxtTrailingSpacesOptions.TRIM:
         Assert.assertTrue(paragraphs.get(0).getText().endsWith("Line 1\r"));
         Assert.assertTrue(paragraphs.get(1).getText().endsWith("Line 2\r"));
         Assert.assertTrue(paragraphs.get(2).getText().endsWith("Line 3\f"));
         break;
 }
 
```

**Returns:**
int - Ön boşluk işleme için tercih edilen seçenek. Döndürülen değer [TxtLeadingSpacesOptions](../../com.aspose.words/txtleadingspacesoptions/) sabitlerinden biridir.
### getLoadFormat() {#getLoadFormat}
```
public int getLoadFormat()
```


Yüklenecek belgenin formatını belirtir. Varsayılan değer [LoadFormat.AUTO](../../com.aspose.words/loadformat/\#AUTO) dır.

 **Remarks:** 

Dosya formatını otomatik olarak algılaması için [LoadFormat.AUTO](../../com.aspose.words/loadformat/\#AUTO) değerini belirtmeniz önerilir. Yüklemek üzere olduğunuz belgenin formatını biliyorsanız, formatı açıkça belirtebilir ve bu, formatın otomatik algılanmasıyla ilgili ek yükü azaltarak yükleme süresini biraz kısaltır. Açık bir yükleme formatı belirtir ve bu format yanlış çıkarsa, otomatik algılama devreye girer ve dosyayı yüklemek için ikinci bir deneme yapılır.

 **Examples:** 

HTML belgesi açarken temel bir URI nasıl belirtileceğini gösterir.

```

 // Suppose we want to load an .html document that contains an image linked by a relative URI
 // while the image is in a different location. In that case, we will need to resolve the relative URI into an absolute one.
 // We can provide a base URI using an HtmlLoadOptions object.
 HtmlLoadOptions loadOptions = new HtmlLoadOptions(LoadFormat.HTML, "", getImageDir());

 Assert.assertEquals(LoadFormat.HTML, loadOptions.getLoadFormat());

 Document doc = new Document(getMyDir() + "Missing image.html", loadOptions);

 // While the image was broken in the input .html, our custom base URI helped us repair the link.
 Shape imageShape = (Shape) doc.getChildNodes(NodeType.SHAPE, true).get(0);
 Assert.assertTrue(imageShape.isImage());

 // This output document will display the image that was missing.
 doc.save(getArtifactsDir() + "HtmlLoadOptions.BaseUri.docx");
 
```

**Returns:**
int - İlgili  int  değeri. Döndürülen değer [LoadFormat](../../com.aspose.words/loadformat/) sabitlerinden biridir.
### getMswVersion() {#getMswVersion}
```
public int getMswVersion()
```


Belge yükleme sürecinin belirli bir MS Word sürümüyle eşleşmesini belirtmeye izin verir. Varsayılan değer [MsWordVersion.WORD\_2019](../../com.aspose.words/mswordversion/\#WORD-2019) dır.

 **Remarks:** 

Farklı Word sürümleri, yükleme sürecinde belge içeriği ve biçimlendirmesinin belirli yönlerini biraz farklı şekilde işleyebilir; bu da Belge Nesne Modeli'nde küçük farklılıklara yol açabilir.

 **Examples:** 

Belge yükleme sırasında belirli bir Microsoft Word sürümünün yükleme prosedürünü taklit etmeyi gösterir.

```

 // By default, Aspose.Words load documents according to Microsoft Word 2019 specification.
 LoadOptions loadOptions = new LoadOptions();

 Assert.assertEquals(MsWordVersion.WORD_2019, loadOptions.getMswVersion());

 // This document is missing the default paragraph formatting style.
 // This default style will be regenerated when we load the document either with Microsoft Word or Aspose.Words.
 loadOptions.setMswVersion(MsWordVersion.WORD_2007);
 Document doc = new Document(getMyDir() + "Document.docx", loadOptions);

 // The style's line spacing will have this value when loaded by Microsoft Word 2007 specification.
 Assert.assertEquals(12.95d, doc.getStyles().getDefaultParagraphFormat().getLineSpacing(), 0.01d);
 
```

**Returns:**
int - İlgili  int  değeri. Döndürülen değer [MsWordVersion](../../com.aspose.words/mswordversion/) sabitlerinden biridir.
### getPassword() {#getPassword}
```
public String getPassword()
```


Şifreli bir belgeyi açmak için şifreyi alır.  null  veya boş dize olabilir. Varsayılan değer  null  dır.

 **Remarks:** 

Şifreli bir belgeyi açmak için şifreyi bilmeniz gerekir. Belge şifreli değilse, bunu  null  veya boş dizeye ayarlayın.

 **Examples:** 

Şifreli belge dosyasını imzalamayı gösterir.

```

 // Create an X.509 certificate from a PKCS#12 store, which should contain a private key.
 CertificateHolder certificateHolder = CertificateHolder.create(getMyDir() + "morzal.pfx", "aw");

 // Create a comment, date, and decryption password which will be applied with our new digital signature.
 SignOptions signOptions = new SignOptions();
 {
     signOptions.setComments("Comment");
     signOptions.setSignTime(new Date());
     signOptions.setDecryptionPassword("docPassword");
 }

 // Set a local system filename for the unsigned input document, and an output filename for its new digitally signed copy.
 String inputFileName = getMyDir() + "Encrypted.docx";
 String outputFileName = getArtifactsDir() + "DigitalSignatureUtil.DecryptionPassword.docx";

 DigitalSignatureUtil.sign(inputFileName, outputFileName, certificateHolder, signOptions);
 
```

**Returns:**
java.lang.String - Şifreli bir belgeyi açmak için şifre.
### getPreserveIncludePictureField() {#getPreserveIncludePictureField}
```
public boolean getPreserveIncludePictureField()
```


Microsoft Word formatları okunurken INCLUDEPICTURE alanının korunup korunmayacağını alır. Varsayılan değer false.

 **Remarks:** 

Varsayılan olarak, INCLUDEPICTURE alanı bir şekil nesnesine dönüştürülür. Alanın korunması gerektiğinde, örneğin programlı olarak güncellemek istediğinizde, bunu geçersiz kılabilirsiniz. Ancak bu yaklaşım Aspose.Words için yaygın değildir. Kendi sorumluluğunuzda kullanın.

Olası kullanım senaryolarından biri, resmin kaynak yolunu dinamik olarak değiştirmek için MERGEFIELD'i bir alt alan olarak kullanmaktır. Bu durumda modelde INCLUDEPICTURE'ın korunması gerekir.

 **Examples:** 

Bir belge yüklenirken INCLUDEPICTURE alanlarını korumanın veya atmanın nasıl yapılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 FieldIncludePicture includePicture = (FieldIncludePicture) builder.insertField(FieldType.FIELD_INCLUDE_PICTURE, true);
 includePicture.setSourceFullName(getImageDir() + "Transparent background logo.png");
 includePicture.update(true);

 try (ByteArrayOutputStream docStream = new ByteArrayOutputStream()) {
     doc.save(docStream, new OoxmlSaveOptions(SaveFormat.DOCX));

     // We can set a flag in a LoadOptions object to decide whether to convert all INCLUDEPICTURE fields
     // into image shapes when loading a document that contains them.
     LoadOptions loadOptions = new LoadOptions();
     {
         loadOptions.setPreserveIncludePictureField(preserveIncludePictureField);
     }

     doc = new Document(new ByteArrayInputStream(docStream.toByteArray()), loadOptions);
     FieldCollection fieldCollection = doc.getRange().getFields();

     if (preserveIncludePictureField) {
         Assert.assertTrue(IterableUtils.matchesAny(fieldCollection, f -> f.getType() == FieldType.FIELD_INCLUDE_PICTURE));

         doc.updateFields();
         doc.save(getArtifactsDir() + "Field.PreserveIncludePicture.docx");
     } else {
         Assert.assertFalse(IterableUtils.matchesAny(fieldCollection, f -> f.getType() == FieldType.FIELD_INCLUDE_PICTURE));
     }
 }
 
```

**Returns:**
boolean - Microsoft Word formatları okunurken INCLUDEPICTURE alanının korunup korunmayacağı.
### getProgressCallback() {#getProgressCallback}
```
public IDocumentLoadingCallback getProgressCallback()
```


Bir belge yüklenirken çağrılır ve yükleme ilerlemesiyle ilgili verileri kabul eder.

 **Remarks:** 

[LoadFormat.DOCX](../../com.aspose.words/loadformat/\#DOCX), [LoadFormat.FLAT\_OPC](../../com.aspose.words/loadformat/\#FLAT-OPC), [LoadFormat.DOCM](../../com.aspose.words/loadformat/\#DOCM), [LoadFormat.DOTM](../../com.aspose.words/loadformat/\#DOTM), [LoadFormat.DOTX](../../com.aspose.words/loadformat/\#DOTX), [LoadFormat.MARKDOWN](../../com.aspose.words/loadformat/\#MARKDOWN), [LoadFormat.RTF](../../com.aspose.words/loadformat/\#RTF), [LoadFormat.WORD\_ML](../../com.aspose.words/loadformat/\#WORD-ML), [LoadFormat.DOC](../../com.aspose.words/loadformat/\#DOC), [LoadFormat.DOT](../../com.aspose.words/loadformat/\#DOT), [LoadFormat.ODT](../../com.aspose.words/loadformat/\#ODT), [LoadFormat.OTT](../../com.aspose.words/loadformat/\#OTT) formats supported.

 **Examples:** 

Belge yüklemesinin beklenen süreden fazla sürmesi durumunda kullanıcıyı nasıl bilgilendireceğinizi gösterir.

```

 public void progressCallback() throws Exception
 {
     LoadingProgressCallback progressCallback = new LoadingProgressCallback();

     LoadOptions loadOptions = new LoadOptions(); { loadOptions.setProgressCallback(progressCallback); }

     try
     {
         new Document(getMyDir() + "Big document.docx", loadOptions);
     }
     catch (IllegalStateException exception)
     {
         System.out.println(exception.getMessage());
         // Handle loading duration issue.
     }
 }

 /// 
 /// Cancel a document loading after the "MaxDuration" seconds.
 /// 
 public static class LoadingProgressCallback implements IDocumentLoadingCallback
 {
     /// 
     /// Ctr.
     /// 
     public LoadingProgressCallback()
     {
         mLoadingStartedAt = new Date();
     }

     /// 
     /// Callback method which called during document loading.
     /// 
     /// Loading arguments.
     public void notify(DocumentLoadingArgs args)
     {
         Date canceledAt = new Date();
         long diff = canceledAt.getTime() - mLoadingStartedAt.getTime();
         long ellapsedSeconds = TimeUnit.MILLISECONDS.toSeconds(diff);

         if (ellapsedSeconds > MAX_DURATION)
             throw new IllegalStateException(MessageFormat.format("EstimatedProgress = {0}; CanceledAt = {1}", args.getEstimatedProgress(), canceledAt));
     }

     /// 
     /// Date and time when document loading is started.
     /// 
     private Date mLoadingStartedAt;

     /// 
     /// Maximum allowed duration in sec.
     /// 
     private static final double MAX_DURATION = 0.5;
 }
 
```

**Returns:**
[IDocumentLoadingCallback](../../com.aspose.words/idocumentloadingcallback/) - The corresponding [IDocumentLoadingCallback](../../com.aspose.words/idocumentloadingcallback/) value.
### getRecoveryMode() {#getRecoveryMode}
```
public int getRecoveryMode()
```


Belge yüklenirken hatalar oluşursa belgenin nasıl işleneceğini tanımlar. Sisteminin belgeyi kurtarmaya çalışıp çalışmayacağını veya başka bir tanımlı davranışı izleyeceğini belirtmek için bu özelliği kullanın. Varsayılan değer [DocumentRecoveryMode.TRY\_RECOVER](../../com.aspose.words/documentrecoverymode/\#TRY-RECOVER).

 **Examples:** 

Yükleme sırasında hatalar oluştuysa bir belgeyi kurtarmaya nasıl çalışılacağını gösterir.

```

 LoadOptions loadOptions = new LoadOptions();
 loadOptions.setRecoveryMode(DocumentRecoveryMode.TRY_RECOVER);

 Document doc = new Document(getMyDir() + "Corrupted footnotes.docx", loadOptions);
 
```

**Returns:**
int - İlgili int değeri. Döndürülen değer [DocumentRecoveryMode](../../com.aspose.words/documentrecoverymode/) sabitlerinden biridir.
### getResourceLoadingCallback() {#getResourceLoadingCallback}
```
public IResourceLoadingCallback getResourceLoadingCallback()
```


Bir belge HTML veya MHTML'den içe aktarıldığında dış kaynakların (görüntüler, stil sayfaları) nasıl yükleneceğini kontrol etmeye izin verir.

 **Examples:** 

Html belgeleri yüklenirken dış kaynakların nasıl ele alınacağını gösterir.

```

 public void loadOptionsCallback() throws Exception {
     LoadOptions loadOptions = new LoadOptions();
     loadOptions.setResourceLoadingCallback(new HtmlLinkedResourceLoadingCallback());

     // When we load the document, our callback will handle linked resources such as CSS stylesheets and images.
     Document doc = new Document(getMyDir() + "Images.html", loadOptions);
     doc.save(getArtifactsDir() + "LoadOptions.LoadOptionsCallback.pdf");
 }

 /// 
 /// Prints the filenames of all external stylesheets and substitutes all images of a loaded html document.
 /// 
 private static class HtmlLinkedResourceLoadingCallback implements IResourceLoadingCallback {
     public int resourceLoading(ResourceLoadingArgs args) throws IOException {
         switch (args.getResourceType()) {
             case ResourceType.CSS_STYLE_SHEET:
                 System.out.println(MessageFormat.format("External CSS Stylesheet found upon loading: {0}", args.getOriginalUri()));
                 return ResourceLoadingAction.DEFAULT;
             case ResourceType.IMAGE:
                 System.out.println(MessageFormat.format("External Image found upon loading: {0}", args.getOriginalUri()));

                 final String newImageFilename = "Logo.jpg";
                 System.out.println(MessageFormat.format("\tImage will be substituted with: {0}", newImageFilename));

                 byte[] imageBytes = FileUtils.readFileToByteArray(new File(getImageDir() + newImageFilename));
                 args.setData(imageBytes);

                 return ResourceLoadingAction.USER_PROVIDED;
         }

         return ResourceLoadingAction.DEFAULT;
     }
 }
 
```

**Returns:**
[IResourceLoadingCallback](../../com.aspose.words/iresourceloadingcallback/) - The corresponding [IResourceLoadingCallback](../../com.aspose.words/iresourceloadingcallback/) value.
### getTempFolder() {#getTempFolder}
```
public String getTempFolder()
```


Belge okunurken geçici dosyaların kullanılmasına izin verir. Varsayılan olarak bu özellik null'dur ve geçici dosya kullanılmaz.

 **Remarks:** 

Klasör mevcut olmalı ve yazılabilir olmalıdır, aksi takdirde bir istisna fırlatılır.

Aspose.Words, okuma tamamlandığında tüm geçici dosyaları otomatik olarak siler.

 **Examples:** 

Geçici dosyalar kullanarak bir belgeyi nasıl yükleyeceğinizi gösterir.

```

 // Note that such an approach can reduce memory usage but degrades speed.
 LoadOptions loadOptions = new LoadOptions();
 loadOptions.setTempFolder("C:\\TempFolder\\");

 // Ensure that the directory exists and load.
 new File(loadOptions.getTempFolder()).mkdir();

 Document doc = new Document(getMyDir() + "Document.docx", loadOptions);
 
```

Bir belgeyi yüklerken belleğin yerine sabit sürücüyü nasıl kullanacağınızı gösterir.

```

 // When we load a document, various elements are temporarily stored in memory as the save operation occurs.
 // We can use this option to use a temporary folder in the local file system instead,
 // which will reduce our application's memory overhead.
 LoadOptions options = new LoadOptions();
 options.setTempFolder(getArtifactsDir() + "TempFiles");

 // The specified temporary folder must exist in the local file system before the load operation.
 Files.createDirectory(Paths.get(options.getTempFolder()));

 Document doc = new Document(getMyDir() + "Document.docx", options);

 // The folder will persist with no residual contents from the load operation.
 Assert.assertTrue(DocumentHelper.directoryGetFiles(options.getTempFolder(), "*.*").size() == 0);
 
```

**Returns:**
java.lang.String - İlgili java.lang.String değeri.
### getTrailingSpacesOptions() {#getTrailingSpacesOptions}
```
public int getTrailingSpacesOptions()
```


Son boşluk işleme için tercih edilen seçeneği alır. Varsayılan değer [TxtTrailingSpacesOptions.TRIM](../../com.aspose.words/txttrailingspacesoptions/\#TRIM) dir.

 **Examples:** 

Düz metin belgeleri yüklenirken boşlukların nasıl kırpılacağını gösterir.

```

 String textDoc = "      Line 1 \n" +
         "    Line 2   \n" +
         " Line 3       ";

 // Create a "TxtLoadOptions" object, which we can pass to a document's constructor
 // to modify how we load a plaintext document.
 TxtLoadOptions loadOptions = new TxtLoadOptions();

 // Set the "LeadingSpacesOptions" property to "TxtLeadingSpacesOptions.Preserve"
 // to preserve all whitespace characters at the start of every line.
 // Set the "LeadingSpacesOptions" property to "TxtLeadingSpacesOptions.ConvertToIndent"
 // to remove all whitespace characters from the start of every line,
 // and then apply a left first line indent to the paragraph to simulate the effect of the whitespaces.
 // Set the "LeadingSpacesOptions" property to "TxtLeadingSpacesOptions.Trim"
 // to remove all whitespace characters from every line's start.
 loadOptions.setLeadingSpacesOptions(txtLeadingSpacesOptions);

 // Set the "TrailingSpacesOptions" property to "TxtTrailingSpacesOptions.Preserve"
 // to preserve all whitespace characters at the end of every line.
 // Set the "TrailingSpacesOptions" property to "TxtTrailingSpacesOptions.Trim" to
 // remove all whitespace characters from the end of every line.
 loadOptions.setTrailingSpacesOptions(txtTrailingSpacesOptions);

 Document doc = new Document(new ByteArrayInputStream(textDoc.getBytes()), loadOptions);
 ParagraphCollection paragraphs = doc.getFirstSection().getBody().getParagraphs();

 switch (txtLeadingSpacesOptions) {
     case TxtLeadingSpacesOptions.CONVERT_TO_INDENT:
         Assert.assertEquals(37.8d, paragraphs.get(0).getParagraphFormat().getFirstLineIndent());
         Assert.assertEquals(25.2d, paragraphs.get(1).getParagraphFormat().getFirstLineIndent());
         Assert.assertEquals(6.3d, paragraphs.get(2).getParagraphFormat().getFirstLineIndent());

         Assert.assertTrue(paragraphs.get(0).getText().startsWith("Line 1"));
         Assert.assertTrue(paragraphs.get(1).getText().startsWith("Line 2"));
         Assert.assertTrue(paragraphs.get(2).getText().startsWith("Line 3"));
         break;
     case TxtLeadingSpacesOptions.PRESERVE:
         Assert.assertTrue(IterableUtils.matchesAll(paragraphs, s -> s.getParagraphFormat().getFirstLineIndent() == 0.0d));

         Assert.assertTrue(paragraphs.get(0).getText().startsWith("      Line 1"));
         Assert.assertTrue(paragraphs.get(1).getText().startsWith("    Line 2"));
         Assert.assertTrue(paragraphs.get(2).getText().startsWith(" Line 3"));
         break;
     case TxtLeadingSpacesOptions.TRIM:
         Assert.assertTrue(IterableUtils.matchesAll(paragraphs, s -> s.getParagraphFormat().getFirstLineIndent() == 0.0d));

         Assert.assertTrue(paragraphs.get(0).getText().startsWith("Line 1"));
         Assert.assertTrue(paragraphs.get(1).getText().startsWith("Line 2"));
         Assert.assertTrue(paragraphs.get(2).getText().startsWith("Line 3"));
         break;
 }

 switch (txtTrailingSpacesOptions) {
     case TxtTrailingSpacesOptions.PRESERVE:
         Assert.assertTrue(paragraphs.get(0).getText().endsWith("Line 1 \r"));
         Assert.assertTrue(paragraphs.get(1).getText().endsWith("Line 2   \r"));
         Assert.assertTrue(paragraphs.get(2).getText().endsWith("Line 3       \f"));
         break;
     case TxtTrailingSpacesOptions.TRIM:
         Assert.assertTrue(paragraphs.get(0).getText().endsWith("Line 1\r"));
         Assert.assertTrue(paragraphs.get(1).getText().endsWith("Line 2\r"));
         Assert.assertTrue(paragraphs.get(2).getText().endsWith("Line 3\f"));
         break;
 }
 
```

**Returns:**
int - Son boşluk işleme için tercih edilen seçenek. Döndürülen değer [TxtTrailingSpacesOptions](../../com.aspose.words/txttrailingspacesoptions/) sabitlerinden biridir.
### getUpdateDirtyFields() {#getUpdateDirtyFields}
```
public boolean getUpdateDirtyFields()
```


Alanları  dirty  özniteliğiyle güncelleyip güncellemeyeceğini belirtir.

 **Examples:** 

Alan sonucunu güncellemek için özel özelliğin nasıl kullanılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Give the document's built-in "Author" property value, and then display it with a field.
 doc.getBuiltInDocumentProperties().setAuthor("John Doe");
 FieldAuthor field = (FieldAuthor) builder.insertField(FieldType.FIELD_AUTHOR, true);

 Assert.assertFalse(field.isDirty());
 Assert.assertEquals("John Doe", field.getResult());

 // Update the property. The field still displays the old value.
 doc.getBuiltInDocumentProperties().setAuthor("John & Jane Doe");

 Assert.assertEquals("John Doe", field.getResult());

 // Since the field's value is out of date, we can mark it as "dirty".
 // This value will stay out of date until we update the field manually with the Field.Update() method.
 field.isDirty(true);

 // If we save without calling an update method,
 // the field will keep displaying the out of date value in the output document.
 doc.save(getArtifactsDir() + "Filed.UpdateDirtyFields.docx");

 // The LoadOptions object has an option to update all fields
 // marked as "dirty" when loading the document.
 LoadOptions options = new LoadOptions();
 options.setUpdateDirtyFields(updateDirtyFields);

 doc = new Document(getArtifactsDir() + "Filed.UpdateDirtyFields.docx", options);

 Assert.assertEquals("John & Jane Doe", doc.getBuiltInDocumentProperties().getAuthor());

 field = (FieldAuthor) doc.getRange().getFields().get(0);

 // Updating dirty fields like this automatically set their "IsDirty" flag to false.
 if (updateDirtyFields) {
     Assert.assertEquals("John & Jane Doe", field.getResult());
     Assert.assertFalse(field.isDirty());
 } else {
     Assert.assertEquals("John Doe", field.getResult());
     Assert.assertTrue(field.isDirty());
 }
 
```

**Returns:**
boolean - İlgili  boolean  değeri.
### getUseSystemLcid() {#getUseSystemLcid}
```
public boolean getUseSystemLcid()
```


Sayfa ayarı varsayılan kenar boşluklarını belirlemek için Windows kayıt defterinden alınan LCID değerinin kullanılıp kullanılmayacağını alır.

 **Remarks:** 

true olarak ayarlanırsa, Windows kayıt defterinden LCID değerini alan MS Word davranışı taklit edilir.

Varsayılan değer  false  dır.

**Returns:**
boolean - Sayfa ayarı varsayılan kenar boşluklarını belirlemek için Windows kayıt defterinden alınan LCID değerinin kullanılıp kullanılmayacağı.
### getWarningCallback() {#getWarningCallback}
```
public IWarningCallback getWarningCallback()
```


Veri veya biçimlendirme doğruluğunun kaybolmasına neden olabilecek bir sorun tespit edildiğinde, yükleme işlemi sırasında çağrılır.

 **Examples:** 

Belge yüklemesi sırasında oluşan uyarıların nasıl yazdırılacağını ve saklanacağını gösterir.

```

 public void loadOptionsWarningCallback() throws Exception {
     // Create a new LoadOptions object and set its WarningCallback attribute
     // as an instance of our IWarningCallback implementation.
     LoadOptions loadOptions = new LoadOptions();
     loadOptions.setWarningCallback(new DocumentLoadingWarningCallback());

     // Our callback will print all warnings that come up during the load operation.
     Document doc = new Document(getMyDir() + "Document.docx", loadOptions);

     ArrayList warnings = ((DocumentLoadingWarningCallback)loadOptions.getWarningCallback()).getWarnings();
     Assert.assertEquals(2, warnings.size());
 }

 /// 
 /// IWarningCallback that prints warnings and their details as they arise during document loading.
 /// 
 private static class DocumentLoadingWarningCallback implements IWarningCallback {
     public void warning(WarningInfo info) {
         System.out.println(MessageFormat.format("Warning: {0}", info.getWarningType()));
         System.out.println(MessageFormat.format("\tSource: {0}", info.getSource()));
         System.out.println(MessageFormat.format("\tDescription: {0}", info.getDescription()));
         mWarnings.add(info);
     }

     public ArrayList getWarnings() {
         return mWarnings;
     }

     private final  ArrayList mWarnings = new ArrayList();
 }
 
```

**Returns:**
[IWarningCallback](../../com.aspose.words/iwarningcallback/) - The corresponding [IWarningCallback](../../com.aspose.words/iwarningcallback/) value.
### setAutoNumberingDetection(boolean value) {#setAutoNumberingDetection-boolean}
```
public void setAutoNumberingDetection(boolean value)
```


Bir belge yüklenirken otomatik numaralandırma algılamasının gerçekleştirileceğini belirten boolean değeri ayarlar. Varsayılan değer true'tur.

 **Examples:** 

Otomatik numaralandırma algılamasını devre dışı bırakmanın nasıl yapılacağını gösterir.

```

 TxtLoadOptions options = new TxtLoadOptions(); { options.setAutoNumberingDetection(false); }
 Document doc = new Document(getMyDir() + "Number detection.txt", options);
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | Bir belge yüklenirken otomatik numaralandırma algılamasının gerçekleştirileceğini belirten boolean değer. |

### setBaseUri(String value) {#setBaseUri-java.lang.String}
```
public void setBaseUri(String value)
```


Gerekli olduğunda belgede bulunan göreli URI'leri mutlak URI'lere dönüştürmek için kullanılacak dizeyi ayarlar. null veya boş dize olabilir. Varsayılan değer null.

 **Remarks:** 

Bu özellik, göreli URI'leri mutlak URI'lere dönüştürmek için aşağıdaki durumlarda kullanılır:

1.  Bir akıştan HTML belgesi yüklenirken ve belge göreli URI'li görseller içerdiğinde ve BASE HTML öğesinde bir temel URI belirtilmemişse.
2.  Bir belge PDF ve diğer formatlara kaydedilirken, göreli URI'ler kullanılarak bağlanan görselleri alarak bu görsellerin çıktı belgesine kaydedilmesini sağlamak için.

 **Examples:** 

Bir akıştan temel URI kullanarak görseller içeren bir HTML belgesinin nasıl açılacağını gösterir.

```

 InputStream stream = new FileInputStream(getMyDir() + "Document.html");
 try  {
     // Pass the URI of the base folder while loading it
     // so that any images with relative URIs in the HTML document can be found.
     LoadOptions loadOptions = new LoadOptions();
     loadOptions.setBaseUri(getImageDir());

     Document doc = new Document(stream, loadOptions);

     // Verify that the first shape of the document contains a valid image.
     Shape shape = (Shape) doc.getChild(NodeType.SHAPE, 0, true);

     Assert.assertTrue(shape.isImage());
     Assert.assertNotNull(shape.getImageData().getImageBytes());
     Assert.assertEquals(32.0, ConvertUtil.pointToPixel(shape.getWidth()), 0.01);
     Assert.assertEquals(32.0, ConvertUtil.pointToPixel(shape.getHeight()), 0.01);
 } finally {
     if (stream != null) stream.close();
 }
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | Gerekli olduğunda belgede bulunan göreceli URI'ları mutlak URI'lara çözmek için kullanılacak dize. |

### setConvertMetafilesToPng(boolean value) {#setConvertMetafilesToPng-boolean}
```
public void setConvertMetafilesToPng(boolean value)
```


Metafile ( **F:Aspose.FileFormat.Wmf** veya **F:Aspose.FileFormat.Emf**) görüntülerinin **F:Aspose.FileFormat.Png** görüntü formatına dönüştürülüp dönüştürülmeyeceğini ayarlar.

 **Remarks:** 

Metafile'lar ( **F:Aspose.FileFormat.Wmf** veya **F:Aspose.FileFormat.Emf**) sıkıştırılmamış bir görüntü formatıdır ve bazen belgeyi tutmak ve işlemek için çok fazla RAM gerektirir. Bu seçenek, belge yüklenirken tüm metafile görüntülerini **F:Aspose.FileFormat.Png**'ye dönüştürmeye olanak tanır. Lütfen unutmayın - vektör grafikleri rastere dönüştürmek görüntü kalitesini düşürür.

 **Examples:** 

Belge yüklenirken WMF/EMF'nin PNG'ye nasıl dönüştürüleceğini gösterir.

```

 Document doc = new Document();

 Shape shape = new Shape(doc, ShapeType.IMAGE);
 shape.getImageData().setImage(getImageDir() + "Windows MetaFile.wmf");
 shape.setWidth(100.0);
 shape.setHeight(100.0);

 doc.getFirstSection().getBody().getFirstParagraph().appendChild(shape);

 doc.save(getArtifactsDir() + "Image.CreateImageDirectly.docx");

 shape = (Shape) doc.getChild(NodeType.SHAPE, 0, true);

 TestUtil.verifyImageInShape(1600, 1600, ImageType.WMF, shape);

 LoadOptions loadOptions = new LoadOptions();
 loadOptions.setConvertMetafilesToPng(true);

 doc = new Document(getArtifactsDir() + "Image.CreateImageDirectly.docx", loadOptions);
 shape = (Shape) doc.getChild(NodeType.SHAPE, 0, true);

 TestUtil.verifyImageInShape(1600, 1600, ImageType.PNG, shape);
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | Metafile (**F:Aspose.FileFormat.Wmf** veya **F:Aspose.FileFormat.Emf**) görüntülerini **F:Aspose.FileFormat.Png** görüntü formatına dönüştürüp dönüştürmeyeceği. |

### setConvertShapeToOfficeMath(boolean value) {#setConvertShapeToOfficeMath-boolean}
```
public void setConvertShapeToOfficeMath(boolean value)
```


EquationXML içeren şekillerin Office Math nesnelerine dönüştürülüp dönüştürülmeyeceğini ayarlar.

 **Examples:** 

EquationXML şekillerinin Office Math nesnelerine nasıl dönüştürüleceğini gösterir.

```

 LoadOptions loadOptions = new LoadOptions();

 // Use this flag to specify whether to convert the shapes with EquationXML attributes
 // to Office Math objects and then load the document.
 loadOptions.setConvertShapeToOfficeMath(isConvertShapeToOfficeMath);

 Document doc = new Document(getMyDir() + "Math shapes.docx", loadOptions);

 if (isConvertShapeToOfficeMath) {
     Assert.assertEquals(16, doc.getChildNodes(NodeType.SHAPE, true).getCount());
     Assert.assertEquals(34, doc.getChildNodes(NodeType.OFFICE_MATH, true).getCount());
 } else {
     Assert.assertEquals(24, doc.getChildNodes(NodeType.SHAPE, true).getCount());
     Assert.assertEquals(0, doc.getChildNodes(NodeType.OFFICE_MATH, true).getCount());
 }
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | EquationXML içeren şekilleri Office Math nesnelerine dönüştürüp dönüştürmeyeceği. |

### setDetectHyperlinks(boolean value) {#setDetectHyperlinks-boolean}
```
public void setDetectHyperlinks(boolean value)
```


Metinde hiperlinklerin algılanıp algılanmayacağını belirtir. Varsayılan değer false'tur.

 **Examples:** 

Köprüleri okuma ve görüntüleme yöntemini gösterir.

```

 final String INPUT_TEXT = "Some links in TXT:\n" +
         "https://www.aspose.com/\n" +
         "https://docs.aspose.com/words/net/\n";

 try (ByteArrayInputStream stream = new ByteArrayInputStream(INPUT_TEXT.getBytes(StandardCharsets.US_ASCII)))
 {
     // Load document with hyperlinks.
     TxtLoadOptions loadOptions = new TxtLoadOptions();
     loadOptions.setDetectHyperlinks(true);
     Document doc = new Document(stream, loadOptions);

     // Print hyperlinks text.
     for (Field field : doc.getRange().getFields())
         System.out.println(field.getResult());

     Assert.assertEquals(doc.getRange().getFields().get(0).getResult().trim(), "https://www.aspose.com/");
     Assert.assertEquals(doc.getRange().getFields().get(1).getResult().trim(), "https://docs.aspose.com/words/net/");
 }
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### setDetectNumberingWithWhitespaces(boolean value) {#setDetectNumberingWithWhitespaces-boolean}
```
public void setDetectNumberingWithWhitespaces(boolean value)
```


Belge düz metin formatından içe aktarıldığında numaralı liste öğelerinin nasıl tanınacağını belirtmeye olanak tanır. Varsayılan değer true'tur.

 **Remarks:** 

Bu seçenek false olarak ayarlanırsa, liste tanıma algoritması, liste numaraları nokta, sağ köşeli parantez veya madde işareti (örneğin "\\u2022", "*", "-" veya "o") ile bittiğinde liste paragraflarını algılar.

Bu seçenek true olarak ayarlanırsa, boşluk karakterleri de liste numarası ayırıcıları olarak kullanılır: Arapça stil numaralandırma (1., 1.1.2.) için liste tanıma algoritması hem boşlukları hem de nokta (".") sembollerini kullanır.

 **Examples:** 

Düz metin belgeleri yüklenirken listelerin nasıl algılanacağını gösterir.

```

 // Create a plaintext document in a string with four separate parts that we may interpret as lists,
 // with different delimiters. Upon loading the plaintext document into a "Document" object,
 // Aspose.Words will always detect the first three lists and will add a "List" object
 // for each to the document's "Lists" property.
 final String TEXT_DOC = "Full stop delimiters:\n" +
         "1. First list item 1\n" +
         "2. First list item 2\n" +
         "3. First list item 3\n\n" +
         "Right bracket delimiters:\n" +
         "1) Second list item 1\n" +
         "2) Second list item 2\n" +
         "3) Second list item 3\n\n" +
         "Bullet delimiters:\n" +
         "\u2022 Third list item 1\n" +
         "\u2022 Third list item 2\n" +
         "\u2022 Third list item 3\n\n" +
         "Whitespace delimiters:\n" +
         "1 Fourth list item 1\n" +
         "2 Fourth list item 2\n" +
         "3 Fourth list item 3";

 // Create a "TxtLoadOptions" object, which we can pass to a document's constructor
 // to modify how we load a plaintext document.
 TxtLoadOptions loadOptions = new TxtLoadOptions();

 // Set the "DetectNumberingWithWhitespaces" property to "true" to detect numbered items
 // with whitespace delimiters, such as the fourth list in our document, as lists.
 // This may also falsely detect paragraphs that begin with numbers as lists.
 // Set the "DetectNumberingWithWhitespaces" property to "false"
 // to not create lists from numbered items with whitespace delimiters.
 loadOptions.setDetectNumberingWithWhitespaces(detectNumberingWithWhitespaces);

 Document doc = new Document(new ByteArrayInputStream(TEXT_DOC.getBytes()), loadOptions);

 List paragraphList = Arrays.stream(doc.getFirstSection().getBody().getParagraphs().toArray())
         .filter(Paragraph.class::isInstance)
         .map(Paragraph.class::cast)
         .collect(Collectors.toList());

 if (detectNumberingWithWhitespaces) {
     Assert.assertEquals(4, doc.getLists().getCount());
     Assert.assertTrue(IterableUtils.matchesAny(paragraphList, s -> s.getText().contains("Fourth list") && s.isListItem()));
 } else {
     Assert.assertEquals(3, doc.getLists().getCount());
     Assert.assertFalse(IterableUtils.matchesAny(paragraphList, s -> s.getText().contains("Fourth list") && s.isListItem()));
 }
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### setDocumentDirection(int value) {#setDocumentDirection-int}
```
public void setDocumentDirection(int value)
```


Bir belge yönünü ayarlar. Varsayılan değer [DocumentDirection.LEFT\_TO\_RIGHT](../../com.aspose.words/documentdirection/\#LEFT-TO-RIGHT) dir.

 **Examples:** 

Düz metin belge metin yönünün nasıl algılanacağını gösterir.

```

 // Create a "TxtLoadOptions" object, which we can pass to a document's constructor
 // to modify how we load a plaintext document.
 TxtLoadOptions loadOptions = new TxtLoadOptions();

 // Set the "DocumentDirection" property to "DocumentDirection.Auto" automatically detects
 // the direction of every paragraph of text that Aspose.Words loads from plaintext.
 // Each paragraph's "Bidi" property will store its direction.
 loadOptions.setDocumentDirection(DocumentDirection.AUTO);

 // Detect Hebrew text as right-to-left.
 Document doc = new Document(getMyDir() + "Hebrew text.txt", loadOptions);

 Assert.assertTrue(doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat().getBidi());

 // Detect English text as right-to-left.
 doc = new Document(getMyDir() + "English text.txt", loadOptions);

 Assert.assertFalse(doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat().getBidi());
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | int | Bir belge yönü. Değer [DocumentDirection](../../com.aspose.words/documentdirection/) sabitlerinden biri olmalıdır. |

### setEncoding(Charset value) {#setEncoding-java.nio.charset.Charset}
```
public void setEncoding(Charset value)
```


Belge içinde kodlama belirtilmemişse bir HTML, TXT veya CHM belgesini yüklemek için kullanılacak kodlamayı ayarlar.  null  olabilir. Varsayılan değer  null .

 **Remarks:** 

Bu özellik yalnızca HTML, TXT veya CHM belgeleri yüklenirken kullanılır.

Kodlama belge içinde belirtilmemişse ve bu özellik  null  ise, sistem kodlamayı otomatik olarak tespit etmeye çalışır.

 **Examples:** 

Bir belgeyi açmak için kullanılacak kodlamanın nasıl ayarlanacağını gösterir.

```

 LoadOptions loadOptions = new LoadOptions();
 {
     loadOptions.setEncoding(StandardCharsets.US_ASCII);
 }

 // Load the document while passing the LoadOptions object, then verify the document's contents.
 Document doc = new Document(getMyDir() + "English text.txt", loadOptions);

 Assert.assertTrue(doc.toString(SaveFormat.TEXT).contains("This is a sample text in English."));
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.nio.charset.Charset | Belge içinde kodlama belirtilmemişse bir HTML, TXT veya CHM belgesini yüklemek için kullanılacak kodlama. |

### setFontSettings(FontSettings value) {#setFontSettings-com.aspose.words.FontSettings}
```
public void setFontSettings(FontSettings value)
```


Belge yazı tipi ayarlarını belirtmeye izin verir.

 **Remarks:** 

Bazı formatlar yüklenirken Aspose.Words yazı tiplerini çözümlemek zorunda kalabilir. Örneğin, HTML belgeleri yüklenirken Aspose.Words yazı tiplerini çözerek font geri dönüşümünü gerçekleştirebilir.

null  olarak ayarlanırsa, varsayılan statik yazı tipi ayarları [FontSettings.getDefaultInstance()](../../com.aspose.words/fontsettings/\#getDefaultInstance) kullanılacaktır.

Varsayılan değer  null  dır.

 **Examples:** 

Yükleme sırasında yazı tipi ikamelerini nasıl belirleyeceğinizi gösterir.

```

 LoadOptions loadOptions = new LoadOptions();
 loadOptions.setFontSettings(new FontSettings());

 // Set a font substitution rule for a LoadOptions object.
 // If the document we are loading uses a font which we do not have,
 // this rule will substitute the unavailable font with one that does exist.
 // In this case, all uses of the "MissingFont" will convert to "Comic Sans MS".
 TableSubstitutionRule substitutionRule = loadOptions.getFontSettings().getSubstitutionSettings().getTableSubstitution();
 substitutionRule.addSubstitutes("MissingFont", "Comic Sans MS");

 Document doc = new Document(getMyDir() + "Missing font.html", loadOptions);

 // At this point such text will still be in "MissingFont".
 // Font substitution will take place when we render the document.
 Assert.assertEquals("MissingFont", doc.getFirstSection().getBody().getFirstParagraph().getRuns().get(0).getFont().getName());

 doc.save(getArtifactsDir() + "FontSettings.ResolveFontsBeforeLoadingDocument.pdf");
 
```

Bir belgeyi yüklerken yazı tipi ikame ayarlarını nasıl uygulayacağınızı gösterir.

```

 // Create a FontSettings object that will substitute the "Times New Roman" font
 // with the font "Arvo" from our "MyFonts" folder.
 FontSettings fontSettings = new FontSettings();
 fontSettings.setFontsFolder(getFontsDir(), false);
 fontSettings.getSubstitutionSettings().getTableSubstitution().addSubstitutes("Times New Roman", "Arvo");

 // Set that FontSettings object as a property of a newly created LoadOptions object.
 LoadOptions loadOptions = new LoadOptions();
 loadOptions.setFontSettings(fontSettings);

 // Load the document, then render it as a PDF with the font substitution.
 Document doc = new Document(getMyDir() + "Document.docx", loadOptions);

 doc.save(getArtifactsDir() + "LoadOptions.FontSettings.pdf");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | [FontSettings](../../com.aspose.words/fontsettings/) | İlgili [FontSettings](../../com.aspose.words/fontsettings/) değeri. |

### setIgnoreOleData(boolean value) {#setIgnoreOleData-boolean}
```
public void setIgnoreOleData(boolean value)
```


OLE verilerinin göz ardı edilip edilmeyeceğini belirtir.

 **Remarks:** 

OLE verisinin yok sayılması, hedef format OLE nesnelerini desteklemediğinde veri kaybı olmadan bellek tüketimini azaltabilir ve performansı artırabilir.

Varsayılan değer  false  dır.

 **Examples:** 

Yükleme sırasında OLE verisinin yok sayılmasını gösterir.

```

 // Ignoring OLE data may reduce memory consumption and increase performance
 // without data lost in a case when destination format does not support OLE objects.
 LoadOptions loadOptions = new LoadOptions();
 loadOptions.setIgnoreOleData(true);
 Document doc = new Document(getMyDir() + "OLE objects.docx", loadOptions);

 doc.save(getArtifactsDir() + "LoadOptions.IgnoreOleData.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### setLeadingSpacesOptions(int value) {#setLeadingSpacesOptions-int}
```
public void setLeadingSpacesOptions(int value)
```


Ön boşluk işleme için tercih edilen seçeneği ayarlar. Varsayılan değer [TxtLeadingSpacesOptions.CONVERT\_TO\_INDENT](../../com.aspose.words/txtleadingspacesoptions/\#CONVERT-TO-INDENT) dir.

 **Examples:** 

Düz metin belgeleri yüklenirken boşlukların nasıl kırpılacağını gösterir.

```

 String textDoc = "      Line 1 \n" +
         "    Line 2   \n" +
         " Line 3       ";

 // Create a "TxtLoadOptions" object, which we can pass to a document's constructor
 // to modify how we load a plaintext document.
 TxtLoadOptions loadOptions = new TxtLoadOptions();

 // Set the "LeadingSpacesOptions" property to "TxtLeadingSpacesOptions.Preserve"
 // to preserve all whitespace characters at the start of every line.
 // Set the "LeadingSpacesOptions" property to "TxtLeadingSpacesOptions.ConvertToIndent"
 // to remove all whitespace characters from the start of every line,
 // and then apply a left first line indent to the paragraph to simulate the effect of the whitespaces.
 // Set the "LeadingSpacesOptions" property to "TxtLeadingSpacesOptions.Trim"
 // to remove all whitespace characters from every line's start.
 loadOptions.setLeadingSpacesOptions(txtLeadingSpacesOptions);

 // Set the "TrailingSpacesOptions" property to "TxtTrailingSpacesOptions.Preserve"
 // to preserve all whitespace characters at the end of every line.
 // Set the "TrailingSpacesOptions" property to "TxtTrailingSpacesOptions.Trim" to
 // remove all whitespace characters from the end of every line.
 loadOptions.setTrailingSpacesOptions(txtTrailingSpacesOptions);

 Document doc = new Document(new ByteArrayInputStream(textDoc.getBytes()), loadOptions);
 ParagraphCollection paragraphs = doc.getFirstSection().getBody().getParagraphs();

 switch (txtLeadingSpacesOptions) {
     case TxtLeadingSpacesOptions.CONVERT_TO_INDENT:
         Assert.assertEquals(37.8d, paragraphs.get(0).getParagraphFormat().getFirstLineIndent());
         Assert.assertEquals(25.2d, paragraphs.get(1).getParagraphFormat().getFirstLineIndent());
         Assert.assertEquals(6.3d, paragraphs.get(2).getParagraphFormat().getFirstLineIndent());

         Assert.assertTrue(paragraphs.get(0).getText().startsWith("Line 1"));
         Assert.assertTrue(paragraphs.get(1).getText().startsWith("Line 2"));
         Assert.assertTrue(paragraphs.get(2).getText().startsWith("Line 3"));
         break;
     case TxtLeadingSpacesOptions.PRESERVE:
         Assert.assertTrue(IterableUtils.matchesAll(paragraphs, s -> s.getParagraphFormat().getFirstLineIndent() == 0.0d));

         Assert.assertTrue(paragraphs.get(0).getText().startsWith("      Line 1"));
         Assert.assertTrue(paragraphs.get(1).getText().startsWith("    Line 2"));
         Assert.assertTrue(paragraphs.get(2).getText().startsWith(" Line 3"));
         break;
     case TxtLeadingSpacesOptions.TRIM:
         Assert.assertTrue(IterableUtils.matchesAll(paragraphs, s -> s.getParagraphFormat().getFirstLineIndent() == 0.0d));

         Assert.assertTrue(paragraphs.get(0).getText().startsWith("Line 1"));
         Assert.assertTrue(paragraphs.get(1).getText().startsWith("Line 2"));
         Assert.assertTrue(paragraphs.get(2).getText().startsWith("Line 3"));
         break;
 }

 switch (txtTrailingSpacesOptions) {
     case TxtTrailingSpacesOptions.PRESERVE:
         Assert.assertTrue(paragraphs.get(0).getText().endsWith("Line 1 \r"));
         Assert.assertTrue(paragraphs.get(1).getText().endsWith("Line 2   \r"));
         Assert.assertTrue(paragraphs.get(2).getText().endsWith("Line 3       \f"));
         break;
     case TxtTrailingSpacesOptions.TRIM:
         Assert.assertTrue(paragraphs.get(0).getText().endsWith("Line 1\r"));
         Assert.assertTrue(paragraphs.get(1).getText().endsWith("Line 2\r"));
         Assert.assertTrue(paragraphs.get(2).getText().endsWith("Line 3\f"));
         break;
 }
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | int | Ön boşluk işleme için tercih edilen seçenek. Değer [TxtLeadingSpacesOptions](../../com.aspose.words/txtleadingspacesoptions/) sabitlerinden biri olmalıdır. |

### setLoadFormat(int value) {#setLoadFormat-int}
```
public void setLoadFormat(int value)
```


Yüklenecek belgenin formatını belirtir. Varsayılan değer [LoadFormat.AUTO](../../com.aspose.words/loadformat/\#AUTO) dır.

 **Remarks:** 

Dosya formatını otomatik olarak algılaması için [LoadFormat.AUTO](../../com.aspose.words/loadformat/\#AUTO) değerini belirtmeniz önerilir. Yüklemek üzere olduğunuz belgenin formatını biliyorsanız, formatı açıkça belirtebilir ve bu, formatın otomatik algılanmasıyla ilgili ek yükü azaltarak yükleme süresini biraz kısaltır. Açık bir yükleme formatı belirtir ve bu format yanlış çıkarsa, otomatik algılama devreye girer ve dosyayı yüklemek için ikinci bir deneme yapılır.

 **Examples:** 

HTML belgesi açarken temel bir URI nasıl belirtileceğini gösterir.

```

 // Suppose we want to load an .html document that contains an image linked by a relative URI
 // while the image is in a different location. In that case, we will need to resolve the relative URI into an absolute one.
 // We can provide a base URI using an HtmlLoadOptions object.
 HtmlLoadOptions loadOptions = new HtmlLoadOptions(LoadFormat.HTML, "", getImageDir());

 Assert.assertEquals(LoadFormat.HTML, loadOptions.getLoadFormat());

 Document doc = new Document(getMyDir() + "Missing image.html", loadOptions);

 // While the image was broken in the input .html, our custom base URI helped us repair the link.
 Shape imageShape = (Shape) doc.getChildNodes(NodeType.SHAPE, true).get(0);
 Assert.assertTrue(imageShape.isImage());

 // This output document will display the image that was missing.
 doc.save(getArtifactsDir() + "HtmlLoadOptions.BaseUri.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | int | İlgili  int  değeri. Değer, [LoadFormat](../../com.aspose.words/loadformat/) sabitlerinden biri olmalıdır. |

### setMswVersion(int value) {#setMswVersion-int}
```
public void setMswVersion(int value)
```


Belge yükleme sürecinin belirli bir MS Word sürümüyle eşleşmesini belirtmeye izin verir. Varsayılan değer [MsWordVersion.WORD\_2019](../../com.aspose.words/mswordversion/\#WORD-2019) dır.

 **Remarks:** 

Farklı Word sürümleri, yükleme sürecinde belge içeriği ve biçimlendirmesinin belirli yönlerini biraz farklı şekilde işleyebilir; bu da Belge Nesne Modeli'nde küçük farklılıklara yol açabilir.

 **Examples:** 

Belge yükleme sırasında belirli bir Microsoft Word sürümünün yükleme prosedürünü taklit etmeyi gösterir.

```

 // By default, Aspose.Words load documents according to Microsoft Word 2019 specification.
 LoadOptions loadOptions = new LoadOptions();

 Assert.assertEquals(MsWordVersion.WORD_2019, loadOptions.getMswVersion());

 // This document is missing the default paragraph formatting style.
 // This default style will be regenerated when we load the document either with Microsoft Word or Aspose.Words.
 loadOptions.setMswVersion(MsWordVersion.WORD_2007);
 Document doc = new Document(getMyDir() + "Document.docx", loadOptions);

 // The style's line spacing will have this value when loaded by Microsoft Word 2007 specification.
 Assert.assertEquals(12.95d, doc.getStyles().getDefaultParagraphFormat().getLineSpacing(), 0.01d);
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | int | İlgili  int  değeri. Değer, [MsWordVersion](../../com.aspose.words/mswordversion/) sabitlerinden biri olmalıdır. |

### setPassword(String value) {#setPassword-java.lang.String}
```
public void setPassword(String value)
```


Şifreli bir belgeyi açmak için şifreyi ayarlar.  null  veya boş dize olabilir. Varsayılan değer  null .

 **Remarks:** 

Şifreli bir belgeyi açmak için şifreyi bilmeniz gerekir. Belge şifreli değilse, bunu  null  veya boş dizeye ayarlayın.

 **Examples:** 

Şifreli belge dosyasını imzalamayı gösterir.

```

 // Create an X.509 certificate from a PKCS#12 store, which should contain a private key.
 CertificateHolder certificateHolder = CertificateHolder.create(getMyDir() + "morzal.pfx", "aw");

 // Create a comment, date, and decryption password which will be applied with our new digital signature.
 SignOptions signOptions = new SignOptions();
 {
     signOptions.setComments("Comment");
     signOptions.setSignTime(new Date());
     signOptions.setDecryptionPassword("docPassword");
 }

 // Set a local system filename for the unsigned input document, and an output filename for its new digitally signed copy.
 String inputFileName = getMyDir() + "Encrypted.docx";
 String outputFileName = getArtifactsDir() + "DigitalSignatureUtil.DecryptionPassword.docx";

 DigitalSignatureUtil.sign(inputFileName, outputFileName, certificateHolder, signOptions);
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | Şifreli bir belgeyi açmak için şifre. |

### setPreserveIncludePictureField(boolean value) {#setPreserveIncludePictureField-boolean}
```
public void setPreserveIncludePictureField(boolean value)
```


Microsoft Word formatlarını okurken INCLUDEPICTURE alanının korunup korunmayacağını ayarlar. Varsayılan değer  false .

 **Remarks:** 

Varsayılan olarak, INCLUDEPICTURE alanı bir şekil nesnesine dönüştürülür. Alanın korunması gerektiğinde, örneğin programlı olarak güncellemek istediğinizde, bunu geçersiz kılabilirsiniz. Ancak bu yaklaşım Aspose.Words için yaygın değildir. Kendi sorumluluğunuzda kullanın.

Olası kullanım senaryolarından biri, resmin kaynak yolunu dinamik olarak değiştirmek için MERGEFIELD'i bir alt alan olarak kullanmaktır. Bu durumda modelde INCLUDEPICTURE'ın korunması gerekir.

 **Examples:** 

Bir belge yüklenirken INCLUDEPICTURE alanlarını korumanın veya atmanın nasıl yapılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 FieldIncludePicture includePicture = (FieldIncludePicture) builder.insertField(FieldType.FIELD_INCLUDE_PICTURE, true);
 includePicture.setSourceFullName(getImageDir() + "Transparent background logo.png");
 includePicture.update(true);

 try (ByteArrayOutputStream docStream = new ByteArrayOutputStream()) {
     doc.save(docStream, new OoxmlSaveOptions(SaveFormat.DOCX));

     // We can set a flag in a LoadOptions object to decide whether to convert all INCLUDEPICTURE fields
     // into image shapes when loading a document that contains them.
     LoadOptions loadOptions = new LoadOptions();
     {
         loadOptions.setPreserveIncludePictureField(preserveIncludePictureField);
     }

     doc = new Document(new ByteArrayInputStream(docStream.toByteArray()), loadOptions);
     FieldCollection fieldCollection = doc.getRange().getFields();

     if (preserveIncludePictureField) {
         Assert.assertTrue(IterableUtils.matchesAny(fieldCollection, f -> f.getType() == FieldType.FIELD_INCLUDE_PICTURE));

         doc.updateFields();
         doc.save(getArtifactsDir() + "Field.PreserveIncludePicture.docx");
     } else {
         Assert.assertFalse(IterableUtils.matchesAny(fieldCollection, f -> f.getType() == FieldType.FIELD_INCLUDE_PICTURE));
     }
 }
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | Microsoft Word formatlarını okurken INCLUDEPICTURE alanının korunup korunmayacağı. |

### setProgressCallback(IDocumentLoadingCallback value) {#setProgressCallback-com.aspose.words.IDocumentLoadingCallback}
```
public void setProgressCallback(IDocumentLoadingCallback value)
```


Bir belge yüklenirken çağrılır ve yükleme ilerlemesiyle ilgili verileri kabul eder.

 **Remarks:** 

[LoadFormat.DOCX](../../com.aspose.words/loadformat/\#DOCX), [LoadFormat.FLAT\_OPC](../../com.aspose.words/loadformat/\#FLAT-OPC), [LoadFormat.DOCM](../../com.aspose.words/loadformat/\#DOCM), [LoadFormat.DOTM](../../com.aspose.words/loadformat/\#DOTM), [LoadFormat.DOTX](../../com.aspose.words/loadformat/\#DOTX), [LoadFormat.MARKDOWN](../../com.aspose.words/loadformat/\#MARKDOWN), [LoadFormat.RTF](../../com.aspose.words/loadformat/\#RTF), [LoadFormat.WORD\_ML](../../com.aspose.words/loadformat/\#WORD-ML), [LoadFormat.DOC](../../com.aspose.words/loadformat/\#DOC), [LoadFormat.DOT](../../com.aspose.words/loadformat/\#DOT), [LoadFormat.ODT](../../com.aspose.words/loadformat/\#ODT), [LoadFormat.OTT](../../com.aspose.words/loadformat/\#OTT) formats supported.

 **Examples:** 

Belge yüklemesinin beklenen süreden fazla sürmesi durumunda kullanıcıyı nasıl bilgilendireceğinizi gösterir.

```

 public void progressCallback() throws Exception
 {
     LoadingProgressCallback progressCallback = new LoadingProgressCallback();

     LoadOptions loadOptions = new LoadOptions(); { loadOptions.setProgressCallback(progressCallback); }

     try
     {
         new Document(getMyDir() + "Big document.docx", loadOptions);
     }
     catch (IllegalStateException exception)
     {
         System.out.println(exception.getMessage());
         // Handle loading duration issue.
     }
 }

 /// 
 /// Cancel a document loading after the "MaxDuration" seconds.
 /// 
 public static class LoadingProgressCallback implements IDocumentLoadingCallback
 {
     /// 
     /// Ctr.
     /// 
     public LoadingProgressCallback()
     {
         mLoadingStartedAt = new Date();
     }

     /// 
     /// Callback method which called during document loading.
     /// 
     /// Loading arguments.
     public void notify(DocumentLoadingArgs args)
     {
         Date canceledAt = new Date();
         long diff = canceledAt.getTime() - mLoadingStartedAt.getTime();
         long ellapsedSeconds = TimeUnit.MILLISECONDS.toSeconds(diff);

         if (ellapsedSeconds > MAX_DURATION)
             throw new IllegalStateException(MessageFormat.format("EstimatedProgress = {0}; CanceledAt = {1}", args.getEstimatedProgress(), canceledAt));
     }

     /// 
     /// Date and time when document loading is started.
     /// 
     private Date mLoadingStartedAt;

     /// 
     /// Maximum allowed duration in sec.
     /// 
     private static final double MAX_DURATION = 0.5;
 }
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | [IDocumentLoadingCallback](../../com.aspose.words/idocumentloadingcallback/) | İlgili [IDocumentLoadingCallback](../../com.aspose.words/idocumentloadingcallback/) değeri. |

### setRecoveryMode(int value) {#setRecoveryMode-int}
```
public void setRecoveryMode(int value)
```


Belge yüklenirken hatalar oluşursa belgenin nasıl işleneceğini tanımlar. Sisteminin belgeyi kurtarmaya çalışıp çalışmayacağını veya başka bir tanımlı davranışı izleyeceğini belirtmek için bu özelliği kullanın. Varsayılan değer [DocumentRecoveryMode.TRY\_RECOVER](../../com.aspose.words/documentrecoverymode/\#TRY-RECOVER).

 **Examples:** 

Yükleme sırasında hatalar oluştuysa bir belgeyi kurtarmaya nasıl çalışılacağını gösterir.

```

 LoadOptions loadOptions = new LoadOptions();
 loadOptions.setRecoveryMode(DocumentRecoveryMode.TRY_RECOVER);

 Document doc = new Document(getMyDir() + "Corrupted footnotes.docx", loadOptions);
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | int | İlgili  int  değeri. Değer, [DocumentRecoveryMode](../../com.aspose.words/documentrecoverymode/) sabitlerinden biri olmalıdır. |

### setResourceLoadingCallback(IResourceLoadingCallback value) {#setResourceLoadingCallback-com.aspose.words.IResourceLoadingCallback}
```
public void setResourceLoadingCallback(IResourceLoadingCallback value)
```


Bir belge HTML veya MHTML'den içe aktarıldığında dış kaynakların (görüntüler, stil sayfaları) nasıl yükleneceğini kontrol etmeye izin verir.

 **Examples:** 

Html belgeleri yüklenirken dış kaynakların nasıl ele alınacağını gösterir.

```

 public void loadOptionsCallback() throws Exception {
     LoadOptions loadOptions = new LoadOptions();
     loadOptions.setResourceLoadingCallback(new HtmlLinkedResourceLoadingCallback());

     // When we load the document, our callback will handle linked resources such as CSS stylesheets and images.
     Document doc = new Document(getMyDir() + "Images.html", loadOptions);
     doc.save(getArtifactsDir() + "LoadOptions.LoadOptionsCallback.pdf");
 }

 /// 
 /// Prints the filenames of all external stylesheets and substitutes all images of a loaded html document.
 /// 
 private static class HtmlLinkedResourceLoadingCallback implements IResourceLoadingCallback {
     public int resourceLoading(ResourceLoadingArgs args) throws IOException {
         switch (args.getResourceType()) {
             case ResourceType.CSS_STYLE_SHEET:
                 System.out.println(MessageFormat.format("External CSS Stylesheet found upon loading: {0}", args.getOriginalUri()));
                 return ResourceLoadingAction.DEFAULT;
             case ResourceType.IMAGE:
                 System.out.println(MessageFormat.format("External Image found upon loading: {0}", args.getOriginalUri()));

                 final String newImageFilename = "Logo.jpg";
                 System.out.println(MessageFormat.format("\tImage will be substituted with: {0}", newImageFilename));

                 byte[] imageBytes = FileUtils.readFileToByteArray(new File(getImageDir() + newImageFilename));
                 args.setData(imageBytes);

                 return ResourceLoadingAction.USER_PROVIDED;
         }

         return ResourceLoadingAction.DEFAULT;
     }
 }
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | [IResourceLoadingCallback](../../com.aspose.words/iresourceloadingcallback/) | İlgili [IResourceLoadingCallback](../../com.aspose.words/iresourceloadingcallback/) değeri. |

### setTempFolder(String value) {#setTempFolder-java.lang.String}
```
public void setTempFolder(String value)
```


Belge okunurken geçici dosyaların kullanılmasına izin verir. Varsayılan olarak bu özellik null'dur ve geçici dosya kullanılmaz.

 **Remarks:** 

Klasör mevcut olmalı ve yazılabilir olmalıdır, aksi takdirde bir istisna fırlatılır.

Aspose.Words, okuma tamamlandığında tüm geçici dosyaları otomatik olarak siler.

 **Examples:** 

Geçici dosyalar kullanarak bir belgeyi nasıl yükleyeceğinizi gösterir.

```

 // Note that such an approach can reduce memory usage but degrades speed.
 LoadOptions loadOptions = new LoadOptions();
 loadOptions.setTempFolder("C:\\TempFolder\\");

 // Ensure that the directory exists and load.
 new File(loadOptions.getTempFolder()).mkdir();

 Document doc = new Document(getMyDir() + "Document.docx", loadOptions);
 
```

Bir belgeyi yüklerken belleğin yerine sabit sürücüyü nasıl kullanacağınızı gösterir.

```

 // When we load a document, various elements are temporarily stored in memory as the save operation occurs.
 // We can use this option to use a temporary folder in the local file system instead,
 // which will reduce our application's memory overhead.
 LoadOptions options = new LoadOptions();
 options.setTempFolder(getArtifactsDir() + "TempFiles");

 // The specified temporary folder must exist in the local file system before the load operation.
 Files.createDirectory(Paths.get(options.getTempFolder()));

 Document doc = new Document(getMyDir() + "Document.docx", options);

 // The folder will persist with no residual contents from the load operation.
 Assert.assertTrue(DocumentHelper.directoryGetFiles(options.getTempFolder(), "*.*").size() == 0);
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | İlgili java.lang.String değeri. |

### setTrailingSpacesOptions(int value) {#setTrailingSpacesOptions-int}
```
public void setTrailingSpacesOptions(int value)
```


Son boşluk işleme için tercih edilen seçeneği ayarlar. Varsayılan değer [TxtTrailingSpacesOptions.TRIM](../../com.aspose.words/txttrailingspacesoptions/\#TRIM) dir.

 **Examples:** 

Düz metin belgeleri yüklenirken boşlukların nasıl kırpılacağını gösterir.

```

 String textDoc = "      Line 1 \n" +
         "    Line 2   \n" +
         " Line 3       ";

 // Create a "TxtLoadOptions" object, which we can pass to a document's constructor
 // to modify how we load a plaintext document.
 TxtLoadOptions loadOptions = new TxtLoadOptions();

 // Set the "LeadingSpacesOptions" property to "TxtLeadingSpacesOptions.Preserve"
 // to preserve all whitespace characters at the start of every line.
 // Set the "LeadingSpacesOptions" property to "TxtLeadingSpacesOptions.ConvertToIndent"
 // to remove all whitespace characters from the start of every line,
 // and then apply a left first line indent to the paragraph to simulate the effect of the whitespaces.
 // Set the "LeadingSpacesOptions" property to "TxtLeadingSpacesOptions.Trim"
 // to remove all whitespace characters from every line's start.
 loadOptions.setLeadingSpacesOptions(txtLeadingSpacesOptions);

 // Set the "TrailingSpacesOptions" property to "TxtTrailingSpacesOptions.Preserve"
 // to preserve all whitespace characters at the end of every line.
 // Set the "TrailingSpacesOptions" property to "TxtTrailingSpacesOptions.Trim" to
 // remove all whitespace characters from the end of every line.
 loadOptions.setTrailingSpacesOptions(txtTrailingSpacesOptions);

 Document doc = new Document(new ByteArrayInputStream(textDoc.getBytes()), loadOptions);
 ParagraphCollection paragraphs = doc.getFirstSection().getBody().getParagraphs();

 switch (txtLeadingSpacesOptions) {
     case TxtLeadingSpacesOptions.CONVERT_TO_INDENT:
         Assert.assertEquals(37.8d, paragraphs.get(0).getParagraphFormat().getFirstLineIndent());
         Assert.assertEquals(25.2d, paragraphs.get(1).getParagraphFormat().getFirstLineIndent());
         Assert.assertEquals(6.3d, paragraphs.get(2).getParagraphFormat().getFirstLineIndent());

         Assert.assertTrue(paragraphs.get(0).getText().startsWith("Line 1"));
         Assert.assertTrue(paragraphs.get(1).getText().startsWith("Line 2"));
         Assert.assertTrue(paragraphs.get(2).getText().startsWith("Line 3"));
         break;
     case TxtLeadingSpacesOptions.PRESERVE:
         Assert.assertTrue(IterableUtils.matchesAll(paragraphs, s -> s.getParagraphFormat().getFirstLineIndent() == 0.0d));

         Assert.assertTrue(paragraphs.get(0).getText().startsWith("      Line 1"));
         Assert.assertTrue(paragraphs.get(1).getText().startsWith("    Line 2"));
         Assert.assertTrue(paragraphs.get(2).getText().startsWith(" Line 3"));
         break;
     case TxtLeadingSpacesOptions.TRIM:
         Assert.assertTrue(IterableUtils.matchesAll(paragraphs, s -> s.getParagraphFormat().getFirstLineIndent() == 0.0d));

         Assert.assertTrue(paragraphs.get(0).getText().startsWith("Line 1"));
         Assert.assertTrue(paragraphs.get(1).getText().startsWith("Line 2"));
         Assert.assertTrue(paragraphs.get(2).getText().startsWith("Line 3"));
         break;
 }

 switch (txtTrailingSpacesOptions) {
     case TxtTrailingSpacesOptions.PRESERVE:
         Assert.assertTrue(paragraphs.get(0).getText().endsWith("Line 1 \r"));
         Assert.assertTrue(paragraphs.get(1).getText().endsWith("Line 2   \r"));
         Assert.assertTrue(paragraphs.get(2).getText().endsWith("Line 3       \f"));
         break;
     case TxtTrailingSpacesOptions.TRIM:
         Assert.assertTrue(paragraphs.get(0).getText().endsWith("Line 1\r"));
         Assert.assertTrue(paragraphs.get(1).getText().endsWith("Line 2\r"));
         Assert.assertTrue(paragraphs.get(2).getText().endsWith("Line 3\f"));
         break;
 }
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | int | Son boşluk işleme için tercih edilen seçenek. Değer [TxtTrailingSpacesOptions](../../com.aspose.words/txttrailingspacesoptions/) sabitlerinden biri olmalıdır. |

### setUpdateDirtyFields(boolean value) {#setUpdateDirtyFields-boolean}
```
public void setUpdateDirtyFields(boolean value)
```


Alanları  dirty  özniteliğiyle güncelleyip güncellemeyeceğini belirtir.

 **Examples:** 

Alan sonucunu güncellemek için özel özelliğin nasıl kullanılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Give the document's built-in "Author" property value, and then display it with a field.
 doc.getBuiltInDocumentProperties().setAuthor("John Doe");
 FieldAuthor field = (FieldAuthor) builder.insertField(FieldType.FIELD_AUTHOR, true);

 Assert.assertFalse(field.isDirty());
 Assert.assertEquals("John Doe", field.getResult());

 // Update the property. The field still displays the old value.
 doc.getBuiltInDocumentProperties().setAuthor("John & Jane Doe");

 Assert.assertEquals("John Doe", field.getResult());

 // Since the field's value is out of date, we can mark it as "dirty".
 // This value will stay out of date until we update the field manually with the Field.Update() method.
 field.isDirty(true);

 // If we save without calling an update method,
 // the field will keep displaying the out of date value in the output document.
 doc.save(getArtifactsDir() + "Filed.UpdateDirtyFields.docx");

 // The LoadOptions object has an option to update all fields
 // marked as "dirty" when loading the document.
 LoadOptions options = new LoadOptions();
 options.setUpdateDirtyFields(updateDirtyFields);

 doc = new Document(getArtifactsDir() + "Filed.UpdateDirtyFields.docx", options);

 Assert.assertEquals("John & Jane Doe", doc.getBuiltInDocumentProperties().getAuthor());

 field = (FieldAuthor) doc.getRange().getFields().get(0);

 // Updating dirty fields like this automatically set their "IsDirty" flag to false.
 if (updateDirtyFields) {
     Assert.assertEquals("John & Jane Doe", field.getResult());
     Assert.assertFalse(field.isDirty());
 } else {
     Assert.assertEquals("John Doe", field.getResult());
     Assert.assertTrue(field.isDirty());
 }
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### setUseSystemLcid(boolean value) {#setUseSystemLcid-boolean}
```
public void setUseSystemLcid(boolean value)
```


Sayfa ayarı varsayılan kenar boşluklarını belirlemek için Windows kayıt defterinden alınan LCID değerinin kullanılıp kullanılmayacağını ayarlar.

 **Remarks:** 

true olarak ayarlanırsa, Windows kayıt defterinden LCID değerini alan MS Word davranışı taklit edilir.

Varsayılan değer  false  dır.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | Sayfa ayarı varsayılan kenar boşluklarını belirlemek için Windows kayıt defterinden alınan LCID değerinin kullanılıp kullanılmayacağını. |

### setWarningCallback(IWarningCallback value) {#setWarningCallback-com.aspose.words.IWarningCallback}
```
public void setWarningCallback(IWarningCallback value)
```


Veri veya biçimlendirme doğruluğunun kaybolmasına neden olabilecek bir sorun tespit edildiğinde, yükleme işlemi sırasında çağrılır.

 **Examples:** 

Belge yüklemesi sırasında oluşan uyarıların nasıl yazdırılacağını ve saklanacağını gösterir.

```

 public void loadOptionsWarningCallback() throws Exception {
     // Create a new LoadOptions object and set its WarningCallback attribute
     // as an instance of our IWarningCallback implementation.
     LoadOptions loadOptions = new LoadOptions();
     loadOptions.setWarningCallback(new DocumentLoadingWarningCallback());

     // Our callback will print all warnings that come up during the load operation.
     Document doc = new Document(getMyDir() + "Document.docx", loadOptions);

     ArrayList warnings = ((DocumentLoadingWarningCallback)loadOptions.getWarningCallback()).getWarnings();
     Assert.assertEquals(2, warnings.size());
 }

 /// 
 /// IWarningCallback that prints warnings and their details as they arise during document loading.
 /// 
 private static class DocumentLoadingWarningCallback implements IWarningCallback {
     public void warning(WarningInfo info) {
         System.out.println(MessageFormat.format("Warning: {0}", info.getWarningType()));
         System.out.println(MessageFormat.format("\tSource: {0}", info.getSource()));
         System.out.println(MessageFormat.format("\tDescription: {0}", info.getDescription()));
         mWarnings.add(info);
     }

     public ArrayList getWarnings() {
         return mWarnings;
     }

     private final  ArrayList mWarnings = new ArrayList();
 }
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | [IWarningCallback](../../com.aspose.words/iwarningcallback/) | İlgili [IWarningCallback](../../com.aspose.words/iwarningcallback/) değeri. |

