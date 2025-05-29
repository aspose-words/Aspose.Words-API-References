---
title: Document.Save
linktitle: Save
articleTitle: Save
second_title: .NET için Aspose.Words
description: Akıllı kaydetme yöntemimizle belgelerinizi zahmetsizce kaydedin; sorunsuz depolama için dosya uzantısına göre doğru formatı otomatik olarak seçin.
type: docs
weight: 750
url: /tr/net/aspose.words/document/save/
---
## Save(*string*) {#save_2}

Belgeyi bir dosyaya kaydeder. Uzantıdan kaydetme biçimini otomatik olarak belirler.

```csharp
public SaveOutputParameters Save(string fileName)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| fileName | String | Belgenin adı. belirtilen dosya adına sahip bir belge zaten varsa, var olan belgenin üzerine yazılır. |

### Geri dönüş değeri

İsteğe bağlı olarak kullanabileceğiniz ek bilgiler.

## Örnekler

Bir belgenin nasıl açılacağını ve .PDF'e nasıl dönüştürüleceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Document.docx");

doc.Save(ArtifactsDir + "Document.ConvertToPdf.pdf");
```

PDF'in .docx'e nasıl dönüştürüleceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");

doc.Save(ArtifactsDir + "PDF2Word.ConvertPdfToDocx.pdf");

// Az önce kaydettiğimiz PDF belgesini yükleyelim ve .docx formatına dönüştürelim.
Document pdfDoc = new Document(ArtifactsDir + "PDF2Word.ConvertPdfToDocx.pdf");

pdfDoc.Save(ArtifactsDir + "PDF2Word.ConvertPdfToDocx.docx");
```

### Ayrıca bakınız

* class [SaveOutputParameters](../../../aspose.words.saving/saveoutputparameters/)
* class [Document](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)

---

## Save(*string, [SaveFormat](../../saveformat/)*) {#save_3}

Belgeyi belirtilen biçimde bir dosyaya kaydeder.

```csharp
public SaveOutputParameters Save(string fileName, SaveFormat saveFormat)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| fileName | String | Belgenin adı. belirtilen dosya adına sahip bir belge zaten varsa, var olan belgenin üzerine yazılır. |
| saveFormat | SaveFormat | Belgenin kaydedileceği biçim. |

### Geri dönüş değeri

İsteğe bağlı olarak kullanabileceğiniz ek bilgiler.

## Örnekler

DOCX'ten HTML formatına nasıl dönüştürüleceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Document.docx");

doc.Save(ArtifactsDir + "Document.ConvertToHtml.html", SaveFormat.Html);
```

### Ayrıca bakınız

* class [SaveOutputParameters](../../../aspose.words.saving/saveoutputparameters/)
* enum [SaveFormat](../../saveformat/)
* class [Document](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)

---

## Save(*string, [SaveOptions](../../../aspose.words.saving/saveoptions/)*) {#save_4}

Belirtilen kaydetme seçeneklerini kullanarak belgeyi bir dosyaya kaydeder.

```csharp
public SaveOutputParameters Save(string fileName, SaveOptions saveOptions)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| fileName | String | Belgenin adı. belirtilen dosya adına sahip bir belge zaten varsa, var olan belgenin üzerine yazılır. |
| saveOptions | SaveOptions | Belgenin nasıl kaydedileceğini kontrol eden seçenekleri belirtir.`hükümsüz`. |

### Geri dönüş değeri

İsteğe bağlı olarak kullanabileceğiniz ek bilgiler.

## Örnekler

SaveOptions ile işlenmiş bir belgenin kalitesinin nasıl iyileştirileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Size = 60;
builder.Writeln("Some text.");

SaveOptions options = new ImageSaveOptions(SaveFormat.Jpeg);
doc.Save(ArtifactsDir + "Document.ImageSaveOptions.Default.jpg", options);

options.UseAntiAliasing = true;
options.UseHighQualityRendering = true;

