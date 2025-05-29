---
title: Font.ComplexScript
linktitle: ComplexScript
articleTitle: ComplexScript
second_title: .NET için Aspose.Words
description: Unicode değerlerinden bağımsız olarak, metninizin gelişmiş okunabilirlik ve stil için karmaşık bir betik olarak biçimlendirilmesini sağlayan Font ComplexScript özelliğini keşfedin.
type: docs
weight: 80
url: /tr/net/aspose.words/font/complexscript/
---
## Font.ComplexScript property

Bu çalışmanın içeriğinin, bu çalışmanın biçimlendirmesini belirlerken Unicode karakter değerlerinden bağımsız olarak karmaşık betik metni olarak ele alınıp alınmayacağını belirtir.

```csharp
public bool ComplexScript { get; set; }
```

## Örnekler

Her zaman karmaşık bir betik olarak ele alınan metnin nasıl ekleneceğini gösterir.

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
