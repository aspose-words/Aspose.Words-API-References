---
title: HtmlSaveOptions.ExportRoundtripInformation
second_title: Aspose.Words for .NET API Referansı
description: HtmlSaveOptions mülk. HTML MHTML veya EPUBa kaydederken gidiş dönüş bilgilerinin yazıp yazılmayacağını belirtir. Varsayılan değerdoğru HTML için veyanlış MHTML ve EPUB için.
type: docs
weight: 250
url: /tr/net/aspose.words.saving/htmlsaveoptions/exportroundtripinformation/
---
## HtmlSaveOptions.ExportRoundtripInformation property

HTML, MHTML veya EPUB'a kaydederken gidiş dönüş bilgilerinin yazıp yazılmayacağını belirtir. Varsayılan değer`doğru` HTML için ve`yanlış` MHTML ve EPUB için.

```csharp
public bool ExportRoundtripInformation { get; set; }
```

### Notlar

Gidiş dönüş bilgilerinin kaydedilmesi, HTML belgelerinin bir dosyaya geri yüklenmesi sırasında sekme durakları, yorumlar, üstbilgiler ve altbilgiler gibi belge özelliklerinin geri yüklenmesini sağlar.[`Document`](../../../aspose.words/document/) nesne.

Ne zaman`doğru`, gidiş dönüş bilgileri, karşılık gelen HTML öğelerinin -aw-* CSS özellikleri olarak dışa aktarılır.

Ne zaman`yanlış`, üretilen dosyalara hiçbir gidiş dönüş bilgisinin çıktılanmasına neden olmaz.

### Örnekler

.html'ye dönüştürürken gizli öğelerin nasıl korunacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Bir belgeyi .html'ye dönüştürürken, gizli yer imleri, orijinal şekil konumları gibi bazı öğeler,
// veya dipnotlar kaldırılacak veya düz metne dönüştürülecek ve etkin bir şekilde kaybolacaktır.
// ExportRoundtripInformation true olarak ayarlanmış bir HtmlSaveOptions nesnesiyle kaydetmek, bu öğeleri koruyacaktır.

// Belgeyi HTML'ye kaydettiğimizde, belirlemek için bir SaveOptions nesnesi iletebiliriz.
// kaydetme işleminin HTML'nin desteklemediği veya kullanmadığı belge öğelerini nasıl dışa aktaracağı,
// gizli yer imleri ve orijinal şekil konumları gibi.
// "ExportRoundtripInformation" bayrağını "true" olarak ayarlarsak, kaydetme işlemi bu öğeleri koruyacaktır.
// "ExportRoundTripInformation" bayrağını "false" olarak ayarlarsak, kaydetme işlemi bu öğeleri atacaktır.
// Kaydedilmiş HTML'yi Aspose.Words kullanarak yüklemek istiyorsak, bu tür öğeleri korumak isteyeceğiz,
// bir kez daha işe yarayabilecekleri için.
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
* ad alanı [Aspose.Words.Saving](../../htmlsaveoptions/)
* toplantı [Aspose.Words](../../../)


