---
title: FieldEQ.AsOfficeMath
linktitle: AsOfficeMath
articleTitle: AsOfficeMath
second_title: .NET için Aspose.Words
description: EQ alanlarını FieldEQ'nun AsOfficeMath yöntemi ile dönüştürerek sorunsuz belge entegrasyonu için bunları zahmetsizce Office Math nesnelerine dönüştürün.
type: docs
weight: 20
url: /tr/net/aspose.words.fields/fieldeq/asofficemath/
---
## FieldEQ.AsOfficeMath method

EQ alanına karşılık gelen Office Math nesnesini döndürür.

```csharp
public OfficeMath AsOfficeMath()
```

### Geri dönüş değeri

Geri Döndürür`hükümsüz` eğer alan kodu boş veya geçersizse, aksi takdirde[`OfficeMath`](../../../aspose.words.math/officemath/) örnek.

## Örnekler

EQ alanının Office Math ile nasıl değiştirileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Field sample - EQ.docx");
FieldEQ fieldEQ = doc.Range.Fields.OfType<FieldEQ>().First();

OfficeMath officeMath = fieldEQ.AsOfficeMath();

fieldEQ.Start.ParentNode.InsertBefore(officeMath, fieldEQ.Start);
fieldEQ.Remove();

doc.Save(ArtifactsDir + "Field.EQAsOfficeMath.docx");
```

### Ayrıca bakınız

* class [OfficeMath](../../../aspose.words.math/officemath/)
* class [FieldEQ](../)
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)
