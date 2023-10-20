---
title: DocumentBuilder.InsertTableOfContents
linktitle: InsertTableOfContents
articleTitle: InsertTableOfContents
second_title: Aspose.Words for .NET
description: DocumentBuilder InsertTableOfContents yöntem. Belgeye bir TOC içindekiler tablosu alanı ekler C#'da.
type: docs
weight: 460
url: /tr/net/aspose.words/documentbuilder/inserttableofcontents/
---
## DocumentBuilder.InsertTableOfContents method

Belgeye bir TOC (içindekiler tablosu) alanı ekler.

```csharp
public Field InsertTableOfContents(string switches)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| switches | String | TOC alanı değişir. |

## Notlar

Bu yöntem, belgenin konumunda geçerli konumuna bir TOC (içindekiler tablosu) alanı ekler.

Bir Word belgesindeki içindekiler tablosu çeşitli şekillerde oluşturulabilir ve çeşitli seçenekler kullanılarak biçimlendirilebilir. Tablonun oluşturulma ve Microsoft Word tarafından görüntülenme şekli, alan anahtarları tarafından kontrol edilir.

Anahtarları belirtmenin en kolay yolu, Ekle-&gt;Referans-&gt;Dizin ve Tablolar menüsünü, kullanarak bir Word belgesine içerikli bir tablo eklemek ve yapılandırmak, ardından anahtarları görmek için alan kodlarının görünümünü açmaktır. Alan kodlarının görüntülenmesini açmak veya kapatmak için Microsoft Word'de Alt+F9 tuşlarına basabilirsiniz.

Örneğin, bir içindekiler tablosu oluşturduktan sonra belgeye aşağıdaki alan eklenir :**{ TOC \o "1-3" \h \z \u }** . Kopyalayabilirsiniz**\o "1-3" \h \z \u** ve bunu switch parametresi olarak kullanın.

Dikkat`InsertTableOfContents` yalnızca bir İçindekiler alanı ekleyecektir, but aslında içindekiler tablosunu oluşturmayacaktır. İçindekiler tablosu, alan güncellendiğinde Microsoft Word tarafından oluşturulur.

Bu yöntemi kullanarak bir içindekiler tablosu eklerseniz ve ardından file dosyasını Microsoft Word'de açarsanız, TOC alanı henüz güncelleştirilmediğinden içindekiler tablosunu göremezsiniz.

Microsoft Word'de, bir belge açıldığında alanlar otomatik olarak güncellenmez, ancak bir belgedeki alanları istediğiniz zaman F9 tuşuna basarak güncelleyebilirsiniz.

## Örnekler

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

* class [Field](../../../aspose.words.fields/field/)
* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
