---
title: Field.Unlink
linktitle: Unlink
articleTitle: Unlink
second_title: .NET için Aspose.Words
description: Alanların bağlantısını zahmetsizce kaldırmak, veri yönetiminizi geliştirmek ve en iyi sonuçlar için iş akışınızı kolaylaştırmak için Alan Bağlantısını Kaldırma yöntemini keşfedin.
type: docs
weight: 130
url: /tr/net/aspose.words.fields/field/unlink/
---
## Field.Unlink method

Alan bağlantısını kaldırma işlemini gerçekleştirir.

```csharp
public bool Unlink()
```

### Geri dönüş değeri

`doğru` eğer alan bağlantısı kaldırılmışsa, aksi takdirde`YANLIŞ` .

## Notlar

Alanı en son sonuçla değiştirir.

XE (Dizin Girişi) alanları ve SEQ (Sıra) alanları gibi bazı alanların bağlantısı kaldırılamaz.

## Örnekler

Bir alanın bağlantısının nasıl kaldırılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Linked fields.docx");
doc.Range.Fields[1].Unlink();
```

### Ayrıca bakınız

* class [Field](../)
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)
