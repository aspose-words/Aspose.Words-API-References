---
title: Document.Save
linktitle: Save
articleTitle: Save
second_title: Aspose.Words for .NET
description: Document Save yöntem. Belgeyi bir dosyaya kaydeder. Uzantıdan kaydetme biçimini otomatik olarak belirler C#'da.
type: docs
weight: 700
url: /tr/net/aspose.words/document/save/
---
## Save(*string*) {#save_2}

Belgeyi bir dosyaya kaydeder. Uzantıdan kaydetme biçimini otomatik olarak belirler.

```csharp
public SaveOutputParameters Save(string fileName)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| fileName | String | Belgenin adı. the belirtilen dosya adına sahip bir belge zaten mevcutsa, mevcut belgenin üzerine yazılır. |

### Geri dönüş değeri

İsteğe bağlı olarak kullanabileceğiniz ek bilgiler.

## Örnekler

Bir belgenin nasıl açılacağını ve .PDF'ye nasıl dönüştürüleceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Document.docx");

doc.Save(ArtifactsDir + "Document.ConvertToPdf.pdf");
```

PDF'nin .docx'e nasıl dönüştürüleceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");

doc.Save(ArtifactsDir + "PDF2Word.ConvertPdfToDocx.pdf");

// Az önce kaydettiğimiz PDF belgesini yükleyin ve .docx'e dönüştürün.
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

Belgeyi belirtilen formatta bir dosyaya kaydeder.

```csharp
public SaveOutputParameters Save(string fileName, SaveFormat saveFormat)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| fileName | String | Belgenin adı. the belirtilen dosya adına sahip bir belge zaten mevcutsa, mevcut belgenin üzerine yazılır. |
| saveFormat | SaveFormat | Belgenin kaydedileceği format. |

### Geri dönüş değeri

İsteğe bağlı olarak kullanabileceğiniz ek bilgiler.

## Örnekler

DOCX'ten HTML biçimine nasıl dönüştürüleceğini gösterir.

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
| fileName | String | Belgenin adı. the belirtilen dosya adına sahip bir belge zaten mevcutsa, mevcut belgenin üzerine yazılır. |
| saveOptions | SaveOptions | Belgenin nasıl kaydedileceğini denetleyen seçenekleri belirtir. Olabilir`hükümsüz`. |

### Geri dönüş değeri

İsteğe bağlı olarak kullanabileceğiniz ek bilgiler.

## Örnekler

İşlenen bir belgenin kalitesinin SaveOptions ile nasıl iyileştirileceğini gösterir.

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

PDF'nin .docx'e nasıl dönüştürüleceğini ve SaveOptions nesnesiyle kaydetme işleminin nasıl özelleştirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

doc.Save(ArtifactsDir + "PDF2Word.ConvertPdfToDocxCustom.pdf");

// Az önce kaydettiğimiz PDF belgesini yükleyin ve .docx'e dönüştürün.
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

// Belgenin "Save" yöntemine aktarabileceğimiz bir "ImageSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi bir görüntüye dönüştürme biçimini değiştirmek için.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);

for (int i = 0; i < doc.PageCount; i++)
{
    // "PageSet" özelliğini ilk sayfanın numarasına ayarlayın
    // belgenin görüntülenmeye nereden başlayacağı.
    options.PageSet = new PageSet(i);
    // Sayfayı 2325x5325 piksel ve 600 dpi çözünürlükte dışa aktarın.
    options.Resolution = 600;
    options.ImageSize = new Size(2325, 5325);

    doc.Save(ArtifactsDir + $"ImageSaveOptions.PageByPage.{i + 1}.tiff", options);
}
```

Bir belgedeki bir sayfanın JPEG görüntüsüne nasıl dönüştürüleceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2.");
builder.InsertImage(ImageDir + "Logo.jpg");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 3.");

// Belgenin "Save" yöntemine aktarabileceğimiz bir "ImageSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi bir görüntüye dönüştürme biçimini değiştirmek için.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Jpeg);

// İkinci sayfayı seçmek için "PageSet"i "1" olarak ayarlayın
// belgenin görüntülenmeye başlanacağı sıfır tabanlı dizin.
options.PageSet = new PageSet(1);

// Belgeyi JPEG formatında kaydettiğimizde Aspose.Words yalnızca bir sayfa oluşturur.
// Bu görüntü ikinci sayfadan başlayarak bir sayfa içerecektir,
// bu sadece orijinal belgenin ikinci sayfası olacaktır.
doc.Save(ArtifactsDir + "ImageSaveOptions.OnePage.jpg", options);
```

Bir belgeyi JPEG olarak kaydederken sıkıştırmanın nasıl yapılandırılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertImage(ImageDir + "Logo.jpg");

// Belgenin "Save" yöntemine aktarabileceğimiz bir "ImageSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi bir görüntüye dönüştürme biçimini değiştirmek için.
ImageSaveOptions imageOptions = new ImageSaveOptions(SaveFormat.Jpeg);

// Belgeyi oluştururken daha güçlü sıkıştırma kullanmak için "JpegQuality" özelliğini "10" olarak ayarlayın.
// Bu, belgenin dosya boyutunu azaltacaktır ancak görüntü, sıkıştırma kusurlarını daha belirgin bir şekilde görüntüleyecektir.
imageOptions.JpegQuality = 10;

doc.Save(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighCompression.jpg", imageOptions);

Assert.That(20000, Is.AtLeast(new FileInfo(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighCompression.jpg").Length));

// Belgeyi işlerken daha zayıf sıkıştırma kullanmak için "JpegQuality" özelliğini "100" olarak ayarlayın.
// Bu, dosya boyutunun artması pahasına görüntünün kalitesini artıracaktır.
imageOptions.JpegQuality = 100;

doc.Save(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighQuality.jpg", imageOptions);

Assert.That(60000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighQuality.jpg").Length));
```

