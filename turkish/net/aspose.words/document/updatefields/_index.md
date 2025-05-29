---
title: Document.UpdateFields
linktitle: UpdateFields
articleTitle: UpdateFields
second_title: .NET için Aspose.Words
description: Belgenizi UpdateFields yöntemiyle yenileyin; gelişmiş doğruluk ve sorunsuz düzenleme için tüm alan değerlerini verimli bir şekilde yenileyin.
type: docs
weight: 810
url: /tr/net/aspose.words/document/updatefields/
---
## Document.UpdateFields method

Tüm belgedeki alanların değerlerini günceller.

```csharp
public void UpdateFields()
```

## Notlar

Bir belgeyi açtığınızda, değiştirdiğinizde ve kaydettiğinizde, Aspose.Words alanları otomatik olarak güncellemez, olduğu gibi korur. Bu nedenle, document 'yi programlı olarak değiştirdiyseniz ve kaydedilen belgede doğru (hesaplanan) alan değerlerinin göründüğünden emin olmak istiyorsanız, genellikle kaydetmeden önce bu yöntemi çağırmak istersiniz.

Bir posta birleştirme işlemini gerçekleştirdikten sonra alanları güncellemeye gerek yoktur, çünkü posta birleştirme bir tür update alanıdır ve belgedeki tüm alanları otomatik olarak günceller.

Bu yöntem tüm alan türlerini güncellemez. Desteklenen alan türlerinin ayrıntılı listesi için Programcı Kılavuzu'na bakın.

Bu yöntem, sayfa düzeni algoritmalarıyla ilgili alanları (örneğin PAGE, PAGES, PAGEREF) güncellemez. Sayfa düzeniyle ilgili alanlar, bir belgeyi görüntülediğinizde veya çağırdığınızda güncellenir.[`UpdatePageLayout`](../updatepagelayout/).

Kullanın[`NormalizeFieldTypes`](../normalizefieldtypes/) Alan türlerini etkileyen belge değişiklikleri varsa, alanların güncellenmesinden önceki yöntem.

Belgenin belirli bir bölümündeki alanları güncellemek için şunu kullanın:[`UpdateFields`](../../range/updatefields/).

## Örnekler

QUOTE alanının kullanılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Text özelliğinin değerini gösterecek bir QUOTE alanı ekleyin.
FieldQuote field = (FieldQuote)builder.InsertField(FieldType.FieldQuote, true);
field.Text = "\"Quoted text\"";

Assert.AreEqual(" QUOTE  \"\\\"Quoted text\\\"\"", field.GetFieldCode());

// Bir QUOTE alanı ekleyin ve içine bir DATE alanı yerleştirin.
// DATE alanları, Microsoft Word kullanarak belgeyi her açtığımızda değerlerini geçerli tarihe günceller.
// DATE alanını bu şekilde QUOTE alanının içine yerleştirmek değerini donduracaktır
// belgeyi oluşturduğumuz tarihe.
builder.Write("\nDocument creation date: ");
field = (FieldQuote)builder.InsertField(FieldType.FieldQuote, true);
builder.MoveTo(field.Separator);
builder.InsertField(FieldType.FieldDate, true);

Assert.AreEqual(" QUOTE \u0013 DATE \u0014" + DateTime.Now.Date.ToShortDateString() + "\u0015", field.GetFieldCode());

// Tüm alanları doğru sonuçları gösterecek şekilde güncelleyin.
doc.UpdateFields();

Assert.AreEqual("\"Quoted text\"", doc.Range.Fields[0].Result);

doc.Save(ArtifactsDir + "Field.QUOTE.docx");
```

Kullanıcı ayrıntılarının nasıl ayarlanacağını ve alanlar kullanılarak nasıl görüntüleneceğini gösterir.

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

// Kullanıcı adı, kullanıcı adı ve kullanıcı adresi değerlerini görüntüleyen kullanıcı adı alanlarını ekleyin
 // Yukarıda oluşturduğumuz UserInformation nesnesinin ilgili özellikleri.
Assert.AreEqual(userInformation.Name, builder.InsertField(" USERNAME ").Result);
Assert.AreEqual(userInformation.Initials, builder.InsertField(" USERINITIALS ").Result);
Assert.AreEqual(userInformation.Address, builder.InsertField(" USERADDRESS ").Result);

// Alan seçenekleri nesnesinin ayrıca tüm belgelerdeki alanların başvurabileceği statik bir varsayılan kullanıcısı vardır.
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

Başlık stillerini girdi olarak kullanarak bir belgeye İçindekiler Tablosu'nun (TOC) nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Belgenin ilk sayfasına bir içerik tablosu ekleyin.
// Tabloyu 1 ila 3 düzey başlıklarına sahip paragrafları alacak şekilde yapılandırın.
// Ayrıca, girişlerini bizi götürecek köprü metinleri olarak ayarlayın
// Microsoft Word'de sol tıklandığında başlığın bulunduğu yere.
builder.InsertTableOfContents("\\o \"1-3\" \\h \\z \\u");
builder.InsertBreak(BreakType.PageBreak);

// Başlık stilleri içeren paragraflar ekleyerek içindekiler tablosunu doldurun.
// 1 ile 3 arasında bir seviyeye sahip her başlık tabloda bir girdi oluşturacaktır.
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

// İçindekiler tablosu, güncel bir sonuç göstermek için güncellenmesi gereken bir tür alandır.
doc.UpdateFields();
doc.Save(ArtifactsDir + "DocumentBuilder.InsertToc.docx");
```

### Ayrıca bakınız

* class [Document](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