doc.Save(ArtifactsDir + "Document.ImageSaveOptions.HighQuality.jpg", options);
```

Bir PDF'in .docx formatına nasıl dönüştürüleceğini ve SaveOptions nesnesiyle kaydetme işleminin nasıl özelleştirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

doc.Save(ArtifactsDir + "PDF2Word.ConvertPdfToDocxCustom.pdf");

// Az önce kaydettiğimiz PDF belgesini yükleyelim ve .docx formatına dönüştürelim.
Document pdfDoc = new Document(ArtifactsDir + "PDF2Word.ConvertPdfToDocxCustom.pdf");

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(SaveFormat.Docx);

// Kaydedilen belgeyi bir parola ile şifrelemek için "Parola" özelliğini ayarlayın.
saveOptions.Password = "MyPassword";

pdfDoc.Save(ArtifactsDir + "PDF2Word.ConvertPdfToDocxCustom.docx", saveOptions);
```

Bir belgenin her sayfasının ayrı bir TIFF görüntüsüne nasıl dönüştürüleceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2.");
builder.InsertImage(ImageDir + "Logo.jpg");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 3.");

// Belgenin "Kaydet" metoduna geçirebileceğimiz bir "ImageSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi görüntüye dönüştürme şeklini değiştirmek için.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);

for (int i = 0; i < doc.PageCount; i++)
{
    // "PageSet" özelliğini ilk sayfanın numarasına ayarlayın
    // belgenin hangisinden oluşturulmaya başlanacağı.
    options.PageSet = new PageSet(i);
    // Sayfayı 2325x5325 piksel ve 600 dpi olarak dışa aktar.
    options.Resolution = 600;
    options.ImageSize = new Size(2325, 5325);

    doc.Save(ArtifactsDir + $"ImageSaveOptions.PageByPage.{i + 1}.tiff", options);
}
```

Bir belgenin bir sayfasının JPEG görüntüsüne nasıl dönüştürüleceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2.");
builder.InsertImage(ImageDir + "Logo.jpg");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 3.");

// Belgenin "Kaydet" metoduna geçirebileceğimiz bir "ImageSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi görüntüye dönüştürme şeklini değiştirmek için.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Jpeg);
// İkinci sayfayı seçmek için "PageSet"i "1" olarak ayarlayın
// belgenin oluşturulmaya başlanacağı sıfır tabanlı dizin.
options.PageSet = new PageSet(1);

// Belgeyi JPEG formatında kaydettiğimizde Aspose.Words yalnızca bir sayfa oluşturur.
// Bu resim ikinci sayfadan başlayarak tek bir sayfa içerecektir,
// bu sadece orijinal belgenin ikinci sayfası olacak.
doc.Save(ArtifactsDir + "ImageSaveOptions.OnePage.jpg", options);
```

Bir belgeyi JPEG olarak kaydederken sıkıştırmanın nasıl yapılandırılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertImage(ImageDir + "Logo.jpg");

