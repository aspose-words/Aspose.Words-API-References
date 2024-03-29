---
title: HtmlSaveOptions.EpubNavigationMapLevel
second_title: Aspose.Words for .NET API Referansı
description: HtmlSaveOptions mülk. IDPF EPUB formatına dışa aktarırken navigasyon haritasına doldurulan başlıkların maksimum seviyesini belirtir. Varsayılan değer3 .
type: docs
weight: 110
url: /tr/net/aspose.words.saving/htmlsaveoptions/epubnavigationmaplevel/
---
## HtmlSaveOptions.EpubNavigationMapLevel property

IDPF EPUB formatına dışa aktarırken navigasyon haritasına doldurulan başlıkların maksimum seviyesini belirtir. Varsayılan değer`3` .

```csharp
public int EpubNavigationMapLevel { get; set; }
```

### Notlar

IDPF EPUB biçimindeki gezinme haritası, kullanıcı aracılarının belge yapısı içinde kolay gezinme yolu sağlamasına olanak tanır. Gezinme noktaları genellikle belgedeki başlıklara karşılık gelir. Başlıkları düzeye kadar doldurmak için **N** bu değeri ata`EpubNavigationMapLevel`.

Varsayılan olarak, üç başlık düzeyi doldurulur: stil paragrafları **Başlık 1** , **Başlık 2** ve **Başlık 3**. Karşılık gelen maksimum düzeyi istemek için bu özelliği 1 ile 9 arasında bir değere ayarlayabilirsiniz. Sıfıra ayarlamak, gezinme haritasını yalnızca belge kökleri veya belge bölümlerinin köklerine indirgeyecektir.

### Örnekler

Kaydedilmiş bir Epub belgesinin gezinme panelinde görünen başlıkların nasıl filtreleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// "Başlık" stilini kullanarak biçimlendirdiğimiz her paragraf başlık işlevi görebilir.
// Her başlığın, başlık stilinin sayısına göre belirlenen bir başlık düzeyi de olabilir.
// Aşağıdaki başlıklar 1-3 seviyelerindedir.
builder.ParagraphFormat.Style = builder.Document.Styles["Heading 1"];
builder.Writeln("Heading #1");
builder.ParagraphFormat.Style = builder.Document.Styles["Heading 2"];
builder.Writeln("Heading #2");
builder.ParagraphFormat.Style = builder.Document.Styles["Heading 3"];
builder.Writeln("Heading #3");
builder.ParagraphFormat.Style = builder.Document.Styles["Heading 1"];
builder.Writeln("Heading #4");
builder.ParagraphFormat.Style = builder.Document.Styles["Heading 2"];
builder.Writeln("Heading #5");
builder.ParagraphFormat.Style = builder.Document.Styles["Heading 3"];
builder.Writeln("Heading #6");

// Epub okuyucuları genellikle belgeleri için bir içindekiler tablosu oluşturur.
// Belgedeki "Başlık" stiline sahip her paragraf bu içindekiler tablosunda bir giriş oluşturacaktır.
 // Maksimum başlık seviyesi ayarlamak için "EpubNavigationMapLevel" özelliğini kullanabiliriz.
// Epub okuyucu, içindekiler tablosuna belirttiğimiz seviyenin üzerinde olan başlıklar eklemeyecektir.
HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.Epub);
options.EpubNavigationMapLevel = 2;

// Belgemizin ikisi 2. seviyenin üzerinde olmak üzere altı başlığı vardır.
// Bu belgenin içindekiler tablosunda dört giriş olacaktır.
doc.Save(ArtifactsDir + "HtmlSaveOptions.EpubHeadings.epub", options);
```

### Ayrıca bakınız

* class [HtmlSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../htmlsaveoptions/)
* toplantı [Aspose.Words](../../../)


