---
title: HtmlLoadOptions.HtmlLoadOptions
second_title: Aspose.Words for .NET API Referansı
description: HtmlLoadOptions inşaatçı. Bu sınıfın yeni bir örneğini varsayılan değerlerle başlatır.
type: docs
weight: 10
url: /tr/net/aspose.words.loading/htmlloadoptions/htmlloadoptions/
---
## HtmlLoadOptions() {#constructor}

Bu sınıfın yeni bir örneğini varsayılan değerlerle başlatır.

```csharp
public HtmlLoadOptions()
```

### Örnekler

Bir HTML belgesi yüklenirken koşullu yorumların nasıl destekleneceğini gösterir.

```csharp
HtmlLoadOptions loadOptions = new HtmlLoadOptions();

// Değer doğruysa yüklenen belgeyi ayrıştırırken VML kodunu dikkate alırız.
loadOptions.SupportVml = supportVml;

// Bu belge "<!--[if gte vml 1]>" içinde bir JPEG resmi içeriyor etiketler,
// ve "<![if !vml]>" içinde farklı bir PNG resmi Etiketler.
// "SupportVml" bayrağını "true" olarak ayarlarsak Aspose.Words JPEG'i yükleyecektir.
// Bu bayrağı "false" olarak ayarlarsak Aspose.Words yalnızca PNG'yi yükleyecektir.
Document doc = new Document(MyDir + "VML conditional.htm", loadOptions);

if (supportVml)
    Assert.AreEqual(ImageType.Jpeg, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).ImageData.ImageType);
else
    Assert.AreEqual(ImageType.Png, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).ImageData.ImageType);
```

### Ayrıca bakınız

* class [HtmlLoadOptions](../)
* ad alanı [Aspose.Words.Loading](../../htmlloadoptions/)
* toplantı [Aspose.Words](../../../)

---

## HtmlLoadOptions(string) {#constructor_2}

Şifrelenmiş bir belgeyi yüklemek için bu sınıfın yeni bir örneğini belirtilen parolayla başlatmak için kullanılan bir kısayol.

```csharp
public HtmlLoadOptions(string password)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| password | String | Şifrelenmiş bir belgeyi açmak için kullanılan parola. Olabilir`hükümsüz` veya boş dize. |

### Örnekler

Bir Html belgesinin nasıl şifreleneceğini ve ardından parola kullanılarak nasıl açılacağını gösterir.

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
* ad alanı [Aspose.Words.Loading](../../htmlloadoptions/)
* toplantı [Aspose.Words](../../../)

---

## HtmlLoadOptions(LoadFormat, string, string) {#constructor_1}

Özellikleri belirtilen değerlere ayarlanmış olarak bu sınıfın yeni bir örneğini başlatmak için kullanılan bir kısayol.

```csharp
public HtmlLoadOptions(LoadFormat loadFormat, string password, string baseUri)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| loadFormat | LoadFormat | Yüklenecek belgenin formatı. |
| password | String | Şifrelenmiş bir belgeyi açmak için kullanılan parola. Olabilir`hükümsüz` veya boş dize. |
| baseUri | String | Göreli URI'leri mutlak olarak çözümlemek için kullanılacak dize. Olabilir`hükümsüz` veya boş dize. |

### Örnekler

Bir html belgesini açarken temel URI'nin nasıl belirtileceğini gösterir.

```csharp
// Göreli bir URI ile bağlantılı bir resim içeren bir .html belgesi yüklemek istediğimizi varsayalım
// resim farklı bir konumdayken. Bu durumda, göreceli URI'yi mutlak bir URI'ye dönüştürmemiz gerekecek.
 // HtmlLoadOptions nesnesini kullanarak bir temel URI sağlayabiliriz.
HtmlLoadOptions loadOptions = new HtmlLoadOptions(LoadFormat.Html, "", ImageDir);

Assert.AreEqual(LoadFormat.Html, loadOptions.LoadFormat);

Document doc = new Document(MyDir + "Missing image.html", loadOptions);

// Görüntü .html girişinde bozuk olsa da, özel temel URI'miz bağlantıyı onarmamıza yardımcı oldu.
Shape imageShape = (Shape)doc.GetChildNodes(NodeType.Shape, true)[0];
Assert.True(imageShape.IsImage);

// Bu çıktı belgesi eksik olan resmi gösterecektir.
doc.Save(ArtifactsDir + "HtmlLoadOptions.BaseUri.docx");
```

### Ayrıca bakınız

* enum [LoadFormat](../../../aspose.words/loadformat/)
* class [HtmlLoadOptions](../)
* ad alanı [Aspose.Words.Loading](../../htmlloadoptions/)
* toplantı [Aspose.Words](../../../)


