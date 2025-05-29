---
title: CompressionLevel Enum
linktitle: CompressionLevel
articleTitle: CompressionLevel
second_title: .NET için Aspose.Words
description: OOXML dosya boyutlarını optimize etmek, belge işlemede performansı ve verimliliği artırmak için Aspose.Words.Saving.CompressionLevel enum'unu keşfedin.
type: docs
weight: 5610
url: /tr/net/aspose.words.saving/compressionlevel/
---
## CompressionLevel enumeration

OOXML dosyaları için sıkıştırma düzeyi.

(DOCX ve DOTX dosyaları dahili olarak bir ZIP arşividir, bu özellik arşivin sıkıştırma seviyesini kontrol eder.

FlatOpc dosyasının bir ZIP arşivi olmadığını ve bu nedenle bu özelliğin FlatOpc dosyalarını etkilemediğini unutmayın.)

```csharp
public enum CompressionLevel
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Normal | `0` | Normal sıkıştırma seviyesi. Aspose.Words tarafından kullanılan varsayılan sıkıştırma seviyesi. |
| Maximum | `1` | Maksimum sıkıştırma seviyesi. |
| Fast | `2` | Hızlı sıkıştırma seviyesi. |
| SuperFast | `3` | Süper Hızlı sıkıştırma seviyesi. Microsoft Word bu sıkıştırma seviyesini kullanır. |

## Örnekler

Bir OOXML belgesini kaydederken kullanılacak sıkıştırma düzeyinin nasıl belirleneceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Big document.docx");

// Belgeyi OOXML biçiminde kaydettiğimizde, bir OoxmlSaveOptions nesnesi oluşturabiliriz
// ve ardından belgenin nasıl kaydedileceğini değiştirmek için bunu belgenin kaydetme yöntemine geçiriyoruz.
// En güçlü ve en yavaş sıkıştırmayı uygulamak için "CompressionLevel" özelliğini "CompressionLevel.Maximum" olarak ayarlayın.
// Uygulamak için "CompressionLevel" özelliğini "CompressionLevel.Normal" olarak ayarlayın
// Aspose.Words'ün OOXML belgelerini kaydederken kullandığı varsayılan sıkıştırma.
// Daha hızlı ve daha zayıf bir sıkıştırma uygulamak için "CompressionLevel" özelliğini "CompressionLevel.Fast" olarak ayarlayın.
// Uygulamak için "CompressionLevel" özelliğini "CompressionLevel.SuperFast" olarak ayarlayın
// Microsoft Word'ün kullandığı varsayılan sıkıştırma.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(SaveFormat.Docx);
saveOptions.CompressionLevel = compressionLevel;

Stopwatch st = Stopwatch.StartNew();
doc.Save(ArtifactsDir + "OoxmlSaveOptions.DocumentCompression.docx", saveOptions);
st.Stop();

FileInfo fileInfo = new FileInfo(ArtifactsDir + "OoxmlSaveOptions.DocumentCompression.docx");

Console.WriteLine($"Saving operation done using the \"{compressionLevel}\" compression level:");
Console.WriteLine($"\tDuration:\t{st.ElapsedMilliseconds} ms");
Console.WriteLine($"\tFile Size:\t{fileInfo.Length} bytes");
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Saving](../../aspose.words.saving/)
* toplantı [Aspose.Words](../../)
