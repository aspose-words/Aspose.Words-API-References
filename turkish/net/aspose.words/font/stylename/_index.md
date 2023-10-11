---
title: Font.StyleName
second_title: Aspose.Words for .NET API Referansı
description: Font mülk. Bu biçimlendirmeye uygulanan karakter stilinin adını alır veya ayarlar.
type: docs
weight: 420
url: /tr/net/aspose.words/font/stylename/
---
## Font.StyleName property

Bu biçimlendirmeye uygulanan karakter stilinin adını alır veya ayarlar.

```csharp
public string StyleName { get; set; }
```

### Örnekler

Mevcut metnin stilinin nasıl değiştirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Aşağıda stillere referans vermenin iki yolu verilmiştir.
// 1 - Stil adının kullanılması:
builder.Font.StyleName = "Emphasis";
builder.Writeln("Text originally in \"Emphasis\" style");

// 2 - Yerleşik bir stil tanımlayıcı kullanma:
builder.Font.StyleIdentifier = StyleIdentifier.IntenseEmphasis;
builder.Writeln("Text originally in \"Intense Emphasis\" style");

// Bir stilin tüm kullanımlarını diğerine dönüştürün,
// eski ve yeni stillere referans vermek için yukarıdaki yöntemleri kullanıyoruz.
foreach (Run run in doc.GetChildNodes(NodeType.Run, true).OfType<Run>())
{
    if (run.Font.StyleName == "Emphasis")
        run.Font.StyleName = "Strong";

    if (run.Font.StyleIdentifier == StyleIdentifier.IntenseEmphasis)
        run.Font.StyleIdentifier = StyleIdentifier.Strong;
}

doc.Save(ArtifactsDir + "Font.ChangeStyle.docx");
```

### Ayrıca bakınız

* class [Font](../)
* ad alanı [Aspose.Words](../../font/)
* toplantı [Aspose.Words](../../../)


