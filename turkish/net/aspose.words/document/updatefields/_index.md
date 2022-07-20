---
title: UpdateFields
second_title: Aspose.Words for .NET API Referansı
description: Belgenin tamamındaki alanların değerlerini günceller.
type: docs
weight: 730
url: /tr/net/aspose.words/document/updatefields/
---
## Document.UpdateFields method

Belgenin tamamındaki alanların değerlerini günceller.

```csharp
public void UpdateFields()
```

### Notlar

Bir belgeyi açtığınızda, değiştirdiğinizde ve sonra kaydettiğinizde, Aspose.Words alanları otomatik olarak güncellemez, onları olduğu gibi tutar. Bu nedenle, document 'yi programlı olarak değiştirdiyseniz ve emin olmak istiyorsanız, kaydetmeden önce genellikle bu yöntemi çağırmak istersiniz. uygun (hesaplanmış) alan değerleri kaydedilen belgede görünür.

Adres mektup birleştirme yürütüldükten sonra alanları güncellemeye gerek yoktur çünkü adres mektup birleştirme bir tür update alanıdır ve belgedeki tüm alanları otomatik olarak günceller.

Bu yöntem tüm alan türlerini güncellemez. Desteklenen alan türlerinin ayrıntılı listesi için Programcı Kılavuzu'na bakın.

Bu yöntem, sayfa düzeni algoritmalarıyla ilgili alanları güncellemez (örn. PAGE, PAGES, PAGEREF). Bir belge oluşturduğunuzda veya çağırdığınızda sayfa düzeniyle ilgili alanlar güncellenir.[`UpdatePageLayout`](../updatepagelayout).

Kullan[`NormalizeFieldTypes`](../normalizefieldtypes) Alan türlerini etkileyen belge değişiklikleri varsa, alanların güncellenmesinden önceki yöntem.

Belge kullanımının belirli bir bölümündeki alanları güncellemek için[`UpdateFields`](../../range/updatefields).

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
// DATE alanları, Microsoft Word kullanarak belgeyi her açtığımızda değerlerini güncel tarihe günceller.
// DATE alanını QUOTE alanına bu şekilde yerleştirmek değerini dondurur
// belgeyi oluşturduğumuz tarihe.
builder.Write("\nDocument creation date: ");
field = (FieldQuote)builder.InsertField(FieldType.FieldQuote, true);
builder.MoveTo(field.Separator);
builder.InsertField(FieldType.FieldDate, true);

Assert.AreEqual(" QUOTE \u0013 DATE \u0014" + DateTime.Now.Date.ToShortDateString() + "\u0015", field.GetFieldCode());

// Doğru sonuçlarını görüntülemek için tüm alanları güncelleyin.
doc.UpdateFields();

Assert.AreEqual("\"Quoted text\"", doc.Range.Fields[0].Result);

doc.Save(ArtifactsDir + "Field.QUOTE.docx");
```

Kullanıcı ayrıntılarının nasıl ayarlanacağını ve alanları kullanarak nasıl görüntüleneceğini gösterir.

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

// değerlerini görüntüleyen USERNAME, USERINITIALS ve USERADDRESS alanlarını girin
// yukarıda oluşturduğumuz UserInformation nesnesinin ilgili özellikleri. 
Assert.AreEqual(userInformation.Name, builder.InsertField(" USERNAME ").Result);
Assert.AreEqual(userInformation.Initials, builder.InsertField(" USERINITIALS ").Result);
Assert.AreEqual(userInformation.Address, builder.InsertField(" USERADDRESS ").Result);

// Alan seçenekleri nesnesi ayrıca tüm belgelerdeki alanların başvurabileceği statik bir varsayılan kullanıcıya sahiptir.
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

Başlık stillerini girdi olarak kullanarak bir belgeye İçindekilerin (TOC) nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Belgenin ilk sayfası için bir içindekiler tablosu ekleyin.
// Tabloyu, 1'den 3'e kadar olan düzeylerdeki başlıklara sahip paragrafları alacak şekilde yapılandırın.
// Ayrıca, girişlerini bizi götürecek köprüler olarak ayarlayın
// Microsoft Word'de sol tıklandığında başlığın konumuna.
builder.InsertTableOfContents("\\o \"1-3\" \\h \\z \\u");
builder.InsertBreak(BreakType.PageBreak);

// Başlık stilleriyle paragraflar ekleyerek içindekileri doldurun.
// Seviyesi 1 ile 3 arasında olan bu tür her bir başlık, tabloda bir giriş oluşturacaktır.
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

// İçindekiler, güncel bir sonucu göstermek için güncellenmesi gereken türden bir alandır.
doc.UpdateFields();
doc.Save(ArtifactsDir + "DocumentBuilder.InsertToc.docx");
```

### Ayrıca bakınız

* class [Document](../../document)
* ad alanı [Aspose.Words](../../document)
* toplantı [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