// Belgenin "Kaydet" metoduna geçirebileceğimiz bir "ImageSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi görüntüye dönüştürme şeklini değiştirmek için.
ImageSaveOptions imageOptions = new ImageSaveOptions(SaveFormat.Jpeg);
// Belgeyi işlerken daha güçlü sıkıştırma kullanmak için "JpegQuality" özelliğini "10" olarak ayarlayın.
// Bu, belgenin dosya boyutunu küçültecektir, ancak görüntü daha belirgin sıkıştırma eserleri gösterecektir.
imageOptions.JpegQuality = 10;
doc.Save(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighCompression.jpg", imageOptions);

// Belgeyi işlerken daha zayıf sıkıştırma kullanmak için "JpegQuality" özelliğini "100" olarak ayarlayın.
// Bu, dosya boyutunun artması pahasına görüntünün kalitesini artıracaktır.
imageOptions.JpegQuality = 100;
doc.Save(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighQuality.jpg", imageOptions);
```

Belgenin tamamının üç düzeyde PDF'ye nasıl dönüştürüleceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 1'den 5'e kadar olan seviyelerin başlıklarını ekleyin.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;

Assert.True(builder.ParagraphFormat.IsHeading);

builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;

builder.Writeln("Heading 1.1");
builder.Writeln("Heading 1.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading3;

builder.Writeln("Heading 1.2.1");
builder.Writeln("Heading 1.2.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading4;

builder.Writeln("Heading 1.2.2.1");
builder.Writeln("Heading 1.2.2.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading5;

builder.Writeln("Heading 1.2.2.2.1");
builder.Writeln("Heading 1.2.2.2.2");

// Belgenin "Kaydet" metoduna geçirebileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .PDF'e nasıl dönüştüreceğini değiştirmek için.
PdfSaveOptions options = new PdfSaveOptions();

// Çıktı PDF belgesi, belge gövdesindeki başlıkları listeleyen bir içerik tablosu olan bir ana hat içerecektir.
// Bu taslaktaki bir girdiye tıkladığımızda ilgili başlığın bulunduğu yere gideceğiz.
// Anahattan 4'ün üstündeki tüm başlıkları hariç tutmak için "HeadingsOutlineLevels" özelliğini "4" olarak ayarlayın.
options.OutlineOptions.HeadingsOutlineLevels = 4;

// Bir ana hat girişinin kendisi ile aynı veya daha düşük seviyedeki bir sonraki giriş arasında daha yüksek seviyede müteakip girişler varsa,
// girişin solunda bir ok belirecektir. Bu giriş, bu tür birkaç "alt girişin" "sahibi"dir.
// Belgemizde, 5. başlık seviyesindeki ana hat girişleri, ikinci 4. seviye ana hat girişinin alt girişleridir.
// 4. ve 5. başlık seviyesi girişleri, 2. 3. seviye girişin alt girişleridir, vb.
// Anahatta, "sahip" girişinin okuna tıklayarak tüm alt girişlerini daraltabilir/genişletebiliriz.
// Tüm başlık düzeyi 2 ve alt anahat girişlerini otomatik olarak genişletmek için "ExpandedOutlineLevels" özelliğini "2" olarak ayarlayın
// ve belgeyi açtığımızda tüm seviye ve 3 ve üzeri girdileri daraltırız.
options.OutlineOptions.ExpandedOutlineLevels = 2;

doc.Save(ArtifactsDir + "PdfSaveOptions.ExpandedOutlineLevels.pdf", options);
```

### Ayrıca bakınız

* class [SaveOutputParameters](../../../aspose.words.saving/saveoutputparameters/)
* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Document](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)

---

## Save(*Stream, [SaveFormat](../../saveformat/)*) {#save}

Belgeyi belirtilen biçimi kullanarak bir akışa kaydeder.

```csharp
public SaveOutputParameters Save(Stream stream, SaveFormat saveFormat)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| stream | Stream | Belgenin nereye kaydedileceğini akıtın. |
| saveFormat | SaveFormat | Belgenin kaydedileceği biçim. |

### Geri dönüş değeri

İsteğe bağlı olarak kullanabileceğiniz ek bilgiler.

## Örnekler

Bir belgenin akışa nasıl kaydedileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Document.docx");

using (MemoryStream dstStream = new MemoryStream())
{
    doc.Save(dstStream, SaveFormat.Docx);

    // Akışın belgeyi içerdiğini doğrulayın.
    Assert.AreEqual("Hello World!\r\rHello Word!\r\r\rHello World!", new Document(dstStream).GetText().Trim());
}
```

Bir belgenin akış yoluyla bir görüntüye nasıl kaydedileceğini ve ardından görüntünün bu akıştan nasıl okunacağını gösterir.

```csharp
Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            builder.Font.Name = "Times New Roman";
            builder.Font.Size = 24;
            builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

            builder.InsertImage(ImageDir + "Logo.jpg");

#if NET461_OR_GREATER || JAVA
            using (MemoryStream stream = new MemoryStream())
            {
                doc.Save(stream, SaveFormat.Bmp);

                stream.Position = 0;

                // Akışı bir görüntüye geri oku.
                using (Image image = Image.FromStream(stream))
                {
                    Assert.AreEqual(ImageFormat.Bmp, image.RawFormat);
                    Assert.AreEqual(816, image.Width);
                    Assert.AreEqual(1056, image.Height);
                }
            }
#elif NET5_0_OR_GREATER
            using (MemoryStream stream = new MemoryStream())
            {
                doc.Save(stream, SaveFormat.Bmp);

                stream.Position = 0;

                SKCodec codec = SKCodec.Create(stream);
                Assert.AreEqual(SKEncodedImageFormat.Bmp, codec.EncodedFormat);

                stream.Position = 0;

                using (SKBitmap image = SKBitmap.Decode(stream))
                {
                    Assert.AreEqual(816, image.Width);
                    Assert.AreEqual(1056, image.Height);
                }
            }
#endif
```

### Ayrıca bakınız

* class [SaveOutputParameters](../../../aspose.words.saving/saveoutputparameters/)
* enum [SaveFormat](../../saveformat/)
* class [Document](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)

---

## Save(*Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/)*) {#save_1}

Belirtilen kaydetme seçeneklerini kullanarak belgeyi bir akışa kaydeder.

```csharp
public SaveOutputParameters Save(Stream stream, SaveOptions saveOptions)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| stream | Stream | Belgenin nereye kaydedileceğini akıtın. |
| saveOptions | SaveOptions | Belgenin nasıl kaydedileceğini kontrol eden seçenekleri belirtir.`hükümsüz` . Eğer bu ise`hükümsüz`, belge ikili DOC formatında kaydedilecektir. |

### Geri dönüş değeri

İsteğe bağlı olarak kullanabileceğiniz ek bilgiler.

## Örnekler

Bir belgedeki sayfaların yalnızca bir kısmının PDF'e nasıl dönüştürüleceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 3.");

using (Stream stream = File.Create(ArtifactsDir + "PdfSaveOptions.OnePage.pdf"))
{
    // Belgenin "Kaydet" metoduna geçirebileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
    // bu yöntemin belgeyi .PDF'e nasıl dönüştüreceğini değiştirmek için.
    PdfSaveOptions options = new PdfSaveOptions();

    // Belgenin ikinci sayfadan başlayarak bir kısmını işlemek için "PageIndex" değerini "1" olarak ayarlayın.
    options.PageSet = new PageSet(1);

    // Bu belge, ikinci sayfadan başlayarak tek bir sayfadan oluşacak ve ikinci sayfada yalnızca ikinci sayfa yer alacaktır.
    doc.Save(stream, options);
}
```

### Ayrıca bakınız

* class [SaveOutputParameters](../../../aspose.words.saving/saveoutputparameters/)
* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Document](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)

