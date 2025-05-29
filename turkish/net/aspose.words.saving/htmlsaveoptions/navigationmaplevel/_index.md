---
title: HtmlSaveOptions.NavigationMapLevel
linktitle: NavigationMapLevel
articleTitle: NavigationMapLevel
second_title: .NET için Aspose.Words
description: HtmlSaveOptions' NavigationMapLevel özelliğini keşfedin, EPUB, MOBI ve AZW3 dışa aktarımlarında başlık seviyelerini kontrol edin. İçeriğinizin görünürlüğünü en üst düzeye çıkarın!
type: docs
weight: 390
url: /tr/net/aspose.words.saving/htmlsaveoptions/navigationmaplevel/
---
## HtmlSaveOptions.NavigationMapLevel property

EPUB, MOBI veya AZW3 biçimlerine aktarırken gezinme haritasına doldurulacak başlıkların maksimum düzeyini belirtir. Varsayılan değer`3` .

```csharp
public int NavigationMapLevel { get; set; }
```

## Notlar

Gezinme haritası, kullanıcı aracılarının belge yapısı içinde gezinmek için kolay bir yol sağlamasını sağlar. Genellikle gezinme noktaları belgedeki başlıklara karşılık gelir. Başlıkları bir üst seviyeye kadar doldurmak için**N** bu değeri atayın`NavigationMapLevel`.

Varsayılan olarak, üç düzeyde başlık doldurulur: stil paragrafları**Başlık 1** ,**Başlık 2** ve**Başlık 3**. Bu özelliği, karşılık gelen maksimum seviyeyi talep etmek için 1 ile 9 arasında bir değere ayarlayabilirsiniz. Bunu sıfıra ayarlamak, gezinme haritasını yalnızca belge köküne veya belge parçalarının köklerine indirger.

## Örnekler

Azw3 belgeleri için içerik tablosunun nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Big document.docx");

HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.Azw3);
options.NavigationMapLevel = 2;

doc.Save(ArtifactsDir + "HtmlSaveOptions.CreateAZW3Toc.azw3", options);
```

Mobi belgeleri için içerik tablosunun nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Big document.docx");

HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.Mobi);
options.NavigationMapLevel = 5;

doc.Save(ArtifactsDir + "HtmlSaveOptions.CreateMobiToc.mobi", options);
```

Kaydedilmiş bir Epub belgesinin gezinme panelinde görünen başlıkların nasıl filtreleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// "Başlık" stilini kullanarak biçimlendirdiğimiz her paragraf başlık görevi görebilir.
// Her başlığın, başlık stilinin numarasına göre belirlenen bir başlık düzeyi de olabilir.
// Aşağıdaki başlıklar 1-3 seviyelerine aittir.
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

// Epub okuyucuları genellikle belgeleri için bir içindekiler tablosu oluştururlar.
// Belgede "Başlık" stili olan her paragraf, bu içerik tablosunda bir giriş oluşturacaktır.
 // Maksimum başlık seviyesini belirlemek için "NavigationMapLevel" özelliğini kullanabiliriz.
// Epub okuyucusu içerik tablosuna belirttiğimiz düzeyin üstündeki başlıkları eklemeyecektir.
HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.Epub);
options.NavigationMapLevel = 2;

// Belgemizde altı başlık var, bunlardan ikisi 2. seviyenin üstünde.
// Bu belgenin içindekiler tablosunda dört giriş olacak.
doc.Save(ArtifactsDir + "HtmlSaveOptions.EpubHeadings.epub", options);
```

### Ayrıca bakınız

* class [HtmlSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
