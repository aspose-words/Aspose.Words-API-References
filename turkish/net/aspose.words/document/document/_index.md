---
title: Document
second_title: Aspose.Words for .NET API Referansı
description: Boş bir Word belgesi oluşturur.
type: docs
weight: 10
url: /tr/net/aspose.words/document/document/
---
## Document() {#constructor}

Boş bir Word belgesi oluşturur.

```csharp
public Document()
```

### Notlar

Belge kağıt boyutu varsayılan olarak Letter'dır. Sayfa kurulumunu değiştirmek istiyorsanız, use [`Bölüm.Sayfa Kurulumu`](../../section/pagesetup).

Oluşturduktan sonra kullanabilirsiniz[`DocumentBuilder`](../../documentbuilder) belge içeriğini kolayca eklemek için.

### Örnekler

Font özelliğini kullanarak bir metin akışının nasıl biçimlendirileceğini gösterir.

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

// Yeni Belge nesneleri varsayılan olarak minimum düğüm kümesiyle gelir
// metin ve şekiller gibi içerik eklemeye başlamak için gereklidir: a Bölüm, Gövde ve Paragraf.
doc.FirstSection.Body.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));

// 2 - Yerel dosya sisteminde bulunan bir belgeyi yükleyin:
doc = new Document(MyDir + "Document.docx");

// Yüklenen dokümanlar, erişebileceğimiz ve düzenleyebileceğimiz içeriklere sahip olacaktır.
Assert.AreEqual("Hello World!", doc.FirstSection.Body.FirstParagraph.GetText().Trim());

// Bir belgenin şifresini çözmek için şifre kullanmak gibi yükleme sırasında yapılması gereken bazı işlemler,
// belge yüklenirken bir LoadOptions nesnesi geçirilerek yapılabilir.
doc = new Document(MyDir + "Encrypted.docx", new LoadOptions("docPassword"));

Assert.AreEqual("Test encrypted document.", doc.FirstSection.Body.FirstParagraph.GetText().Trim());
```

### Ayrıca bakınız

* class [Document](../../document)
* ad alanı [Aspose.Words](../../document)
* toplantı [Aspose.Words](../../../)

---

## Document(string) {#constructor_3}

Bir dosyadan var olan bir belgeyi açar. Dosya biçimini otomatik olarak algılar.

```csharp
public Document(string fileName)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| fileName | String | Açılacak belgenin dosya adı. |

### istisnalar

| istisna | şart |
| --- | --- |
| [UnsupportedFileFormatException](../../unsupportedfileformatexception) | Belge biçimi tanınmıyor veya desteklenmiyor. |
| [FileCorruptedException](../../filecorruptedexception) | Belge bozuk görünüyor ve yüklenemiyor. |
| Exception | Belgeyle ilgili bir sorun var ve Aspose.Words geliştiricilerine bildirilmelidir. |
| IOException | Bir giriş/çıkış istisnası var. |
| [IncorrectPasswordException](../../incorrectpasswordexception) | Belge şifreli ve açmak için bir parola gerektiriyor, ancak yanlış bir parola girdiniz. |
| ArgumentException | Dosyanın adı boş veya boş dize olamaz. |

### Örnekler

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

// Aspose ürünlerini kullanarak PDF belgelerini yüklemenin iki yolu aşağıdadır.
// 1 - Aspose.Words belgesi olarak yükle:
Aspose.Words.Document asposeWordsDoc = new Aspose.Words.Document(ArtifactsDir + "PDF2Word.LoadPdf.pdf");

Assert.AreEqual("Hello world!", asposeWordsDoc.GetText().Trim());

// 2 - Aspose.Pdf belgesi olarak yükle:
Aspose.Pdf.Document asposePdfDoc = new Aspose.Pdf.Document(ArtifactsDir + "PDF2Word.LoadPdf.pdf");

TextFragmentAbsorber textFragmentAbsorber = new TextFragmentAbsorber();
asposePdfDoc.Pages.Accept(textFragmentAbsorber);

Assert.AreEqual("Hello world!", textFragmentAbsorber.Text.Trim());
```

### Ayrıca bakınız

* class [Document](../../document)
* ad alanı [Aspose.Words](../../document)
* toplantı [Aspose.Words](../../../)

---

## Document(string, LoadOptions) {#constructor_4}

Bir dosyadan var olan bir belgeyi açar. Şifreleme parolası gibi ek seçeneklerin belirlenmesine izin verir.

```csharp
public Document(string fileName, LoadOptions loadOptions)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| fileName | String | Açılacak belgenin dosya adı. |
| loadOptions | LoadOptions | Belge yüklerken kullanılacak ek seçenekler. Boş olabilir. |

### istisnalar

