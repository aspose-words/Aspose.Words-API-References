---
title: HtmlLoadOptions
linktitle: HtmlLoadOptions
articleTitle: HtmlLoadOptions
second_title: .NET için Aspose.Words
description: Sorunsuz web geliştirme için varsayılan ayarlarla örnekleri zahmetsizce başlatmak üzere tasarlanmış HtmlLoadOptions oluşturucusunu keşfedin.
type: docs
weight: 10
url: /tr/net/aspose.words.loading/htmlloadoptions/htmlloadoptions/
---
## HtmlLoadOptions() {#constructor}

Bu sınıfın yeni bir örneğini varsayılan değerlerle başlatır.

```csharp
public HtmlLoadOptions()
```

## Örnekler

Bir HTML belgesi yüklenirken koşullu yorumların nasıl destekleneceğini gösterir.

```csharp
HtmlLoadOptions loadOptions = new HtmlLoadOptions();

// Değer doğruysa, yüklenen belgeyi ayrıştırırken VML kodunu dikkate alırız.
loadOptions.SupportVml = supportVml;

// Bu belge "<!--[if gte vml 1]>" etiketleri arasında bir JPEG görüntüsü içeriyor,
// ve "<![if !vml]>" etiketleri arasında farklı bir PNG resmi.
// "SupportVml" bayrağını "true" olarak ayarlarsak, Aspose.Words JPEG'i yükleyecektir.
// Bu bayrağı "false" olarak ayarlarsak, Aspose.Words yalnızca PNG'yi yükleyecektir.
Document doc = new Document(MyDir + "VML conditional.htm", loadOptions);

if (supportVml)
    Assert.AreEqual(ImageType.Jpeg, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).ImageData.ImageType);
else
    Assert.AreEqual(ImageType.Png, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).ImageData.ImageType);
```

### Ayrıca bakınız

* class [HtmlLoadOptions](../)
* ad alanı [Aspose.Words.Loading](../../../aspose.words.loading/)
* toplantı [Aspose.Words](../../../)

---

## HtmlLoadOptions(*string*) {#constructor_2}

Şifrelenmiş bir belgeyi yüklemek için belirtilen parolayla bu sınıfın yeni bir örneğini başlatmak için bir kısayol.

```csharp
public HtmlLoadOptions(string password)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| password | String | Şifrelenmiş bir belgeyi açmak için şifre. Olabilir`hükümsüz` veya boş dize. |

## Örnekler

Bir Html belgesinin nasıl şifreleneceğini ve daha sonra parola kullanılarak nasıl açılacağını gösterir.

```csharp
// Şifrelenmiş bir .docx dosyasından şifrelenmiş bir HTML belgesi oluşturun ve imzalayın.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

SignOptions signOptions = new SignOptions
{
    Comments = "Comment",
    SignTime = DateTime.Now,
    DecryptionPassword = "docPassword"
};

string inputFileName = MyDir + "Encrypted.docx";
string outputFileName = ArtifactsDir + "HtmlLoadOptions.EncryptedHtml.html";
DigitalSignatureUtil.Sign(inputFileName, outputFileName, certificateHolder, signOptions);

// Bu belgeyi yüklemek ve okumak için şifre çözme işlemini geçmemiz gerekecek
// HtmlLoadOptions nesnesini kullanarak şifre.
HtmlLoadOptions loadOptions = new HtmlLoadOptions("docPassword");

Assert.AreEqual(signOptions.DecryptionPassword, loadOptions.Password);

Document doc = new Document(outputFileName, loadOptions);

Assert.AreEqual("Test encrypted document.", doc.GetText().Trim());
```

### Ayrıca bakınız

* class [HtmlLoadOptions](../)
* ad alanı [Aspose.Words.Loading](../../../aspose.words.loading/)
* toplantı [Aspose.Words](../../../)

---

## HtmlLoadOptions(*[LoadFormat](../../../aspose.words/loadformat/), string, string*) {#constructor_1}

Bu sınıfın özelliklerini belirtilen değerlere ayarlayarak yeni bir örneğini başlatmak için bir kısayol.

```csharp
public HtmlLoadOptions(LoadFormat loadFormat, string password, string baseUri)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| loadFormat | LoadFormat | Yüklenecek belgenin biçimi. |
| password | String | Şifrelenmiş bir belgeyi açmak için şifre. Olabilir`hükümsüz` veya boş dize. |
| baseUri | String | Göreceli URI'leri mutlak değere dönüştürmek için kullanılacak dize.`hükümsüz` veya boş dize. |

## Örnekler

Bir HTML belgesini açarken temel URI'nin nasıl belirtileceğini gösterir.

```csharp
// Göreceli bir URI ile bağlantılı bir resim içeren bir .html belgesi yüklemek istediğimizi varsayalım
// görüntü farklı bir konumdayken. Bu durumda, bağıl URI'yi mutlak olana dönüştürmemiz gerekecektir.
 // HtmlLoadOptions nesnesini kullanarak bir temel URI sağlayabiliriz.
HtmlLoadOptions loadOptions = new HtmlLoadOptions(LoadFormat.Html, "", ImageDir);

Assert.AreEqual(LoadFormat.Html, loadOptions.LoadFormat);

Document doc = new Document(MyDir + "Missing image.html", loadOptions);

// Giriş .html'deki resim bozulmuş olsa da, özel temel URI'miz bağlantıyı onarmamıza yardımcı oldu.
Shape imageShape = (Shape)doc.GetChildNodes(NodeType.Shape, true)[0];
Assert.True(imageShape.IsImage);

// Bu çıktı belgesi eksik olan resmi gösterecektir.
doc.Save(ArtifactsDir + "HtmlLoadOptions.BaseUri.docx");
```

### Ayrıca bakınız

* enum [LoadFormat](../../../aspose.words/loadformat/)
* class [HtmlLoadOptions](../)
* ad alanı [Aspose.Words.Loading](../../../aspose.words.loading/)
* toplantı [Aspose.Words](../../../)
