---
title: Font.ComplexScript
linktitle: ComplexScript
articleTitle: ComplexScript
second_title: Aspose.Words for .NET
description: Font ComplexScript mülk. Bu çalıştırmanın formatını belirlerken Unicode karakter değerlerinden bağımsız olarak bu çalıştırmanın içeriğinin karmaşık komut dosyası metni olarak değerlendirilip değerlendirilmeyeceğini belirtir C#'da.
type: docs
weight: 80
url: /tr/net/aspose.words/font/complexscript/
---
## Font.ComplexScript property

Bu çalıştırmanın formatını belirlerken Unicode karakter değerlerinden bağımsız olarak bu çalıştırmanın içeriğinin karmaşık komut dosyası metni olarak değerlendirilip değerlendirilmeyeceğini belirtir.

```csharp
public bool ComplexScript { get; set; }
```

## Örnekler

Her zaman karmaşık komut dosyası olarak değerlendirilen metnin nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.ComplexScript = true;

builder.Writeln("Text treated as complex script.");

doc.Save(ArtifactsDir + "Font.ComplexScript.docx");
```

### Ayrıca bakınız

* class [Font](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
