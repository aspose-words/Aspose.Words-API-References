---
title: EditableRange.Id
linktitle: Id
articleTitle: Id
second_title: .NET için Aspose.Words
description: EditableRange Id özelliğini keşfedin, gelişmiş belge denetimi ve verimlilik için düzenlenebilir aralık tanımlayıcılarınıza kolayca erişin ve bunları yönetin.
type: docs
weight: 40
url: /tr/net/aspose.words/editablerange/id/
---
## EditableRange.Id property

Düzenlenebilir aralık tanımlayıcısını alır.

```csharp
public int Id { get; }
```

## Notlar

Bölge, aşağıdaki şekilde sınırlandırılmalıdır:[`EditableRangeStart`](../editablerangestart/) Ve[`EditableRangeEnd`](../editablerangeend/)

Düzenlenebilir aralık tanımlayıcılarının bir belge boyunca benzersiz olması gerekir ve Aspose.Words, belgeleri yüklerken, kaydederken ve birleştirirken düzenlenebilir aralık tanımlayıcılarını otomatik olarak korur.

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

* class [EditableRange](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
