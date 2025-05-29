---
title: CompositeNode.LastChild
linktitle: LastChild
articleTitle: LastChild
second_title: .NET için Aspose.Words
description: Son alt düğüme kolayca erişmek ve onu düzenlemek için CompositeNode LastChild özelliğini keşfedin; böylece veri yapınızın yönetimini geliştirin.
type: docs
weight: 50
url: /tr/net/aspose.words/compositenode/lastchild/
---
## CompositeNode.LastChild property

Düğümün son çocuğunu alır.

```csharp
public Node LastChild { get; }
```

## Notlar

Son alt düğüm yoksa,`hükümsüz` döndürülür.

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
