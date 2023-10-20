---
title: HtmlFixedSaveOptions.ExportFormFields
linktitle: ExportFormFields
articleTitle: ExportFormFields
second_title: Aspose.Words for .NET
description: HtmlFixedSaveOptions ExportFormFields mülk. Form alanlarının metne veya grafiklere dönüştürülmek yerine interaktif öğeleri giriş etiketi olarak olarak dışa aktarılıp aktarılmadığına ilişkin göstergeyi alır veya ayarlar C#'da.
type: docs
weight: 80
url: /tr/net/aspose.words.saving/htmlfixedsaveoptions/exportformfields/
---
## HtmlFixedSaveOptions.ExportFormFields property

Form alanlarının metne veya grafiklere dönüştürülmek yerine, interaktif öğeleri ('giriş' etiketi olarak) olarak dışa aktarılıp aktarılmadığına ilişkin göstergeyi alır veya ayarlar.

```csharp
public bool ExportFormFields { get; set; }
```

## Örnekler

Form alanlarının Html'ye nasıl aktarılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertCheckBox("CheckBox", false, 15);

// Form alanları içeren bir belgeyi .html'ye aktardığımızda,
// Aspose.Words'ün form alanlarını dışa aktarmasının iki yolu vardır.
// "ExportFormFields" bayrağını "true" olarak ayarlamak, bunları etkileşimli nesneler olarak dışa aktaracaktır.
// Bu bayrağın "false" olarak ayarlanması form alanlarını düz metin olarak görüntüleyecektir.
// Bu onları mevcut değerlerinde donduracak ve HTML belgemizin okuyucusunu engelleyecektir
// onlarla etkileşime girebilmekten.
HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions
{
    ExportFormFields = exportFormFields
};

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.ExportFormFields.html", htmlFixedSaveOptions);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlFixedSaveOptions.ExportFormFields.html");

if (exportFormFields)
{
    Assert.True(Regex.Match(outDocContents,
        "<a name=\"CheckBox\" style=\"left:0pt; top:0pt;\"></a>" +
        "<input style=\"position:absolute; left:0pt; top:0pt;\" type=\"checkbox\" name=\"CheckBox\" />").Success);
}
else
{
    Assert.True(Regex.Match(outDocContents, 
        "<a name=\"CheckBox\" style=\"left:0pt; top:0pt;\"></a>" +
        "<div class=\"awdiv\" style=\"left:0.8pt; top:0.8pt; width:14.25pt; height:14.25pt; border:solid 0.75pt #000000;\"").Success);
}
```

### Ayrıca bakınız

* class [HtmlFixedSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
