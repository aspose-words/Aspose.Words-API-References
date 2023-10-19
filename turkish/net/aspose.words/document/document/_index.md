---
title: Document
linktitle: Document
articleTitle: Document
second_title: Aspose.Words for .NET
description: Document inşaatçı. Boş bir Word belgesi oluşturur C#'da.
type: docs
weight: 10
url: /tr/net/aspose.words/document/document/
---
## Document() {#constructor}

Boş bir Word belgesi oluşturur.

```csharp
public Document()
```

## Notlar

Belge kağıt boyutu varsayılan olarak Letter'dır. Sayfa düzenini değiştirmek istiyorsanız kullanın[`PageSetup`](../../section/pagesetup/).

Oluşturduktan sonra kullanabilirsiniz[`DocumentBuilder`](../../documentbuilder/) belge içeriğini kolayca eklemek için.

## Örnekler

Font özelliğini kullanarak bir metin dizisinin nasıl biçimlendirileceğini gösterir.

```csharp
Document doc = new Document();
Run run = new Run(doc, "Hello world!");

Aspose.Words.Font font = run.Font;
font.Name = "Courier New";
font.Size = 36;
font.HighlightColor = Color.Yellow;

doc.FirstSection.Body.FirstParagraph.AppendChild(run);
doc.Save(ArtifactsDir + "Font.CreateFormattedRun.docx");
```

Belgelerin nasıl oluşturulacağını ve yükleneceğini gösterir.

```csharp
// Aspose.Words kullanarak Document nesnesi oluşturmanın iki yolu vardır.
// 1 - Boş bir belge oluşturun:
Document doc = new Document();

// Yeni Belge nesneleri varsayılan olarak minimum düğüm kümesiyle birlikte gelir
// metin ve şekil gibi içerikleri eklemeye başlamak için gereklidir: Bölüm, Gövde ve Paragraf.
doc.FirstSection.Body.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));

// 2 - Yerel dosya sisteminde bulunan bir belgeyi yükleyin:
doc = new Document(MyDir + "Document.docx");

// Yüklenen belgelerde erişebileceğimiz ve düzenleyebileceğimiz içerikler bulunacaktır.
Assert.AreEqual("Hello World!", doc.FirstSection.Body.FirstParagraph.GetText().Trim());

// Bir belgenin şifresini çözmek için şifre kullanmak gibi yükleme sırasında gerçekleşmesi gereken bazı işlemler,
// belge yüklenirken LoadOptions nesnesinin iletilmesiyle yapılabilir.
doc = new Document(MyDir + "Encrypted.docx", new LoadOptions("docPassword"));

Assert.AreEqual("Test encrypted document.", doc.FirstSection.Body.FirstParagraph.GetText().Trim());
```

### Ayrıca bakınız

* class [Document](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)

---

## Document(*string*) {#constructor_3}

Bir dosyadan mevcut bir belgeyi açar. Dosya biçimini otomatik olarak algılar.

```csharp
public Document(string fileName)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| fileName | String | Açılacak belgenin dosya adı. |

### istisnalar

| istisna | şart |
| --- | --- |
| [UnsupportedFileFormatException](../../unsupportedfileformatexception/) | Belge formatı tanınmıyor veya desteklenmiyor. |
| [FileCorruptedException](../../filecorruptedexception/) | Belge bozuk görünüyor ve yüklenemiyor. |
| Exception | Belgede bir sorun var ve Aspose.Words geliştiricilerine bildirilmesi gerekiyor. |
| IOException | Bir giriş/çıkış istisnası var. |
| [IncorrectPasswordException](../../incorrectpasswordexception/) | Belge şifrelenmiş ve açılması için parola gerekiyor, ancak yanlış parola girdiniz. |
| ArgumentException | Dosyanın adı boş veya boş dize olamaz. |

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

PDF'nin nasıl yükleneceğini gösterir.

```csharp
Aspose.Words.Document doc = new Aspose.Words.Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");

doc.Save(ArtifactsDir + "PDF2Word.LoadPdf.pdf");

