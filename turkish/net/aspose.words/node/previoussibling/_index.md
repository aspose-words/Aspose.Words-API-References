---
title: Node.PreviousSibling
linktitle: PreviousSibling
articleTitle: PreviousSibling
second_title: .NET için Aspose.Words
description: Mevcut düğümünüzden önce gelen düğüme kolayca erişmek için Node PreviousSibling özelliğini keşfedin ve DOM manipülasyon becerilerinizi geliştirin.
type: docs
weight: 70
url: /tr/net/aspose.words/node/previoussibling/
---
## Node.PreviousSibling property

Bu düğümden hemen önceki düğümü alır.

```csharp
public Node PreviousSibling { get; }
```

## Notlar

Eğer öncesinde bir düğüm yoksa,`hükümsüz` döndürülür.

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

* class [Node](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
