---
title: TxtSaveOptions.AddBidiMarks
linktitle: AddBidiMarks
articleTitle: AddBidiMarks
second_title: .NET için Aspose.Words
description: TxtSaveOptions AddBidiMarks özelliğinin, daha iyi okunabilirlik ve biçimlendirme için çift yönlü işaretler ekleyerek düz metin dışa aktarımlarını nasıl geliştirdiğini keşfedin.
type: docs
weight: 20
url: /tr/net/aspose.words.saving/txtsaveoptions/addbidimarks/
---
## TxtSaveOptions.AddBidiMarks property

Düz metin biçiminde dışa aktarırken her BiDi çalışmasından önce çift yönlü işaretlerin eklenip eklenmeyeceğini belirtir.

Varsayılan değer:`YANLIŞ`.

```csharp
public bool AddBidiMarks { get; set; }
```

## Örnekler

Her iki yönlü metin çalıştırmadan önce Unicode Karakteri 'SAĞDAN SOL İŞARETİ'nin (U+200F) nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");
builder.ParagraphFormat.Bidi = true;
builder.Writeln("שלום עולם!");
builder.Writeln("مرحبا بالعالم!");

// Belgenin "Kaydet" metoduna geçirebileceğimiz bir "TxtSaveOptions" nesnesi oluşturun
// Belgeyi düz metne nasıl kaydedeceğimizi değiştirmek için.
TxtSaveOptions saveOptions = new TxtSaveOptions { Encoding = System.Text.Encoding.Unicode};

// Çalışmalardan önce işaretler eklemek için "AddBidiMarks" özelliğini "true" olarak ayarlayın
// gerçeği belirtmek için sağdan sola metinle.
// Tümünü soldan sağa yazmak için "AddBidiMarks" özelliğini "false" olarak ayarlayın
// ve sağdan sola doğru eşit olarak ilerler, hangisinin hangisi olduğunu gösterecek hiçbir şey yoktur.
saveOptions.AddBidiMarks = addBidiMarks;

doc.Save(ArtifactsDir + "TxtSaveOptions.AddBidiMarks.txt", saveOptions);

string docText = System.Text.Encoding.Unicode.GetString(File.ReadAllBytes(ArtifactsDir + "TxtSaveOptions.AddBidiMarks.txt"));

if (addBidiMarks)
{
    Assert.AreEqual("\uFEFFHello world!‎\r\nשלום עולם!‏\r\nمرحبا بالعالم!‏\r\n\r\n", docText);
    Assert.True(docText.Contains("\u200f"));
}
else
{
    Assert.AreEqual("\uFEFFHello world!\r\nשלום עולם!\r\nمرحبا بالعالم!\r\n\r\n", docText);
    Assert.False(docText.Contains("\u200f"));
}
```

### Ayrıca bakınız

* class [TxtSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
