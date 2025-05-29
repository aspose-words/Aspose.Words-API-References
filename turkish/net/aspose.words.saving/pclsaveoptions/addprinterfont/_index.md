---
title: PclSaveOptions.AddPrinterFont
linktitle: AddPrinterFont
articleTitle: AddPrinterFont
second_title: .NET için Aspose.Words
description: Gelişmiş baskı performansı için üreticilerden gelen yazıcı yazı tiplerini verimli bir şekilde yüklemek ve yönetmek amacıyla PclSaveOptions AddPrinterFont yöntemini keşfedin.
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
| fontFullName | String | Yazı tipinin tam adı (örneğin "Times New Roman Bold Italic"). |
| fontPclName | String | Pcl belgesinde kullanılan yazı tipinin adı. |

## Notlar

Pcl spesifikasyonuna göre herhangi bir yazıcıda bulunması gereken 52 adet font vardır. Ancak üreticiler cihazlarına başka fontlar da ekleyebilirler.

## Örnekler

Bir yazıcının belirli bir yazı tipinin tüm örneklerini farklı bir yazı tipiyle nasıl değiştireceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Courier";
builder.Write("Hello world!");

PclSaveOptions saveOptions = new PclSaveOptions();
saveOptions.AddPrinterFont("Courier New", "Courier");

// Bu belgeyi yazdırırken yazıcı "Courier New" yazı tipini kullanacaktır
// Belgemizin "Courier" yazı tipini kullandığı yerlere erişmek için.
doc.Save(ArtifactsDir + "PclSaveOptions.AddPrinterFont.pcl", saveOptions);
```

### Ayrıca bakınız

* class [PclSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
