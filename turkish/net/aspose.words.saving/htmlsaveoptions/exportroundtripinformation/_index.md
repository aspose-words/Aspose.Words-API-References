---
title: HtmlSaveOptions.ExportRoundtripInformation
linktitle: ExportRoundtripInformation
articleTitle: ExportRoundtripInformation
second_title: .NET için Aspose.Words
description: HTML, MHTML ve EPUB formatlarındaki gidiş dönüş verilerini kontrol etmek için HtmlSaveOptions' ExportRoundtripInformation özelliğini keşfedin. Bugün ihracatlarınızı optimize edin!
type: docs
weight: 240
url: /tr/net/aspose.words.saving/htmlsaveoptions/exportroundtripinformation/
---
## HtmlSaveOptions.ExportRoundtripInformation property

HTML, MHTML veya EPUB'a kaydederken gidiş-dönüş bilgilerinin yazılıp yazılmayacağını belirtir. Varsayılan değer`doğru` HTML ve için`YANLIŞ` MHTML ve EPUB için.

```csharp
public bool ExportRoundtripInformation { get; set; }
```

## Notlar

Gidiş-dönüş bilgilerinin kaydedilmesi, HTML belgelerinin bir belgeye geri yüklenmesi sırasında sekme durakları, yorumlar, üstbilgiler ve altbilgiler gibi belge özelliklerinin geri yüklenmesine olanak tanır.[`Document`](../../../aspose.words/document/) nesne.

Ne zaman`doğru`, gidiş dönüş bilgileri, karşılık gelen HTML öğelerinin -aw-* CSS properties biçiminde dışa aktarılır.

Ne zaman`YANLIŞ`, üretilen dosyalara gidiş dönüş bilgisinin çıktı olarak verilmesine neden olmaz.

## Örnekler

.html'ye dönüştürürken gizli öğelerin nasıl korunacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Bir belgeyi .html'ye dönüştürürken gizli yer imleri, orijinal şekil konumları gibi bazı öğeler,
// veya dipnotlar ya kaldırılacak ya da düz metne dönüştürülecek ve etkili bir şekilde kaybolacaktır.
// ExportRoundtripInformation değeri true olarak ayarlanmış bir HtmlSaveOptions nesnesiyle kaydetmek bu öğeleri koruyacaktır.

// Belgeyi HTML'e kaydettiğimizde, SaveOptions nesnesini belirlemek için bir SaveOptions nesnesi geçirebiliriz.
// kaydetme işleminin HTML'nin desteklemediği veya kullanmadığı belge öğelerini nasıl dışa aktaracağı,
// gizli yer imleri ve orijinal şekil konumları gibi.
// "ExportRoundtripInformation" bayrağını "true" olarak ayarlarsak, kaydetme işlemi bu öğeleri koruyacaktır.
// "ExportRoundTripInformation" bayrağını "false" olarak ayarlarsak, kaydetme işlemi bu öğeleri atacaktır.
// Kaydedilen HTML'yi Aspose.Words kullanarak yüklemeyi planlıyorsak bu tür öğeleri korumak isteyeceğiz.
// bir kez daha işe yarayabilirler.
HtmlSaveOptions options = new HtmlSaveOptions { ExportRoundtripInformation = exportRoundtripInformation };

doc.Save(ArtifactsDir + "HtmlSaveOptions.RoundTripInformation.html", options);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.RoundTripInformation.html");
doc = new Document(ArtifactsDir + "HtmlSaveOptions.RoundTripInformation.html");

if (exportRoundtripInformation)
{
    Assert.True(outDocContents.Contains("<div style=\"-aw-headerfooter-type:header-primary; clear:both\">"));
    Assert.True(outDocContents.Contains("<span style=\"-aw-import:ignore\">&#xa0;</span>"));

    Assert.True(outDocContents.Contains(
        "td colspan=\"2\" style=\"width:210.6pt; border-style:solid; border-width:0.75pt 6pt 0.75pt 0.75pt; " +
        "padding-right:2.4pt; padding-left:5.03pt; vertical-align:top; " +
        "-aw-border-bottom:0.5pt single; -aw-border-left:0.5pt single; -aw-border-top:0.5pt single\">"));

    Assert.True(outDocContents.Contains(
        "<li style=\"margin-left:30.2pt; padding-left:5.8pt; -aw-font-family:'Courier New'; -aw-font-weight:normal; -aw-number-format:'o'\">"));

    Assert.True(outDocContents.Contains(
        "<img src=\"HtmlSaveOptions.RoundTripInformation.003.jpeg\" width=\"350\" height=\"180\" alt=\"\" " +
        "style=\"-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline\" />"));

    Assert.True(outDocContents.Contains(
        "<span>Page number </span>" +
        "<span style=\"-aw-field-start:true\"></span>" +
        "<span style=\"-aw-field-code:' PAGE   \\\\* MERGEFORMAT '\"></span>" +
        "<span style=\"-aw-field-separator:true\"></span>" +
        "<span>1</span>" +
        "<span style=\"-aw-field-end:true\"></span>"));

    Assert.AreEqual(1, doc.Range.Fields.Count(f => f.Type == FieldType.FieldPage));
}
else
{
    Assert.True(outDocContents.Contains("<div style=\"clear:both\">"));
    Assert.True(outDocContents.Contains("<span>&#xa0;</span>"));

    Assert.True(outDocContents.Contains(
        "<td colspan=\"2\" style=\"width:210.6pt; border-style:solid; border-width:0.75pt 6pt 0.75pt 0.75pt; " +
        "padding-right:2.4pt; padding-left:5.03pt; vertical-align:top\">"));

    Assert.True(outDocContents.Contains(
        "<li style=\"margin-left:30.2pt; padding-left:5.8pt\">"));

    Assert.True(outDocContents.Contains(
        "<img src=\"HtmlSaveOptions.RoundTripInformation.003.jpeg\" width=\"350\" height=\"180\" alt=\"\" />"));

    Assert.True(outDocContents.Contains(
        "<span>Page number 1</span>"));

    Assert.AreEqual(0, doc.Range.Fields.Count(f => f.Type == FieldType.FieldPage));
}
```

### Ayrıca bakınız

* class [HtmlSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
