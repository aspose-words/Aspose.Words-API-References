---
title: BlockImportMode Enum
linktitle: BlockImportMode
articleTitle: BlockImportMode
second_title: .NET için Aspose.Words
description: Aspose.Words.BlockImportMode enum'unun, sorunsuz iş akışları için blok düzeyindeki öğe özelliği içe aktarımlarını optimize ederek HTML belge entegrasyonunu nasıl geliştirdiğini keşfedin.
type: docs
weight: 4010
url: /tr/net/aspose.words.loading/blockimportmode/
---
## BlockImportMode enumeration

Blok düzeyindeki öğelerin özelliklerinin HTML tabanlı belgelerden nasıl içe aktarılacağını belirtir.

```csharp
public enum BlockImportMode
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Merge | `0` | Üst blokların özellikleri birleştirilir ve alt öğelerde (yani paragraflar veya tablolar) saklanır. |
| Preserve | `1` | Üst blokların özellikleri özel bir mantıksal yapıya aktarılır ve belge düğümlerinden ayrı olarak saklanır. |

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

* ad alanı [Aspose.Words.Loading](../../aspose.words.loading/)
* toplantı [Aspose.Words](../../)
