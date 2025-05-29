---
title: Document
linktitle: Document
articleTitle: Document
second_title: .NET için Aspose.Words
description: Kullanıcı dostu belge oluşturucumuzla boş Word belgelerini zahmetsizce oluşturun. Yazma sürecinizi bugün hızlandırın!
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

Kaynaklardan boş bir belge alınır ve varsayılan olarak, ortaya çıkan belge daha çok şu şekilde oluşturulur:Word2007. Bu boş belge varsayılan yazı tipleri tablosunu, minimum varsayılan stilleri ve gizli stilleri içerir.

[`OptimizeFor`](../../../aspose.words.settings/compatibilityoptions/optimizefor/) Bu yöntem, belirli bir MS Word sürümüne göre belge içeriklerini ve Aspose.Words'ün varsayılan davranışını iyileştirmek için kullanılabilir.

Belge kağıt boyutu varsayılan olarak Letter'dır. Sayfa düzenini değiştirmek istiyorsanız, use [`PageSetup`](../../section/pagesetup/).

Oluşturulduktan sonra kullanabilirsiniz[`DocumentBuilder`](../../documentbuilder/) Belge içeriğini kolayca eklemek için.

## Örnekler

Bir metin dizisinin font özelliğini kullanarak nasıl biçimlendirileceğini gösterir.

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

Basit bir belgenin nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();

// Yeni Belge nesneleri varsayılan olarak en az düğüm kümesiyle birlikte gelir
// metin ve şekiller gibi içerik eklemeye başlamak için gereklidir: Bir Bölüm, Bir Gövde ve Bir Paragraf.
doc.AppendChild(new Section(doc))
    .AppendChild(new Body(doc))
    .AppendChild(new Paragraph(doc))
    .AppendChild(new Run(doc, "Hello world!"));
```

Belgelerin nasıl oluşturulacağını ve yükleneceğini gösterir.

```csharp
// Aspose.Words kullanarak Belge nesnesi oluşturmanın iki yolu vardır.
// 1 - Boş bir belge oluşturun:
Document doc = new Document();

// Yeni Belge nesneleri varsayılan olarak en az düğüm kümesiyle birlikte gelir
// metin ve şekiller gibi içerik eklemeye başlamak için gereklidir: Bir Bölüm, Bir Gövde ve Bir Paragraf.
doc.FirstSection.Body.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));

// 2 - Yerel dosya sisteminde bulunan bir belgeyi yükleyin:
doc = new Document(MyDir + "Document.docx");

// Yüklenen dokümanlar erişebileceğimiz ve düzenleyebileceğimiz içeriklere sahip olacak.
Assert.AreEqual("Hello World!", doc.FirstSection.Body.FirstParagraph.GetText().Trim());

// Bir belgeyi şifresini çözmek için parola kullanmak gibi yükleme sırasında gerçekleşmesi gereken bazı işlemler,
// Belge yüklenirken LoadOptions nesnesi geçirilerek yapılabilir.
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
| [UnsupportedFileFormatException](../../unsupportedfileformatexception/) | Belge biçimi tanınmıyor veya desteklenmiyor. |
| [FileCorruptedException](../../filecorruptedexception/) | Belge bozuk görünüyor ve yüklenemiyor. |
| Exception | Belgede bir sorun var ve bu durum Aspose.Words geliştiricilerine bildirilmelidir. |
| IOException | Giriş/Çıkış istisnası var. |
| [IncorrectPasswordException](../../incorrectpasswordexception/) | Belge şifrelenmiş ve açmak için bir parola gerekiyor, ancak yanlış bir parola girdiniz. |
| ArgumentException | Dosyanın adı null veya boş dize olamaz. |

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

PDF'in nasıl yükleneceğini gösterir.

```csharp
Document doc = new Aspose.Words.Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");

doc.Save(ArtifactsDir + "PDF2Word.LoadPdf.pdf");

// Aşağıda Aspose ürünlerini kullanarak PDF belgelerini yüklemenin iki yolu bulunmaktadır.
// 1 - Aspose.Words belgesi olarak yükle:
Document asposeWordsDoc = new Document(ArtifactsDir + "PDF2Word.LoadPdf.pdf");

Assert.AreEqual("Hello world!", asposeWordsDoc.GetText().Trim());

// 2 - Aspose.Pdf belgesi olarak yükle:
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

Bir dosyadan mevcut bir belgeyi açar. Şifreleme parolası gibi ek seçeneklerin belirtilmesine olanak tanır.

```csharp
public Document(string fileName, LoadOptions loadOptions)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| fileName | String | Açılacak belgenin dosya adı. |
| loadOptions | LoadOptions | Bir belgeyi yüklerken kullanılacak ek seçenekler.`hükümsüz`. |

