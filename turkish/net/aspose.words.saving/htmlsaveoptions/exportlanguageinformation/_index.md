---
title: HtmlSaveOptions.ExportLanguageInformation
linktitle: ExportLanguageInformation
articleTitle: ExportLanguageInformation
second_title: .NET için Aspose.Words
description: HtmlSaveOptions ile HTML, MHTML veya EPUB'da dil dışa aktarımını kontrol edin. Belge erişilebilirliğini artırın ve daha geniş bir kitleye zahmetsizce ulaşın.
type: docs
weight: 180
url: /tr/net/aspose.words.saving/htmlsaveoptions/exportlanguageinformation/
---
## HtmlSaveOptions.ExportLanguageInformation property

Dil bilgilerinin HTML, MHTML veya EPUB'a aktarılıp aktarılmayacağını belirtir. Varsayılan`YANLIŞ` .

```csharp
public bool ExportLanguageInformation { get; set; }
```

## Notlar

Bu özellik şu şekilde ayarlandığında:`doğru` Aspose.Words çıktıları**dil**Dili belirten document öğelerindeki HTML niteliği. Bu, dil ile ilgili semantiği korumak için gerekli olabilir.

## Örnekler

.html'ye kaydederken dil bilgilerinin nasıl korunacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Metni farklı yerel ayarlarda biçimlendirirken yazmak için oluşturucuyu kullanın.
builder.Font.LocaleId = new CultureInfo("en-US").LCID;
builder.Writeln("Hello world!");

builder.Font.LocaleId = new CultureInfo("en-GB").LCID;
builder.Writeln("Hello again!");

builder.Font.LocaleId = new CultureInfo("ru-RU").LCID;
builder.Write("Привет, мир!");

// Belgeyi HTML'e kaydederken SaveOptions nesnesini geçirebiliriz
// her biçimlendirilmiş metnin yerel ayarlarını korumak veya silmek için.
// "ExportLanguageInformation" bayrağını "true" olarak ayarlarsak,
// Çıktı HTML belgesi, <span> etiketlerinin "lang" özniteliklerindeki yerel ayarları içerecektir.
// "ExportLanguageInformation" bayrağını "false" olarak ayarlarsak,
// Çıktı HTML belgesindeki metin herhangi bir yerel bilgi içermeyecektir.
HtmlSaveOptions options = new HtmlSaveOptions
{
    ExportLanguageInformation = exportLanguageInformation,
    PrettyFormat = true
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.ExportLanguageInformation.html", options);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.ExportLanguageInformation.html");

if (exportLanguageInformation)
{
    Assert.True(outDocContents.Contains("<span>Hello world!</span>"));
    Assert.True(outDocContents.Contains("<span lang=\"en-GB\">Hello again!</span>"));
    Assert.True(outDocContents.Contains("<span lang=\"ru-RU\">Привет, мир!</span>"));
}
else
{
    Assert.True(outDocContents.Contains("<span>Hello world!</span>"));
    Assert.True(outDocContents.Contains("<span>Hello again!</span>"));
    Assert.True(outDocContents.Contains("<span>Привет, мир!</span>"));
}
```

### Ayrıca bakınız

* class [HtmlSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
