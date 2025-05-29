---
title: BuiltInDocumentProperties.ScaleCrop
linktitle: ScaleCrop
articleTitle: ScaleCrop
second_title: .NET için Aspose.Words
description: Küçük resim görüntüsünü kontrol eden ve kırpılmış veya ölçeklenmiş görüntülerde en iyi görüntülemeyi sağlayan BuiltInDocumentProperties'deki ScaleCrop özelliğini keşfedin.
type: docs
weight: 260
url: /tr/net/aspose.words.properties/builtindocumentproperties/scalecrop/
---
## BuiltInDocumentProperties.ScaleCrop property

Belge küçük resminin kırpılıp kırpılmayacağını veya ekrana sığacak şekilde ölçeklenip ölçeklenmeyeceğini belirtir.

```csharp
public bool ScaleCrop { get; }
```

## Notlar

Aspose.Words bu özelliği güncellemez.

## Örnekler

Genişletilmiş özelliklerin nasıl alınacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Extended properties.docx");
Assert.IsTrue(doc.BuiltInDocumentProperties.ScaleCrop);
Assert.IsTrue(doc.BuiltInDocumentProperties.SharedDocument);
Assert.IsTrue(doc.BuiltInDocumentProperties.HyperlinksChanged);
```

### Ayrıca bakınız

* class [BuiltInDocumentProperties](../)
* ad alanı [Aspose.Words.Properties](../../../aspose.words.properties/)
* toplantı [Aspose.Words](../../../)