Belgenin ana hatlarında üç düzeyde bir belgenin tamamının PDF'ye nasıl dönüştürüleceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 1'den 5'e kadar olan düzeylerin başlıklarını ekleyin.
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

// Belgenin "Save" yöntemine aktarabileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .PDF'ye dönüştürme biçimini değiştirmek için.
PdfSaveOptions options = new PdfSaveOptions();

// Çıktı PDF belgesi, belge gövdesindeki başlıkları listeleyen bir içindekiler tablosu olan bir taslak içerecektir.
// Bu taslaktaki bir girişe tıklamak bizi ilgili başlığın konumuna götürecektir.
// Seviyeleri 4'ün üzerinde olan tüm başlıkları anahattan hariç tutmak için "HeadingsOutlineLevels" özelliğini "4" olarak ayarlayın.
options.OutlineOptions.HeadingsOutlineLevels = 4;

// Bir anahat girişinin kendisi ile aynı veya daha düşük seviyedeki bir sonraki giriş arasında daha yüksek seviyedeki sonraki girişleri varsa,
// girişin solunda bir ok görünecektir. Bu giriş, bu tür birçok "alt girişin" "sahibidir".
// Belgemizde 5. başlık seviyesindeki taslak girişleri, ikinci 4. seviye taslak girişinin alt girişleridir,
// 4. ve 5. başlık seviyesi girişleri, ikinci 3. seviye girişinin alt girişleridir, vb.
// Ana hatlarıyla, tüm alt girişlerini daraltmak/genişletmek için "sahip" girişinin okuna tıklayabiliriz.
// Tüm başlık düzeyi 2'yi ve alt anahat girişlerini otomatik olarak genişletmek için "ExpandedOutlineLevels" özelliğini "2" olarak ayarlayın
// ve belgeyi açtığımızda tüm seviye ve 3 ve üzeri girişleri daraltıyoruz.
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

Belirtilen formatı kullanarak belgeyi bir akışa kaydeder.

```csharp
public SaveOutputParameters Save(Stream stream, SaveFormat saveFormat)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| stream | Stream | Belgenin nereye kaydedileceğini aktarın. |
| saveFormat | SaveFormat | Belgenin kaydedileceği format. |

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

#if NET48 || JAVA
            using (MemoryStream stream = new MemoryStream())
            {
                doc.Save(stream, SaveFormat.Bmp);

                stream.Position = 0;

                // Akışı bir görüntüye geri okuyun.
                using (Image image = Image.FromStream(stream))
                {
                    Assert.AreEqual(ImageFormat.Bmp, image.RawFormat);
                    Assert.AreEqual(816, image.Width);
                    Assert.AreEqual(1056, image.Height);
                }
            }
#elif NET5_0_OR_GREATER || __MOBILE__
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
| stream | Stream | Belgenin nereye kaydedileceğini aktarın. |
| saveOptions | SaveOptions | Belgenin nasıl kaydedileceğini denetleyen seçenekleri belirtir. Olabilir`hükümsüz` . Eğer bu ise`hükümsüz`, belge ikili DOC biçiminde kaydedilecektir. |

### Geri dönüş değeri

İsteğe bağlı olarak kullanabileceğiniz ek bilgiler.

## Örnekler

Bir belgedeki sayfaların yalnızca bazılarının PDF'ye nasıl dönüştürüleceğini gösterir.

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
    // Belgenin "Save" yöntemine aktarabileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
    // bu yöntemin belgeyi .PDF'ye dönüştürme biçimini değiştirmek için.
    PdfSaveOptions options = new PdfSaveOptions();

    // Belgenin ikinci sayfadan başlayarak bir kısmını oluşturmak için "PageIndex"i "1" olarak ayarlayın.
    options.PageSet = new PageSet(1);

    // Bu belge ikinci sayfadan başlayarak yalnızca ikinci sayfayı içerecek bir sayfa içerecektir.
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
| contentDisposition | ContentDisposition | A[`ContentDisposition`](../../contentdisposition/)that değeri belgenin istemci tarayıcısında nasıl sunulacağını belirtir. |
| saveOptions | SaveOptions | Belgenin nasıl kaydedileceğini denetleyen seçenekleri belirtir. Olabilir`hükümsüz`. |

### Geri dönüş değeri

İsteğe bağlı olarak kullanabileceğiniz ek bilgiler.

## Notlar

Dahili olarak bu yöntem önce bir bellek akışına kaydeder ve ardından yanıt akışı aramayı desteklemediğinden yanıt akışı 'ye kopyalar.

## Örnekler

Adres-mektup birleştirmenin nasıl gerçekleştirileceğini ve ardından belgenin istemci tarayıcısına nasıl kaydedileceğini gösterir.

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

// Belgeyi istemci tarayıcısına gönderin.
Assert.That(() => doc.Save(response, "Artifacts/MailMerge.ExecuteArray.docx", ContentDisposition.Inline, null),
    Throws.TypeOf<ArgumentNullException>()); //HttpResponse testte null olduğundan atıldı.

// Kaydettikten sonra belgeye gereksiz içerik eklemediğimizden emin olmak için bu yanıtı manuel olarak kapatmamız gerekecek.
Assert.That(() => response.End(), Throws.TypeOf<NullReferenceException>());
```

### Ayrıca bakınız

* class [SaveOutputParameters](../../../aspose.words.saving/saveoutputparameters/)
* enum [ContentDisposition](../../contentdisposition/)
* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Document](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
