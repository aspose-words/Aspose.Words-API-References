---
title: Document.EnsureMinimum
linktitle: EnsureMinimum
articleTitle: EnsureMinimum
second_title: .NET için Aspose.Words
description: Belgelerde otomatik olarak bölüm ve paragraf oluşturmak, eksiksiz ve düzenli içerik sağlamak için EnsureMinimum yöntemini nasıl kullanacağınızı öğrenin.
type: docs
weight: 620
url: /tr/net/aspose.words/document/ensureminimum/
---
## Document.EnsureMinimum method

Belgede bölüm yoksa, bir paragraf içeren bir bölüm oluşturur.

```csharp
public void EnsureMinimum()
```

## Örnekler

Bir belgenin içeriğini düzenlemek için gereken minimum düğüm kümesini içermesinin nasıl sağlanacağını gösterir.

```csharp
// Yeni oluşturulan bir belge, bir alt Bölüm, bir alt Bölüm de bir alt Bölüm olmak üzere toplam 1 alt Bölüm ve bir alt Bölüm de toplam 1 alt Bölüm olmak üzere toplam 1 alt Bölüm ve ...
// Belge gövdesinin içeriğini, o paragrafa Çalıştırmalar veya satır içi Şekiller gibi düğümler ekleyerek düzenleyebiliriz.
Document doc = new Document();
NodeCollection nodes = doc.GetChildNodes(NodeType.Any, true);

Assert.AreEqual(NodeType.Section, nodes[0].NodeType);
Assert.AreEqual(doc, nodes[0].ParentNode);

Assert.AreEqual(NodeType.Body, nodes[1].NodeType);
Assert.AreEqual(nodes[0], nodes[1].ParentNode);

Assert.AreEqual(NodeType.Paragraph, nodes[2].NodeType);
Assert.AreEqual(nodes[1], nodes[2].ParentNode);

// Bu, belgeyi düzenleyebilmemiz için ihtiyaç duyduğumuz minimum düğüm kümesidir.
// Bunlardan herhangi birini kaldırırsak belgeyi artık düzenleyemeyiz.
doc.RemoveAllChildren();

Assert.AreEqual(0, doc.GetChildNodes(NodeType.Any, true).Count);

// Belgenin en azından bu üç düğüme sahip olduğundan emin olmak için bu yöntemi çağırın, böylece belgeyi tekrar düzenleyebiliriz.
doc.EnsureMinimum();

Assert.AreEqual(NodeType.Section, nodes[0].NodeType);
Assert.AreEqual(NodeType.Body, nodes[1].NodeType);
Assert.AreEqual(NodeType.Paragraph, nodes[2].NodeType);

((Paragraph)nodes[2]).Runs.Add(new Run(doc, "Hello world!"));
```

### Ayrıca bakınız

* class [Document](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
