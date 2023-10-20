---
title: Field.Unlink
linktitle: Unlink
articleTitle: Unlink
second_title: Aspose.Words for .NET
description: Field Unlink yöntem. Alanın bağlantısını kaldırır C#'da.
type: docs
weight: 130
url: /tr/net/aspose.words.fields/field/unlink/
---
## Field.Unlink method

Alanın bağlantısını kaldırır.

```csharp
public bool Unlink()
```

### Geri dönüş değeri

`doğru` alanın bağlantısı kaldırılmışsa, aksi halde`YANLIŞ` .

## Notlar

Alanı en son sonucuyla değiştirir.

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
