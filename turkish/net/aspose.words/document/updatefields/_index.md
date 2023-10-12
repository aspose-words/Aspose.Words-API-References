---
title: Document.UpdateFields
second_title: Aspose.Words for .NET API Referansı
description: Document yöntem. Belgenin tamamındaki alanların değerlerini günceller.
type: docs
weight: 770
url: /tr/net/aspose.words/document/updatefields/
---
## Document.UpdateFields method

Belgenin tamamındaki alanların değerlerini günceller.

```csharp
public void UpdateFields()
```

### Notlar

Bir belgeyi açtığınızda, değiştirdiğinizde ve ardından kaydettiğinizde Aspose.Words, alanları otomatik olarak güncellemez, onları olduğu gibi tutar. Bu nedenle, document dosyasını programlı olarak değiştirdiyseniz ve emin olmak istiyorsanız, genellikle kaydetmeden önce bu yöntemi çağırmak istersiniz. kaydedilen belgede uygun (hesaplanan) alan değerleri görünür.

Adres-mektup birleştirmeyi yürüttükten sonra alanları güncellemeye gerek yoktur çünkü adres-mektup birleştirme bir tür update alanıdır ve belgedeki tüm alanları otomatik olarak günceller.

Bu yöntem tüm alan türlerini güncellemez. Desteklenen alan türlerinin ayrıntılı listesi için Programcı Kılavuzu'na bakın.

Bu yöntem, sayfa düzeni algoritmalarıyla ilgili alanları (örn. PAGE, PAGES, PAGEREF) güncellemez. Sayfa düzeniyle ilgili alanlar, bir belgeyi oluşturduğunuzda veya çağrı yaptığınızda güncellenir.[`UpdatePageLayout`](../updatepagelayout/).

Kullan[`NormalizeFieldTypes`](../normalizefieldtypes/) Alan türlerini etkileyen belge değişiklikleri varsa alanlar güncellenmeden önce yöntem.

Belgenin belirli bir bölümündeki alanları güncellemek için şunu kullanın:[`UpdateFields`](../../range/updatefields/).

### Örnekler

QUOTE alanının kullanılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Text özelliğinin değerini gösterecek bir QUOTE alanı ekleyin.
FieldQuote field = (FieldQuote)builder.InsertField(FieldType.FieldQuote, true);
field.Text = "\"Quoted text\"";

Assert.AreEqual(" QUOTE  \"\\\"Quoted text\\\"\"", field.GetFieldCode());

// Bir QUOTE alanı ekleyin ve içine bir DATE alanı yerleştirin.
// DATE alanları, belgeyi Microsoft Word kullanarak her açtığımızda değerlerini geçerli tarihe günceller.
// DATE alanını QUOTE alanının içine bu şekilde yerleştirmek, değerini donduracaktır
// belgeyi oluşturduğumuz tarihe.
builder.Write("\nDocument creation date: ");
field = (FieldQuote)builder.InsertField(FieldType.FieldQuote, true);
builder.MoveTo(field.Separator);
builder.InsertField(FieldType.FieldDate, true);

Assert.AreEqual(" QUOTE \u0013 DATE \u0014" + DateTime.Now.Date.ToShortDateString() + "\u0015", field.GetFieldCode());

// Doğru sonuçları görüntülemek için tüm alanları güncelleyin.
doc.UpdateFields();

Assert.AreEqual("\"Quoted text\"", doc.Range.Fields[0].Result);

doc.Save(ArtifactsDir + "Field.QUOTE.docx");
```

Kullanıcı ayrıntılarının nasıl ayarlanacağını ve alanları kullanarak bunların nasıl görüntüleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Bir UserInformation nesnesi oluşturun ve bunu kullanıcı bilgilerini görüntüleyen alanlar için veri kaynağı olarak ayarlayın.
UserInformation userInformation = new UserInformation
{
    Name = "John Doe",
    Initials = "J. D.",
    Address = "123 Main Street"
};
doc.FieldOptions.CurrentUser = userInformation;

// değerlerini görüntüleyen USERNAME, USERINITIALS ve USERAADDRESS alanlarını ekleyin
 // yukarıda oluşturduğumuz UserInformation nesnesinin ilgili özellikleri.
Assert.AreEqual(userInformation.Name, builder.InsertField(" USERNAME ").Result);
Assert.AreEqual(userInformation.Initials, builder.InsertField(" USERINITIALS ").Result);
Assert.AreEqual(userInformation.Address, builder.InsertField(" USERADDRESS ").Result);

// Alan seçenekleri nesnesi aynı zamanda tüm belgelerdeki alanların başvurabileceği statik bir varsayılan kullanıcıya da sahiptir.
UserInformation.DefaultUser.Name = "Default User";
UserInformation.DefaultUser.Initials = "D. U.";
UserInformation.DefaultUser.Address = "One Microsoft Way";
doc.FieldOptions.CurrentUser = UserInformation.DefaultUser;

Assert.AreEqual("Default User", builder.InsertField(" USERNAME ").Result);
Assert.AreEqual("D. U.", builder.InsertField(" USERINITIALS ").Result);
Assert.AreEqual("One Microsoft Way", builder.InsertField(" USERADDRESS ").Result);

doc.UpdateFields();
doc.Save(ArtifactsDir + "FieldOptions.CurrentUser.docx");
```

Giriş olarak başlık stillerini kullanarak bir belgeye içindekiler tablosunun (TOC) nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Belgenin ilk sayfasına bir içindekiler tablosu ekleyin.
// Tabloyu, 1'den 3'e kadar düzeylerdeki başlıklara sahip paragrafları alacak şekilde yapılandırın.
// Ayrıca girişlerini bizi götürecek köprüler olacak şekilde ayarlayın
// Microsoft Word'de sol tıklandığında başlığın konumuna.
builder.InsertTableOfContents("\\o \"1-3\" \\h \\z \\u");
builder.InsertBreak(BreakType.PageBreak);

// Başlık stillerine sahip paragraflar ekleyerek içindekiler tablosunu doldurun.
// Seviyesi 1 ile 3 arasında olan bu tür başlıkların her biri tabloda bir giriş oluşturacaktır.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;
builder.Writeln("Heading 1.1");
builder.Writeln("Heading 1.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Writeln("Heading 2");
builder.Writeln("Heading 3");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;
builder.Writeln("Heading 3.1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading3;
builder.Writeln("Heading 3.1.1");
builder.Writeln("Heading 3.1.2");
builder.Writeln("Heading 3.1.3");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading4;
builder.Writeln("Heading 3.1.3.1");
builder.Writeln("Heading 3.1.3.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;
builder.Writeln("Heading 3.2");
builder.Writeln("Heading 3.3");

// İçindekiler tablosu, güncel bir sonucu göstermek için güncellenmesi gereken türden bir alandır.
doc.UpdateFields();
doc.Save(ArtifactsDir + "DocumentBuilder.InsertToc.docx");
```

### Ayrıca bakınız

* class [Document](../)
* ad alanı [Aspose.Words](../../document/)
* toplantı [Aspose.Words](../../../)


