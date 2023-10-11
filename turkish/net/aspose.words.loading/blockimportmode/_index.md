---
title: Enum BlockImportMode
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Loading.BlockImportMode Sıralama. Blok düzeyindeki öğelerin özelliklerinin HTML tabanlı belgelerden nasıl içe aktarıldığını belirtir.
type: docs
weight: 3560
url: /tr/net/aspose.words.loading/blockimportmode/
---
## BlockImportMode enumeration

Blok düzeyindeki öğelerin özelliklerinin HTML tabanlı belgelerden nasıl içe aktarıldığını belirtir.

```csharp
public enum BlockImportMode
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Merge | `0` | Ana blokların özellikleri birleştirilir ve alt öğelerde (örn. paragraflar veya tablolar) saklanır. |
| Preserve | `1` | Ana blokların özellikleri özel bir mantıksal yapıya aktarılır ve belge düğümlerinden ayrı olarak depolanır. |

### Örnekler

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
// HTML blok düzeyindeki öğelerin içe aktarılmasının yeni modunu ayarlayın.
loadOptions.BlockImportMode = blockImportMode;

Document doc = new Document(stream, loadOptions);
doc.Save(ArtifactsDir + "HtmlLoadOptions.BlockImport.docx");
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Loading](../../aspose.words.loading/)
* toplantı [Aspose.Words](../../)


