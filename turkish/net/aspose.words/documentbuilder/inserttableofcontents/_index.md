---
title: DocumentBuilder.InsertTableOfContents
linktitle: InsertTableOfContents
articleTitle: InsertTableOfContents
second_title: .NET için Aspose.Words
description: DocumentBuilder InsertTableOfContents yöntemiyle belgelerinizi zahmetsizce geliştirin, kolay gezinme ve gelişmiş organizasyon için dinamik bir İçindekiler tablosu ekleyin.
type: docs
weight: 500
url: /tr/net/aspose.words/documentbuilder/inserttableofcontents/
---
## DocumentBuilder.InsertTableOfContents method

Belgeye bir TOC (içindekiler tablosu) alanı ekler.

```csharp
public Field InsertTableOfContents(string switches)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| switches | String | İçindekiler alanı değişir. |

## Notlar

Bu yöntem, belgenin geçerli konumuna at bir İçindekiler (TOC) alanı ekler.

Word belgesindeki bir içerik tablosu çeşitli yollarla oluşturulabilir ve çeşitli seçenekler kullanılarak biçimlendirilebilir. Tablonun oluşturulma ve Microsoft Word tarafından görüntülenme şekli alan anahtarları tarafından kontrol edilir.

Anahtarları belirtmenin en kolay yolu, Ekle-&gt;Başvuru-&gt;Dizin ve Tablolar menüsünü kullanarak bir Word belgesine içerik tablosu eklemek ve yapılandırmak, ardından anahtarları görmek için alan kodlarının gösterimini açmaktır. Alan kodlarının gösterimini açmak veya kapatmak için Microsoft Word'de Alt+F9 tuşlarına basabilirsiniz.

Örneğin, bir içindekiler tablosu oluşturulduktan sonra, belgeye aşağıdaki alan insert eklenir:**{ İçindekiler \o "1-3" \h \z \u }** . Kopyalayabilirsiniz**\o "1-3" \h \z \u** ve bunu anahtar parametresi olarak kullanın.

Dikkat`InsertTableOfContents` yalnızca bir TOC alanı ekleyecektir, ancak aslında içerik tablosunu oluşturmayacaktır. İçerik tablosu, alan güncellendiğinde Microsoft Word tarafından oluşturulur.

Bu yöntemi kullanarak bir içindekiler tablosu ekledikten sonra Microsoft Word'de dosyasını açarsanız, TOC alanı henüz güncellenmediği için içindekiler tablosunu göremezsiniz.

Microsoft Word'de, bir belge açıldığında alanlar otomatik olarak güncellenmez, ancak F9 tuşuna basarak belgedeki alanları istediğiniz zaman güncelleyebilirsiniz.

## Örnekler

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

* class [Field](../../../aspose.words.fields/field/)
* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