| istisna | şart |
| --- | --- |
| [UnsupportedFileFormatException](../../unsupportedfileformatexception) | Belge biçimi tanınmıyor veya desteklenmiyor. |
| [FileCorruptedException](../../filecorruptedexception) | Belge bozuk görünüyor ve yüklenemiyor. |
| Exception | Belgeyle ilgili bir sorun var ve Aspose.Words geliştiricilerine bildirilmelidir. |
| IOException | Bir giriş/çıkış istisnası var. |
| [IncorrectPasswordException](../../incorrectpasswordexception) | Belge şifreli ve açmak için bir parola gerektiriyor, ancak yanlış bir parola girdiniz. |
| ArgumentException | Dosyanın adı boş veya boş dize olamaz. |

### Örnekler

Şifrelenmiş bir Microsoft Word belgesinin nasıl yükleneceğini gösterir.

```csharp
Document doc;

// Aspose.Words şifreli bir belgeyi şifresi olmadan açmaya çalışırsak bir istisna atar.
Assert.Throws<IncorrectPasswordException>(() => doc = new Document(MyDir + "Encrypted.docx"));

// Böyle bir belge yüklenirken parola, bir LoadOptions nesnesi kullanılarak belgenin oluşturucusuna iletilir.
LoadOptions options = new LoadOptions("docPassword");

// Şifreli bir belgeyi LoadOptions nesnesiyle yüklemenin iki yolu vardır.
// 1 - Belgeyi yerel dosya sisteminden dosya adına göre yükleyin:
doc = new Document(MyDir + "Encrypted.docx", options);
// 2 - Belgeyi bir akıştan yükleyin:
using (Stream stream = File.OpenRead(MyDir + "Encrypted.docx"))
{
    doc = new Document(stream, options);
```

Belgelerin nasıl oluşturulacağını ve yükleneceğini gösterir.

```csharp
// Aspose.Words kullanarak Document nesnesi oluşturmanın iki yolu vardır.
// 1 - Boş bir belge oluşturun:
Document doc = new Document();

// Yeni Belge nesneleri varsayılan olarak minimum düğüm kümesiyle gelir
// metin ve şekiller gibi içerik eklemeye başlamak için gereklidir: a Bölüm, Gövde ve Paragraf.
doc.FirstSection.Body.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));

// 2 - Yerel dosya sisteminde bulunan bir belgeyi yükleyin:
doc = new Document(MyDir + "Document.docx");

// Yüklenen dokümanlar, erişebileceğimiz ve düzenleyebileceğimiz içeriklere sahip olacaktır.
Assert.AreEqual("Hello World!", doc.FirstSection.Body.FirstParagraph.GetText().Trim());

// Bir belgenin şifresini çözmek için şifre kullanmak gibi yükleme sırasında yapılması gereken bazı işlemler,
// belge yüklenirken bir LoadOptions nesnesi geçirilerek yapılabilir.
doc = new Document(MyDir + "Encrypted.docx", new LoadOptions("docPassword"));

Assert.AreEqual("Test encrypted document.", doc.FirstSection.Body.FirstParagraph.GetText().Trim());
```

### Ayrıca bakınız

* class [LoadOptions](../../../aspose.words.loading/loadoptions)
* class [Document](../../document)
* ad alanı [Aspose.Words](../../document)
* toplantı [Aspose.Words](../../../)

---

## Document(Stream) {#constructor_1}

Bir akıştan var olan bir belgeyi açar. Dosya biçimini otomatik olarak algılar.

```csharp
public Document(Stream stream)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| stream | Stream | Belgenin nereden yükleneceğini aktarın. |

### istisnalar

| istisna | şart |
| --- | --- |
| [UnsupportedFileFormatException](../../unsupportedfileformatexception) | Belge biçimi tanınmıyor veya desteklenmiyor. |
| [FileCorruptedException](../../filecorruptedexception) | Belge bozuk görünüyor ve yüklenemiyor. |
| Exception | Belgeyle ilgili bir sorun var ve Aspose.Words geliştiricilerine bildirilmelidir. |
| IOException | Bir giriş/çıkış istisnası var. |
| [IncorrectPasswordException](../../incorrectpasswordexception) | Belge şifreli ve açmak için bir parola gerektiriyor, ancak yanlış bir parola girdiniz. |
| ArgumentNullException | Akış boş olamaz. |
| NotSupportedException | Akış, okumayı veya aramayı desteklemiyor. |
| ObjectDisposedException | Akış, elden çıkarılan bir nesnedir. |

### Notlar

Belge, akışın başında saklanmalıdır. Akış rastgele konumlandırmayı desteklemelidir.

### Örnekler

Bir akış kullanarak bir belgenin nasıl yükleneceğini gösterir.

```csharp
using (Stream stream = File.OpenRead(MyDir + "Document.docx"))
{
    Document doc = new Document(stream);

    Assert.AreEqual("Hello World!\r\rHello Word!\r\r\rHello World!", doc.GetText().Trim());
}
```

Bir URL'den bir belgenin nasıl yükleneceğini gösterir.

```csharp
// Bir Microsoft Word belgesine işaret eden bir URL oluşturun.
const string url = "https://omextemplates.content.office.net/support/templates/en-us/tf16402488.dotx";

