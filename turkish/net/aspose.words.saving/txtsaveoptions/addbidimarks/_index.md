---
title: TxtSaveOptions.AddBidiMarks
linktitle: AddBidiMarks
articleTitle: AddBidiMarks
second_title: Aspose.Words for .NET
description: TxtSaveOptions AddBidiMarks mülk. Düz metin biçiminde dışa aktarırken her BiDi çalıştırmadan önce çift yönlü işaretlerin eklenip eklenmeyeceğini belirtir C#'da.
type: docs
weight: 20
url: /tr/net/aspose.words.saving/txtsaveoptions/addbidimarks/
---
## TxtSaveOptions.AddBidiMarks property

Düz metin biçiminde dışa aktarırken her BiDi çalıştırmadan önce çift yönlü işaretlerin eklenip eklenmeyeceğini belirtir.

Varsayılan değer:`YANLIŞ`.

```csharp
public bool AddBidiMarks { get; set; }
```

## Örnekler

Metindeki her çift yönlü Çalıştırma'dan önce 'SAĞDAN SOL İŞARETİ' (U+200F) Unicode Karakterinin nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");
builder.ParagraphFormat.Bidi = true;
builder.Writeln("שלום עולם!");
builder.Writeln("مرحبا بالعالم!");

// Belgenin "Save" yöntemine aktarabileceğimiz bir "TxtSaveOptions" nesnesi oluşturun
// belgeyi düz metne kaydetme şeklimizi değiştirmek için.
TxtSaveOptions saveOptions = new TxtSaveOptions { Encoding = System.Text.Encoding.Unicode};

// Çalıştırmadan önce işaret eklemek için "AddBidiMarks" özelliğini "true" olarak ayarlayın
// gerçeği belirtmek için sağdan sola metinle.
// Tümünü soldan sağa yazmak için "AddBidiMarks" özelliğini "false" olarak ayarlayın
// ve sağdan sola eşit şekilde çalışır ve hangisinin hangisi olduğunu belirtecek hiçbir şey yoktur.
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
