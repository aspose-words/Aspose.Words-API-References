---
title: PclSaveOptions.AddPrinterFont
second_title: Aspose.Words for .NET API Referansı
description: PclSaveOptions yöntem. Üretici tarafından yazıcıya yüklenen yazı tipi hakkında bilgi ekler.
type: docs
weight: 50
url: /tr/net/aspose.words.saving/pclsaveoptions/addprinterfont/
---
## PclSaveOptions.AddPrinterFont method

Üretici tarafından yazıcıya yüklenen yazı tipi hakkında bilgi ekler.

```csharp
public void AddPrinterFont(string fontFullName, string fontPclName)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| fontFullName | String | Yazı tipinin tam adı (örn. "Times New Roman Kalın İtalik"). |
| fontPclName | String | Pcl belgesinde kullanılan yazı tipinin adı. |

### Notlar

Pcl spesifikasyonuna göre herhangi bir yazıcıda yerleşik olarak bulunması gereken 52 yazı tipi vardır. Ancak üreticiler cihazlarına başka yazı tipleri de ekleyebilirler.

### Örnekler

Belirli bir yazı tipinin tüm örneklerini farklı bir yazı tipiyle değiştirmek için yazıcının nasıl alınacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Courier";
builder.Write("Hello world!");

PclSaveOptions saveOptions = new PclSaveOptions();
saveOptions.AddPrinterFont("Courier New", "Courier");

// Bu belgeyi yazdırırken yazıcı "Courier New" yazı tipini kullanacaktır
// belgemizin "Courier" yazı tipini kullandığı yerlere erişmek için.
doc.Save(ArtifactsDir + "PclSaveOptions.AddPrinterFont.pcl", saveOptions);
```

### Ayrıca bakınız

* class [PclSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../pclsaveoptions/)
* toplantı [Aspose.Words](../../../)