---

## Save(*HttpResponse, string, [ContentDisposition](../../contentdisposition/), [SaveOptions](../../../aspose.words.saving/saveoptions/)*) {#save_5}

Belgeyi istemci tarayıcısına gönderir.

```csharp
public SaveOutputParameters Save(HttpResponse response, string fileName, 
    ContentDisposition contentDisposition, SaveOptions saveOptions)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| response | HttpResponse | Belgenin kaydedileceği yanıt nesnesi. |
| fileName | String | İstemci tarayıcısında görünecek belgenin adı. Ad, yol içermemelidir. |
| contentDisposition | ContentDisposition | A[`ContentDisposition`](../../contentdisposition/) that değeri, belgenin istemci tarayıcısında nasıl sunulacağını belirtir. |
| saveOptions | SaveOptions | Belgenin nasıl kaydedileceğini kontrol eden seçenekleri belirtir.`hükümsüz`. |

### Geri dönüş değeri

İsteğe bağlı olarak kullanabileceğiniz ek bilgiler.

## Notlar

Dahili olarak, bu yöntem önce bir bellek akışına kaydeder ve ardından yanıt akışı aramayı desteklemediğinden yanıt akışına kopyalar.

## Örnekler

Posta birleştirmenin nasıl gerçekleştirileceğini ve ardından belgenin istemci tarayıcısına nasıl kaydedileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertField(" MERGEFIELD FullName ");
builder.InsertParagraph();
builder.InsertField(" MERGEFIELD Company ");
builder.InsertParagraph();
builder.InsertField(" MERGEFIELD Address ");
builder.InsertParagraph();
builder.InsertField(" MERGEFIELD City ");

doc.MailMerge.Execute(new string[] { "FullName", "Company", "Address", "City" },
    new object[] { "James Bond", "MI5 Headquarters", "Milbank", "London" });

// Belgeyi istemci tarayıcısına gönder.
//Testte HttpResponse boş olduğu için atıldı.
Assert.Throws<ArgumentNullException>(() => doc.Save(response, "Artifacts/MailMerge.ExecuteArray.docx", ContentDisposition.Inline, null));

// Kaydedildikten sonra belgeye gereksiz içerik eklememek için bu yanıtı manuel olarak kapatmamız gerekecek.
Assert.Throws<NullReferenceException>(() => response.End());
```

### Ayrıca bakınız

* class [SaveOutputParameters](../../../aspose.words.saving/saveoutputparameters/)
* enum [ContentDisposition](../../contentdisposition/)
* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Document](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
