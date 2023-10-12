---
title: Document.EnsureMinimum
second_title: Aspose.Words for .NET API Referansı
description: Document yöntem. Belgede bölüm yoksa tek paragraflı bir bölüm oluşturur.
type: docs
weight: 600
url: /tr/net/aspose.words/document/ensureminimum/
---
## Document.EnsureMinimum method

Belgede bölüm yoksa, tek paragraflı bir bölüm oluşturur.

```csharp
public void EnsureMinimum()
```

### Örnekler

Bir belgenin, içeriğini düzenlemek için gereken minimum sayıda düğüm kümesini içerdiğinden nasıl emin olunacağını gösterir.

```csharp
// Yeni oluşturulan bir belge, bir alt Gövde ve bir alt Paragraf içeren bir alt Bölüm içerir.
// Belge gövdesinin içeriğini o paragrafa Çalıştırmalar veya satır içi Şekiller gibi düğümler ekleyerek düzenleyebiliriz.
Document doc = new Document();
NodeCollection nodes = doc.GetChildNodes(NodeType.Any, true);

Assert.AreEqual(NodeType.Section, nodes[0].NodeType);
Assert.AreEqual(doc, nodes[0].ParentNode);

Assert.AreEqual(NodeType.Body, nodes[1].NodeType);
Assert.AreEqual(nodes[0], nodes[1].ParentNode);

Assert.AreEqual(NodeType.Paragraph, nodes[2].NodeType);
Assert.AreEqual(nodes[1], nodes[2].ParentNode);

// Bu, belgeyi düzenleyebilmemiz için gereken minimum düğüm kümesidir.
// Bunlardan herhangi birini kaldırırsak artık belgeyi düzenleyemeyiz.
doc.RemoveAllChildren();

Assert.AreEqual(0, doc.GetChildNodes(NodeType.Any, true).Count);

// Belgenin en azından bu üç düğüme sahip olduğundan emin olmak için bu yöntemi çağırın, böylece belgeyi yeniden düzenleyebiliriz.
doc.EnsureMinimum();

Assert.AreEqual(NodeType.Section, nodes[0].NodeType);
Assert.AreEqual(NodeType.Body, nodes[1].NodeType);
Assert.AreEqual(NodeType.Paragraph, nodes[2].NodeType);

((Paragraph)nodes[2]).Runs.Add(new Run(doc, "Hello world!"));
```

### Ayrıca bakınız

* class [Document](../)
* ad alanı [Aspose.Words](../../document/)
* toplantı [Aspose.Words](../../../)


