---
title: HtmlSaveOptions.ExportPageMargins
second_title: Aspose.Words for .NET API Referansı
description: HtmlSaveOptions mülk. Sayfa kenar boşluklarının HTMLye mi MHTMLye mi yoksa EPUBa mı aktarılacağını belirtir. VarsayılanYANLIŞ .
type: docs
weight: 210
url: /tr/net/aspose.words.saving/htmlsaveoptions/exportpagemargins/
---
## HtmlSaveOptions.ExportPageMargins property

Sayfa kenar boşluklarının HTML'ye mi, MHTML'ye mi yoksa EPUB'a mı aktarılacağını belirtir. Varsayılan:`YANLIŞ` .

```csharp
public bool ExportPageMargins { get; set; }
```

### Notlar

Aspose.Words varsayılan olarak sayfa kenar boşluklarının alanını göstermez. Herhangi bir öğe belgenin kenarı tarafından tamamen veya kısmen kırpılmışsa, görüntülenen alan bu seçenekle genişletilebilir.

### Örnekler

Çıkış HTML belgelerinde sınırların dışındaki nesnelerin nasıl gösterileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Sarma olmadan bir şekil eklemek için bir oluşturucu kullanın.
Shape shape = builder.InsertShape(ShapeType.Cube, 200, 200);

shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.WrapType = WrapType.None;

// Negatif şekil konumu değerleri, şekli sayfa sınırlarının dışına yerleştirebilir.
// Bunu HTML'ye aktarırsak şekil kesik görünecektir.
shape.Left = -150;

// Belgeyi HTML'ye kaydederken bir SaveOptions nesnesi iletebiliriz
// sayfanın sınırların dışındaki nesneleri tam olarak görüntüleyecek şekilde ayarlanıp ayarlanmayacağına karar vermek için.
// "ExportPageMargins" bayrağını "true" olarak ayarlarsak, şekil çıktı HTML'sinde tamamen görünür olacaktır.
// "ExportPageMargins" bayrağını "false" olarak ayarlarsak,
// belgemiz şekli Microsoft Word'de gördüğümüz gibi kesilmiş olarak görüntüleyecektir.
HtmlSaveOptions options = new HtmlSaveOptions { ExportPageMargins = exportPageMargins };

doc.Save(ArtifactsDir + "HtmlSaveOptions.ExportPageMargins.html", options);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.ExportPageMargins.html");

if (exportPageMargins)
{
    Assert.True(outDocContents.Contains("<style type=\"text/css\">div.Section_1 { margin:70.85pt }</style>"));
    Assert.True(outDocContents.Contains("<div class=\"Section_1\"><p style=\"margin-top:0pt; margin-left:150pt; margin-bottom:0pt\">"));
}
else
{
    Assert.False(outDocContents.Contains("style type=\"text/css\">"));
    Assert.True(outDocContents.Contains("<div><p style=\"margin-top:0pt; margin-left:220.85pt; margin-bottom:0pt\">"));
}
```

### Ayrıca bakınız

* class [HtmlSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../htmlsaveoptions/)
* toplantı [Aspose.Words](../../../)


