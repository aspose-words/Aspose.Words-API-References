---
title: BuiltInDocumentProperties.SharedDocument
linktitle: SharedDocument
articleTitle: SharedDocument
second_title: .NET için Aspose.Words
description: Belgenizin paylaşılıp paylaşılmadığını ortaya çıkaran, iş birliğini ve erişilebilirliği artıran BuiltInDocumentProperties SharedDocument özelliğini keşfedin.
type: docs
weight: 280
url: /tr/net/aspose.words.properties/builtindocumentproperties/shareddocument/
---
## BuiltInDocumentProperties.SharedDocument property

Belgenin paylaşılan bir belge olup olmadığını belirtir.

```csharp
public bool SharedDocument { get; }
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
