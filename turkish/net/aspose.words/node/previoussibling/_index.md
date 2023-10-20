---
title: Node.PreviousSibling
linktitle: PreviousSibling
articleTitle: PreviousSibling
second_title: Aspose.Words for .NET
description: Node PreviousSibling mülk. Bu düğümden hemen önceki düğümü alır C#'da.
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

Önceki düğüm yoksa, bir`hükümsüz` döndürülür.

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

* class [Node](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