### istisnalar

| istisna | şart |
| --- | --- |
| [UnsupportedFileFormatException](../../unsupportedfileformatexception/) | Belge biçimi tanınmıyor veya desteklenmiyor. |
| [FileCorruptedException](../../filecorruptedexception/) | Belge bozuk görünüyor ve yüklenemiyor. |
| Exception | Belgede bir sorun var ve bu durum Aspose.Words geliştiricilerine bildirilmelidir. |
| IOException | Giriş/Çıkış istisnası var. |
| [IncorrectPasswordException](../../incorrectpasswordexception/) | Belge şifrelenmiş ve açmak için bir parola gerekiyor, ancak yanlış bir parola girdiniz. |
| ArgumentException | Dosyanın adı null veya boş dize olamaz. |

## Örnekler

Şifrelenmiş bir Microsoft Word belgesinin nasıl yükleneceğini gösterir.

```csharp
Document doc;

// Şifreli bir belgeyi şifresi olmadan açmaya çalıştığımızda Aspose.Words bir istisna fırlatır.
Assert.Throws<IncorrectPasswordException>(() => doc = new Document(MyDir + "Encrypted.docx"));

// Böyle bir belge yüklenirken parola, LoadOptions nesnesi kullanılarak belgenin oluşturucusuna geçirilir.
LoadOptions options = new LoadOptions("docPassword");

// Şifrelenmiş bir belgeyi LoadOptions nesnesiyle yüklemenin iki yolu vardır.
// 1 - Belgeyi yerel dosya sisteminden dosya adına göre yükle:
doc = new Document(MyDir + "Encrypted.docx", options);
// 2 - Belgeyi bir akıştan yükleyin:
using (Stream stream = File.OpenRead(MyDir + "Encrypted.docx"))
{
    doc = new Document(stream, options);
}
```

Belgelerin nasıl oluşturulacağını ve yükleneceğini gösterir.

```csharp
// Aspose.Words kullanarak Belge nesnesi oluşturmanın iki yolu vardır.
// 1 - Boş bir belge oluşturun:
Document doc = new Document();

// Yeni Belge nesneleri varsayılan olarak en az düğüm kümesiyle birlikte gelir
// metin ve şekiller gibi içerik eklemeye başlamak için gereklidir: Bir Bölüm, Bir Gövde ve Bir Paragraf.
doc.FirstSection.Body.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));

// 2 - Yerel dosya sisteminde bulunan bir belgeyi yükleyin:
doc = new Document(MyDir + "Document.docx");

// Yüklenen dokümanlar erişebileceğimiz ve düzenleyebileceğimiz içeriklere sahip olacak.
Assert.AreEqual("Hello World!", doc.FirstSection.Body.FirstParagraph.GetText().Trim());

// Bir belgeyi şifresini çözmek için parola kullanmak gibi yükleme sırasında gerçekleşmesi gereken bazı işlemler,
// Belge yüklenirken LoadOptions nesnesi geçirilerek yapılabilir.
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
| stream | Stream | Belgenin nereden yükleneceğini akışa alın. |

### istisnalar

| istisna | şart |
| --- | --- |
| [UnsupportedFileFormatException](../../unsupportedfileformatexception/) | Belge biçimi tanınmıyor veya desteklenmiyor. |
| [FileCorruptedException](../../filecorruptedexception/) | Belge bozuk görünüyor ve yüklenemiyor. |
| Exception | Belgede bir sorun var ve bu durum Aspose.Words geliştiricilerine bildirilmelidir. |
| IOException | Giriş/Çıkış istisnası var. |
| [IncorrectPasswordException](../../incorrectpasswordexception/) | Belge şifrelenmiş ve açmak için bir parola gerekiyor, ancak yanlış bir parola girdiniz. |
| ArgumentNullException | Akış boş olamaz. |
| NotSupportedException | Akış okumayı veya aramayı desteklemiyor. |
| ObjectDisposedException | Akarsu, elden çıkarılmış bir nesnedir. |

## Notlar

Belge akışın başlangıcında saklanmalıdır. Akış rastgele konumlandırmayı desteklemelidir.

## Örnekler

Bir belgenin akış kullanılarak nasıl yükleneceğini gösterir.

```csharp
using (Stream stream = File.OpenRead(MyDir + "Document.docx"))
{
    Document doc = new Document(stream);

    Assert.AreEqual("Hello World!\r\rHello Word!\r\r\rHello World!", doc.GetText().Trim());
}
```

Bir belgenin URL'den nasıl yükleneceğini gösterir.

```csharp
// Microsoft Word belgesine işaret eden bir URL oluşturun.
const string url = "https://dosyaörnekleri.com/örnekler/belge/docx/örnek3.docx";