// Aşağıda Aspose ürünlerini kullanarak PDF belgelerini yüklemenin iki yolu verilmiştir.
// 1 - Aspose.Words belgesi olarak yükle:
Aspose.Words.Document asposeWordsDoc = new Aspose.Words.Document(ArtifactsDir + "PDF2Word.LoadPdf.pdf");

Assert.AreEqual("Hello world!", asposeWordsDoc.GetText().Trim());

// 2 - Aspose.Pdf belgesi olarak yükleyin:
Aspose.Pdf.Document asposePdfDoc = new Aspose.Pdf.Document(ArtifactsDir + "PDF2Word.LoadPdf.pdf");

TextFragmentAbsorber textFragmentAbsorber = new TextFragmentAbsorber();
asposePdfDoc.Pages.Accept(textFragmentAbsorber);

Assert.AreEqual("Hello world!", textFragmentAbsorber.Text.Trim());
```

### Ayrıca bakınız

* class [Document](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)

---

## Document(*string, [LoadOptions](../../../aspose.words.loading/loadoptions/)*) {#constructor_4}

Bir dosyadan mevcut bir belgeyi açar. Şifreleme şifresi gibi ek seçeneklerin belirtilmesine olanak tanır.

```csharp
public Document(string fileName, LoadOptions loadOptions)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| fileName | String | Açılacak belgenin dosya adı. |
| loadOptions | LoadOptions | Belge yüklerken kullanılacak ek seçenekler. Olabilir`hükümsüz`. |

### istisnalar

| istisna | şart |
| --- | --- |
| [UnsupportedFileFormatException](../../unsupportedfileformatexception/) | Belge formatı tanınmıyor veya desteklenmiyor. |
| [FileCorruptedException](../../filecorruptedexception/) | Belge bozuk görünüyor ve yüklenemiyor. |
| Exception | Belgede bir sorun var ve Aspose.Words geliştiricilerine bildirilmesi gerekiyor. |
| IOException | Bir giriş/çıkış istisnası var. |
| [IncorrectPasswordException](../../incorrectpasswordexception/) | Belge şifrelenmiş ve açılması için parola gerekiyor, ancak yanlış parola girdiniz. |
| ArgumentException | Dosyanın adı boş veya boş dize olamaz. |

## Örnekler

Şifrelenmiş bir Microsoft Word belgesinin nasıl yükleneceğini gösterir.

```csharp
Document doc;

// Aspose.Words, şifrelenmiş bir belgeyi şifresi olmadan açmaya çalışırsak bir istisna atar.
Assert.Throws<IncorrectPasswordException>(() => doc = new Document(MyDir + "Encrypted.docx"));

// Böyle bir belge yüklenirken parola, LoadOptions nesnesi kullanılarak belgenin yapıcısına iletilir.
LoadOptions options = new LoadOptions("docPassword");

// Şifrelenmiş bir belgeyi LoadOptions nesnesiyle yüklemenin iki yolu vardır.
// 1 - Belgeyi yerel dosya sisteminden dosya adına göre yükleyin:
doc = new Document(MyDir + "Encrypted.docx", options);
// 2 - Belgeyi bir akıştan yükleyin:
using (Stream stream = File.OpenRead(MyDir + "Encrypted.docx"))
{
    doc = new Document(stream, options);
}
```

Belgelerin nasıl oluşturulacağını ve yükleneceğini gösterir.

```csharp
// Aspose.Words kullanarak Document nesnesi oluşturmanın iki yolu vardır.
// 1 - Boş bir belge oluşturun:
Document doc = new Document();

// Yeni Belge nesneleri varsayılan olarak minimum düğüm kümesiyle birlikte gelir
// metin ve şekil gibi içerikleri eklemeye başlamak için gereklidir: Bölüm, Gövde ve Paragraf.
doc.FirstSection.Body.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));

// 2 - Yerel dosya sisteminde bulunan bir belgeyi yükleyin:
doc = new Document(MyDir + "Document.docx");

// Yüklenen belgelerde erişebileceğimiz ve düzenleyebileceğimiz içerikler bulunacaktır.
Assert.AreEqual("Hello World!", doc.FirstSection.Body.FirstParagraph.GetText().Trim());

// Bir belgenin şifresini çözmek için şifre kullanmak gibi yükleme sırasında gerçekleşmesi gereken bazı işlemler,
// belge yüklenirken LoadOptions nesnesinin iletilmesiyle yapılabilir.
doc = new Document(MyDir + "Encrypted.docx", new LoadOptions("docPassword"));

Assert.AreEqual("Test encrypted document.", doc.FirstSection.Body.FirstParagraph.GetText().Trim());
```

