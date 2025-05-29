---
title: HtmlLoadOptions.BlockImportMode
linktitle: BlockImportMode
articleTitle: BlockImportMode
second_title: .NET için Aspose.Words
description: Blok düzeyindeki öğe içe aktarımlarını özelleştirmek için HtmlLoadOptions' BlockImportMode özelliğini keşfedin. En iyi içerik yönetimi için birleştirmeyi kontrol edin!
type: docs
weight: 20
url: /tr/net/aspose.words.loading/htmlloadoptions/blockimportmode/
---
## HtmlLoadOptions.BlockImportMode property

Blok düzeyindeki öğelerin özelliklerinin nasıl içe aktarılacağını belirten bir değeri alır veya ayarlar. Varsayılan değerMerge .

```csharp
public BlockImportMode BlockImportMode { get; set; }
```

## Örnekler

Blok düzeyindeki öğelerin özelliklerinin HTML tabanlı belgelerden nasıl içe aktarıldığını gösterir.

```csharp
const string html = @"
<html>
    <div style='border:dotted'>
        <div style='border:solid'>
            <p>paragraph 1</p>
            <p>paragraph 2</p>
        </div>
    </div>
</html>";
MemoryStream stream = new MemoryStream(Encoding.UTF8.GetBytes(html));

HtmlLoadOptions loadOptions = new HtmlLoadOptions();
// HTML blok düzeyindeki öğelerin içe aktarılması için yeni modu ayarlayın.
loadOptions.BlockImportMode = blockImportMode;

Document doc = new Document(stream, loadOptions);
doc.Save(ArtifactsDir + "HtmlLoadOptions.BlockImport.docx");
```

### Ayrıca bakınız

* enum [BlockImportMode](../../blockimportmode/)
* class [HtmlLoadOptions](../)
* ad alanı [Aspose.Words.Loading](../../../aspose.words.loading/)
* toplantı [Aspose.Words](../../../)
