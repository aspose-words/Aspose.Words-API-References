---
title: CompositeNode.RemoveChild
linktitle: RemoveChild
articleTitle: RemoveChild
second_title: Aspose.Words for .NET
description: CompositeNode RemoveChild yöntem. Belirtilen alt düğümü kaldırır C#'da.
type: docs
weight: 170
url: /tr/net/aspose.words/compositenode/removechild/
---
## CompositeNode.RemoveChild method

Belirtilen alt düğümü kaldırır.

```csharp
public Node RemoveChild(Node oldChild)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| oldChild | Node | Kaldırılacak düğüm. |

### Geri dönüş değeri

Kaldırılan düğüm.

## Notlar

ebeveyni*oldChild* ayarlandı`hükümsüz` düğüm çıkarıldıktan sonra.

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

// Bir bölümü, başka bir bölümle olan kardeş ilişkisine göre kaldırın.
if (lastSection.PreviousSibling != null)
    doc.RemoveChild(firstSection);

// Kaldırdığımız bölüm ilk bölümdü, belgede yalnızca ikinci bölüm kaldı.
Assert.AreEqual("Section 2 text.", doc.GetText().Trim());
```

### Ayrıca bakınız

* class [Node](../../node/)
* class [CompositeNode](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
