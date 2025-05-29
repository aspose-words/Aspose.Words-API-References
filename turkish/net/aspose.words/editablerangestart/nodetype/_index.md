---
title: EditableRangeStart.NodeType
linktitle: NodeType
articleTitle: NodeType
second_title: .NET için Aspose.Words
description: EditableRangeStart NodeType özelliğini keşfedin; kusursuz aralık yönetimi ve iyileştirilmiş kullanıcı deneyimiyle belge düzenlemenizi geliştirin!
type: docs
weight: 30
url: /tr/net/aspose.words/editablerangestart/nodetype/
---
## EditableRangeStart.NodeType property

Geri DöndürürEditableRangeStart .

```csharp
public override NodeType NodeType { get; }
```

## Örnekler

Düzenlenebilir bir aralıkla nasıl çalışılacağını gösterir.

```csharp
Document doc = new Document();
doc.Protect(ProtectionType.ReadOnly, "MyPassword");

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world! Since we have set the document's protection level to read-only," +
                " we cannot edit this paragraph without the password.");

// Düzenlenebilir aralıklar, korunan belgelerin bazı bölümlerini düzenlemeye açık bırakmamıza olanak tanır.
EditableRangeStart editableRangeStart = builder.StartEditableRange();
builder.Writeln("This paragraph is inside an editable range, and can be edited.");
EditableRangeEnd editableRangeEnd = builder.EndEditableRange();

// İyi oluşturulmuş bir düzenlenebilir aralığın bir başlangıç düğümü ve bir bitiş düğümü vardır.
// Bu düğümlerin eşleşen kimlikleri vardır ve düzenlenebilir düğümleri kapsar.
EditableRange editableRange = editableRangeStart.EditableRange;

Assert.AreEqual(editableRangeStart.Id, editableRange.Id);
Assert.AreEqual(editableRangeEnd.Id, editableRange.Id);

// Düzenlenebilir aralığın farklı bölümleri birbirine bağlanır.
Assert.AreEqual(editableRangeStart.Id, editableRange.EditableRangeStart.Id);
Assert.AreEqual(editableRangeStart.Id, editableRangeEnd.EditableRangeStart.Id);
Assert.AreEqual(editableRange.Id, editableRangeStart.EditableRange.Id);
Assert.AreEqual(editableRangeEnd.Id, editableRange.EditableRangeEnd.Id);

// Her bir parçanın düğüm tiplerine şu şekilde erişebiliriz. Düzenlenebilir aralık kendi başına bir düğüm değildir,
// fakat bir başlangıç, bir son ve bunların içerdiği içeriklerden oluşan bir varlık.
Assert.AreEqual(NodeType.EditableRangeStart, editableRangeStart.NodeType);
Assert.AreEqual(NodeType.EditableRangeEnd, editableRangeEnd.NodeType);

builder.Writeln("This paragraph is outside the editable range, and cannot be edited.");

doc.Save(ArtifactsDir + "EditableRange.CreateAndRemove.docx");

// Düzenlenebilir bir aralığı kaldır. Aralığın içindeki tüm düğümler bozulmadan kalacaktır.
editableRange.Remove();
```

### Ayrıca bakınız

* enum [NodeType](../../nodetype/)
* class [EditableRangeStart](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