// Belgeyi bir bayt dizisine indirin, ardından bu diziyi bir bellek akışı kullanarak bir belgeye yükleyin.
using (WebClient webClient = new WebClient())
{
    byte[] dataBytes = webClient.DownloadData(url);

    using (MemoryStream byteStream = new MemoryStream(dataBytes))
    {
        Document doc = new Document(byteStream);

        // Bu aşamada belgenin içeriğini okuyup düzenleyebilir ve ardından yerel dosya sistemine kaydedebiliriz.
        Assert.AreEqual("Use this section to highlight your relevant passions, activities, and how you like to give back. " +
                        "It’s good to include Leadership and volunteer experiences here. " +
                        "Or show off important extras like publications, certifications, languages and more.",
            doc.FirstSection.Body.Paragraphs[4].GetText().Trim());

        doc.Save(ArtifactsDir + "Document.LoadFromWeb.docx");
    }
}
```

### Ayrıca bakınız

* class [Document](../../document)
* ad alanı [Aspose.Words](../../document)
* toplantı [Aspose.Words](../../../)

---

## Document(Stream, LoadOptions) {#constructor_2}

Bir akıştan var olan bir belgeyi açar. Şifreleme parolası gibi ek seçeneklerin belirlenmesine izin verir.

```csharp
public Document(Stream stream, LoadOptions loadOptions)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| stream | Stream | Belgenin nereden yükleneceği akış. |
| loadOptions | LoadOptions | Belge yüklerken kullanılacak ek seçenekler. Boş olabilir. |

### istisnalar

| istisna | şart |
| --- | --- |
| [UnsupportedFileFormatException](../../unsupportedfileformatexception) | Belge biçimi tanınmıyor veya desteklenmiyor. |
| [FileCorruptedException](../../filecorruptedexception) | Belge bozuk görünüyor ve yüklenemiyor. |
| Exception | Belgeyle ilgili bir sorun var ve Aspose.Words geliştiricilerine bildirilmelidir. |
| IOException | Bir giriş/çıkış istisnası var. |
| [IncorrectPasswordException](../../incorrectpasswordexception) | Belge şifreli ve açmak için bir parola gerektiriyor, ancak yanlış bir parola girdiniz. |
| ArgumentNullException | Akış boş olamaz. |
| NotSupportedException | Akış, okumayı veya aramayı desteklemiyor. |
| ObjectDisposedException | Akış, elden çıkarılan bir nesnedir. |

### Notlar

Belge, akışın başında saklanmalıdır. Akış rastgele konumlandırmayı desteklemelidir.

### Örnekler

Bir web sayfasının .docx dosyası olarak nasıl kaydedildiğini gösterir.

```csharp
const string url = "http://www.aspose.com/";

using (WebClient client = new WebClient()) 
{ 
    using (MemoryStream stream = new MemoryStream(client.DownloadData(url)))
    {
        // Göreli görüntü yollarının doğru bir şekilde alınmasını sağlamak için URL tekrar baseUri olarak kullanılır.
        LoadOptions options = new LoadOptions(LoadFormat.Html, "", url);

        // HTML belgesini akıştan yükleyin ve LoadOptions nesnesini iletin.
        Document doc = new Document(stream, options);

        // Bu aşamada belgenin içeriğini okuyup düzenleyebilir ve ardından yerel dosya sistemine kaydedebiliriz.
        doc.Save(ArtifactsDir + "Document.InsertHtmlFromWebPage.docx");
    }
}
```

Temel URI kullanarak bir akıştan görüntüler içeren bir HTML belgesinin nasıl açılacağını gösterir.

```csharp
using (Stream stream = File.OpenRead(MyDir + "Document.html"))
{
    // Yüklerken temel klasörün URI'sini iletin
    // böylece HTML belgesinde göreli URI'leri olan herhangi bir resim bulunabilir.
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

Şifrelenmiş bir Microsoft Word belgesinin nasıl yükleneceğini gösterir.

```csharp
Document doc;

// Aspose.Words şifreli bir belgeyi şifresi olmadan açmaya çalışırsak bir istisna atar.
Assert.Throws<IncorrectPasswordException>(() => doc = new Document(MyDir + "Encrypted.docx"));

// Böyle bir belge yüklenirken parola, bir LoadOptions nesnesi kullanılarak belgenin oluşturucusuna iletilir.
LoadOptions options = new LoadOptions("docPassword");

// Şifreli bir belgeyi LoadOptions nesnesiyle yüklemenin iki yolu vardır.
// 1 - Belgeyi yerel dosya sisteminden dosya adına göre yükleyin:
doc = new Document(MyDir + "Encrypted.docx", options);
// 2 - Belgeyi bir akıştan yükleyin:
using (Stream stream = File.OpenRead(MyDir + "Encrypted.docx"))
{
    doc = new Document(stream, options);
```

### Ayrıca bakınız

* class [LoadOptions](../../../aspose.words.loading/loadoptions)
* class [Document](../../document)
* ad alanı [Aspose.Words](../../document)
* toplantı [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
