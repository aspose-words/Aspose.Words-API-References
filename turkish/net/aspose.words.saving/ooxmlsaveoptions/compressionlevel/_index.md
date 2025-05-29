---
title: OoxmlSaveOptions.CompressionLevel
linktitle: CompressionLevel
articleTitle: CompressionLevel
second_title: .NET için Aspose.Words
description: Gelişmiş performans için özelleştirilebilir sıkıştırma düzeyleriyle belge kaydetmeyi optimize etmek amacıyla OoxmlSaveOptions CompressionLevel özelliğini keşfedin.
type: docs
weight: 30
url: /tr/net/aspose.words.saving/ooxmlsaveoptions/compressionlevel/
---
## OoxmlSaveOptions.CompressionLevel property

Belgeyi kaydetmek için kullanılan sıkıştırma düzeyini belirtir. Varsayılan değerNormal .

```csharp
public CompressionLevel CompressionLevel { get; set; }
```

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

* enum [CompressionLevel](../../compressionlevel/)
* class [OoxmlSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