// Belgeyi bir bayt dizisine indirin, ardından bu diziyi bir bellek akışı kullanarak bir belgeye yükleyin.
using (WebClient webClient = new WebClient())
{
    byte[] dataBytes = webClient.DownloadData(url);

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

Bir akıştan mevcut bir belgeyi açar. Şifreleme parolası gibi ek seçeneklerin belirtilmesine olanak tanır.

```csharp
public Document(Stream stream, LoadOptions loadOptions)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| stream | Stream | Belgenin nereden yükleneceğini gösteren akış. |
| loadOptions | LoadOptions | Bir belgeyi yüklerken kullanılacak ek seçenekler.`hükümsüz`. |

### istisnalar

| istisna | şart |
| --- | --- |
| [UnsupportedFileFormatException](../../unsupportedfileformatexception/) | Belge biçimi tanınmıyor veya desteklenmiyor. |
| [FileCorruptedException](../../filecorruptedexception/) | Belge bozuk görünüyor ve yüklenemiyor. |
| Exception | Belgede bir sorun var ve bu durum Aspose.Words geliştiricilerine bildirilmelidir. |
| IOException | Giriş/Çıkış istisnası var. |
| [IncorrectPasswordException](../../incorrectpasswordexception/) | Belge şifrelenmiş ve açmak için bir parola gerekiyor, ancak yanlış bir parola girdiniz. |
| ArgumentNullException | Akış boş olamaz. |
| NotSupportedException | Akış okumayı veya aramayı desteklemiyor. |
| ObjectDisposedException | Akarsu, elden çıkarılmış bir nesnedir. |

## Notlar

Belge akışın başlangıcında saklanmalıdır. Akış rastgele konumlandırmayı desteklemelidir.

## Örnekler

Bir akıştan gelen görselleri içeren bir HTML belgesinin temel URI kullanılarak nasıl açılacağını gösterir.

```csharp
using (Stream stream = File.OpenRead(MyDir + "Document.html"))
{
    // Yükleme sırasında temel klasörün URI'sini geçirin
    // böylece HTML belgesinde bağıl URI'leri olan tüm resimler bulunabilir.
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

Bir web sayfasının .docx dosyası olarak nasıl kaydedileceğini gösterir.

```csharp
const string url = "https://ürünler.aspose.com/kelimeler/";

using (WebClient client = new WebClient())
{
    var bytes = client.DownloadData(url);
    using (MemoryStream stream = new MemoryStream(bytes))
    {
        // Herhangi bir bağıl görüntü yolunun doğru şekilde alındığından emin olmak için URL tekrar bir baseUri olarak kullanılır.
        LoadOptions options = new LoadOptions(LoadFormat.Html, "", url);

        // HTML belgesini akıştan yükleyin ve LoadOptions nesnesini geçirin.
        Document doc = new Document(stream, options);

        // Bu aşamada belgenin içeriğini okuyup düzenleyebilir ve ardından yerel dosya sistemine kaydedebiliriz.
        doc.Save(ArtifactsDir + "Document.InsertHtmlFromWebPage.docx");
    }
}
```

Şifrelenmiş bir Microsoft Word belgesinin nasıl yükleneceğini gösterir.

```csharp
Document doc;

// Şifreli bir belgeyi şifresi olmadan açmaya çalıştığımızda Aspose.Words bir istisna fırlatır.
Assert.Throws<IncorrectPasswordException>(() => doc = new Document(MyDir + "Encrypted.docx"));

// Böyle bir belge yüklenirken parola, LoadOptions nesnesi kullanılarak belgenin oluşturucusuna geçirilir.
LoadOptions options = new LoadOptions("docPassword");

// Şifrelenmiş bir belgeyi LoadOptions nesnesiyle yüklemenin iki yolu vardır.
// 1 - Belgeyi yerel dosya sisteminden dosya adına göre yükle:
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