### Ayrıca bakınız

* class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* class [Document](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)

---

## Document(*Stream*) {#constructor_1}

Bir akıştan mevcut bir belgeyi açar. Dosya biçimini otomatik olarak algılar.

```csharp
public Document(Stream stream)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| stream | Stream | Belgenin nereden yükleneceğini aktarın. |

### istisnalar

| istisna | şart |
| --- | --- |
| [UnsupportedFileFormatException](../../unsupportedfileformatexception/) | Belge formatı tanınmıyor veya desteklenmiyor. |
| [FileCorruptedException](../../filecorruptedexception/) | Belge bozuk görünüyor ve yüklenemiyor. |
| Exception | Belgede bir sorun var ve Aspose.Words geliştiricilerine bildirilmesi gerekiyor. |
| IOException | Bir giriş/çıkış istisnası var. |
| [IncorrectPasswordException](../../incorrectpasswordexception/) | Belge şifrelenmiş ve açılması için parola gerekiyor, ancak yanlış parola girdiniz. |
| ArgumentNullException | Akış boş olamaz. |
| NotSupportedException | Akış, okumayı veya aramayı desteklemiyor. |
| ObjectDisposedException | Akış, atılmış bir nesnedir. |

## Notlar

Belge akışın başında saklanmalıdır. Akış rastgele konumlandırmayı desteklemelidir.

## Örnekler

Akış kullanarak bir belgenin nasıl yükleneceğini gösterir.

```csharp
using (Stream stream = File.OpenRead(MyDir + "Document.docx"))
{
    Document doc = new Document(stream);

    Assert.AreEqual("Hello World!\r\rHello Word!\r\r\rHello World!", doc.GetText().Trim());
}
```

Bir URL'den belgenin nasıl yükleneceğini gösterir.

```csharp
// Microsoft Word belgesine işaret eden bir URL oluşturun.
const string url = "https://filesamples.com/samples/document/docx/sample3.docx";

// Belgeyi bir bayt dizisine indirin, ardından bu diziyi bir bellek akışı kullanarak bir belgeye yükleyin.
using (HttpClient webClient = new HttpClient())
{
    byte[] dataBytes = await webClient.GetByteArrayAsync(url);

    using (MemoryStream byteStream = new MemoryStream(dataBytes))
    {
        Document doc = new Document(byteStream);

        // Bu aşamada belgenin içeriğini okuyup düzenleyebilir ve ardından yerel dosya sistemine kaydedebiliriz.
        Assert.AreEqual("There are eight section headings in this document. At the beginning, \"Sample Document\" is a level 1 heading. " +
            "The main section headings, such as \"Headings\" and \"Lists\" are level 2 headings. " +
            "The Tables section contains two sub-headings, \"Simple Table\" and \"Complex Table,\" which are both level 3 headings.",                         
            doc.FirstSection.Body.Paragraphs[3].GetText().Trim());

        doc.Save(ArtifactsDir + "Document.LoadFromWeb.docx");
    }
}
```

### Ayrıca bakınız

* class [Document](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)

---

## Document(*Stream, [LoadOptions](../../../aspose.words.loading/loadoptions/)*) {#constructor_2}

Bir akıştan mevcut bir belgeyi açar. Şifreleme şifresi gibi ek seçeneklerin belirtilmesine olanak tanır.

```csharp
public Document(Stream stream, LoadOptions loadOptions)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| stream | Stream | Belgenin nereden yükleneceği akışı. |
| loadOptions | LoadOptions | Belge yüklerken kullanılacak ek seçenekler. Olabilir`hükümsüz`. |

