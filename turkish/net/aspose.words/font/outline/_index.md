---
title: Font.Outline
linktitle: Outline
articleTitle: Outline
second_title: .NET için Aspose.Words
description: Font Outline özelliğini keşfedin. Benzersiz bir tasarım dokunuşu için fontları kolayca ana hatlar olarak biçimlendirin. Bu basit özellik ile tipografinizi geliştirin!
type: docs
weight: 300
url: /tr/net/aspose.words/font/outline/
---
## Font.Outline property

Yazı tipi anahat olarak biçimlendirilmişse doğrudur.

```csharp
public bool Outline { get; set; }
```

## Örnekler

Anahat biçiminde biçimlendirilmiş bir metin çalışmasının nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Metnin dolgu rengini beyaza değiştirmek için Anahat bayrağını ayarlayın ve
 // Her karakterin etrafında metnin orijinal renginde ince bir dış çizgi bırakın.
builder.Font.Outline = true;
builder.Font.Color = Color.Blue;
builder.Font.Size = 36;

builder.Writeln("This text has an outline.");

doc.Save(ArtifactsDir + "Font.Outline.docx");
```

### Ayrıca bakınız

* class [Font](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
