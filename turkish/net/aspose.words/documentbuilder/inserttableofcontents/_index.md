---
title: DocumentBuilder.InsertTableOfContents
second_title: Aspose.Words for .NET API Referansı
description: DocumentBuilder yöntem. Belgeye bir İçindekiler içindekiler alanı ekler.
type: docs
weight: 440
url: /tr/net/aspose.words/documentbuilder/inserttableofcontents/
---
## DocumentBuilder.InsertTableOfContents method

Belgeye bir İçindekiler (içindekiler) alanı ekler.

```csharp
public Field InsertTableOfContents(string switches)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| switches | String | TOC alanı değişir. |

### Notlar

Bu yöntem, geçerli konumdan belgeye bir İçindekiler (içindekiler) alanı ekler.

Bir Word belgesindeki içindekiler tablosu çeşitli şekillerde oluşturulabilir ve çeşitli seçenekler kullanılarak biçimlendirilebilir. Tablonun oluşturulma ve Microsoft Word tarafından görüntülenme şekli alan anahtarları tarafından kontrol edilir.

Anahtarları belirlemenin en kolay yolu, Ekle-&gt;Başvuru-&gt;Dizin ve Tablolar menüsünü kullanarak bir içindekiler tablosunu bir Word belgesine eklemek ve yapılandırmak, ardından anahtarları görmek için alan kodlarının görüntüsünü açmaktır. Alan kodlarının görüntülenmesini açıp kapatmak için Microsoft Word'de Alt+F9'a basabilirsiniz.

Örneğin, bir içindekiler tablosu oluşturduktan sonra, belgeye aşağıdaki alan eklenir: **{ TOC \o "1-3" \h \z \u }** . Kopyalayabilirsiniz **\o "1-3" \h \z \u** ve bunu switch parametresi olarak kullanın.

Dikkat **İçindekiler Tablosu Ekle** yalnızca bir TOC alanı ekleyecektir, ancak aslında içindekiler tablosunu oluşturmayacaktır. İçindekiler, alan güncellendiğinde Microsoft Word tarafından oluşturulur.

Bu yöntemi kullanarak bir içindekiler tablosu ekler ve ardından file dosyasını Microsoft Word'de açarsanız, TOC field henüz güncellenmediğinden içindekiler tablosunu görmezsiniz.

Microsoft Word'de, bir belge açıldığında alanlar otomatik olarak güncellenmez, ancak bir belgedeki alanları istediğiniz zaman F9 tuşuna basarak güncelleyebilirsiniz.

### Örnekler

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

* class [Field](../../../aspose.words.fields/field/)
* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../documentbuilder/)
* toplantı [Aspose.Words](../../../)