### istisnalar

| istisna | şart |
| --- | --- |
| [UnsupportedFileFormatException](../../unsupportedfileformatexception/) | Belge formatı tanınmıyor veya desteklenmiyor. |
| [FileCorruptedException](../../filecorruptedexception/) | Belge bozuk görünüyor ve yüklenemiyor. |
| Exception | Belgede bir sorun var ve Aspose.Words geliştiricilerine bildirilmesi gerekiyor. |
| IOException | Bir giriş/çıkış istisnası var. |
| [IncorrectPasswordException](../../incorrectpasswordexception/) | Belge şifrelenmiş ve açılması için parola gerekiyor, ancak yanlış parola girdiniz. |
| ArgumentNullException | Akış boş olamaz. |
| NotSupportedException | Akış, okumayı veya aramayı desteklemiyor. |
| ObjectDisposedException | Akış, atılmış bir nesnedir. |

## Notlar

Belge akışın başında saklanmalıdır. Akış rastgele konumlandırmayı desteklemelidir.

## Örnekler

Temel URI kullanarak bir akıştan görüntüler içeren bir HTML belgesinin nasıl açılacağını gösterir.

```csharp
using (Stream stream = File.OpenRead(MyDir + "Document.html"))
{
    // Temel klasörü yüklerken URI'yi iletin
    // böylece HTML belgesindeki ilgili URI'lere sahip tüm görseller bulunabilir.
    LoadOptions loadOptions = new LoadOptions();
    loadOptions.BaseUri = ImageDir;

    Document doc = new Document(stream, loadOptions);

    // Belgenin ilk şeklinin geçerli bir resim içerdiğini doğrulayın.
    Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

    Assert.IsTrue(shape.IsImage);
    Assert.IsNotNull(shape.ImageData.ImageBytes);
    Assert.AreEqual(32.0, ConvertUtil.PointToPixel(shape.Width), 0.01);
    Assert.AreEqual(32.0, ConvertUtil.PointToPixel(shape.Height), 0.01);
}
```

Bir web sayfasının .docx dosyası olarak nasıl kaydedildiğini gösterir.

```csharp
const string url = "https://www.aspose.com/";

using (HttpClient client = new HttpClient()) 
{
    var bytes = await client.GetByteArrayAsync(url);
    using (MemoryStream stream = new MemoryStream(bytes))
    {
        // URL, ilgili görüntü yollarının doğru şekilde alındığından emin olmak için tekrar baseUri olarak kullanılır.
        LoadOptions options = new LoadOptions(LoadFormat.Html, "", url);

        // HTML belgesini akıştan yükleyin ve LoadOptions nesnesini iletin.
        Document doc = new Document(stream, options);

        // Bu aşamada belgenin içeriğini okuyup düzenleyebilir ve ardından yerel dosya sistemine kaydedebiliriz.
        doc.Save(ArtifactsDir + "Document.InsertHtmlFromWebPage.docx");
    }
}
```

Şifrelenmiş bir Microsoft Word belgesinin nasıl yükleneceğini gösterir.

```csharp
Document doc;

// Aspose.Words, şifrelenmiş bir belgeyi şifresi olmadan açmaya çalışırsak bir istisna atar.
Assert.Throws<IncorrectPasswordException>(() => doc = new Document(MyDir + "Encrypted.docx"));

// Böyle bir belge yüklenirken parola, LoadOptions nesnesi kullanılarak belgenin yapıcısına iletilir.
LoadOptions options = new LoadOptions("docPassword");

// Şifrelenmiş bir belgeyi LoadOptions nesnesiyle yüklemenin iki yolu vardır.
// 1 - Belgeyi yerel dosya sisteminden dosya adına göre yükleyin:
doc = new Document(MyDir + "Encrypted.docx", options);
// 2 - Belgeyi bir akıştan yükleyin:
using (Stream stream = File.OpenRead(MyDir + "Encrypted.docx"))
{
    doc = new Document(stream, options);
}
```

### Ayrıca bakınız

* class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* class [Document](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
