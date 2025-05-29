---
title: CompositeNode.RemoveChild
linktitle: RemoveChild
articleTitle: RemoveChild
second_title: .NET için Aspose.Words
description: Gelişmiş performans ve verimlilik için düğüm kaldırma işlemini kolaylaştırmak üzere tasarlanan RemoveChild yöntemi ile CompositeNode'unuzu zahmetsizce yönetin.
type: docs
weight: 190
url: /tr/net/aspose.words/compositenode/removechild/
---
## CompositeNode.RemoveChild&lt;T&gt; method

Belirtilen alt düğümü kaldırır.

```csharp
public T RemoveChild<T>(T oldChild)
    where T : Node
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| oldChild | T | Kaldırılacak düğüm. |

### Geri dönüş değeri

Kaldırılan düğüm.

## Notlar

Ebeveyni*oldChild* ayarlandı`hükümsüz` düğüm kaldırıldıktan sonra.

## Örnekler

Belgedeki son bölümden önceki bölümü kaldırmak için Node ve CompositeNode yöntemlerinin nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Section 1 text.");
builder.InsertBreak(BreakType.SectionBreakContinuous);
builder.Writeln("Section 2 text.");

// Her iki bölüm de birbirinin kardeşidir.
Section lastSection = (Section)doc.LastChild;
Section firstSection = (Section)lastSection.PreviousSibling;

// Bir bölümü, başka bir bölümle olan kardeş ilişkisine göre kaldır.
if (lastSection.PreviousSibling != null)
    doc.RemoveChild(firstSection);

// Kaldırdığımız bölüm ilk bölümdü, belgede sadece ikinci bölüm kaldı.
Assert.AreEqual("Section 2 text.", doc.GetText().Trim());
```

### Ayrıca bakınız

* class [Node](../../node/)
* class [CompositeNode](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
