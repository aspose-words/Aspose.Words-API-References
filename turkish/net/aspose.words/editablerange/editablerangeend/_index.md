---
title: EditableRange.EditableRangeEnd
second_title: Aspose.Words for .NET API Referansı
description: EditableRange mülk. Düzenlenebilir aralığın sonunu temsil eden düğümü alır.
type: docs
weight: 10
url: /tr/net/aspose.words/editablerange/editablerangeend/
---
## EditableRange.EditableRangeEnd property

Düzenlenebilir aralığın sonunu temsil eden düğümü alır.

```csharp
public EditableRangeEnd EditableRangeEnd { get; }
```

### Örnekler

Düzenlenebilir bir aralıkla nasıl çalışılacağını gösterir.

```csharp
Document doc = new Document();
doc.Protect(ProtectionType.ReadOnly, "MyPassword");

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world! Since we have set the document's protection level to read-only," +
                " we cannot edit this paragraph without the password.");

// Düzenlenebilir aralıklar, korumalı belgelerin bazı kısımlarını düzenlemeye açık bırakmamıza olanak tanır.
EditableRangeStart editableRangeStart = builder.StartEditableRange();
builder.Writeln("This paragraph is inside an editable range, and can be edited.");
EditableRangeEnd editableRangeEnd = builder.EndEditableRange();

// İyi biçimlendirilmiş düzenlenebilir bir aralığın bir başlangıç düğümü ve bitiş düğümü vardır.
// Bu düğümlerin eşleşen kimlikleri vardır ve düzenlenebilir düğümleri kapsar.
EditableRange editableRange = editableRangeStart.EditableRange;

Assert.AreEqual(editableRangeStart.Id, editableRange.Id);
Assert.AreEqual(editableRangeEnd.Id, editableRange.Id);

// Düzenlenebilir aralığın farklı bölümleri birbirine bağlanır.
Assert.AreEqual(editableRangeStart.Id, editableRange.EditableRangeStart.Id);
Assert.AreEqual(editableRangeStart.Id, editableRangeEnd.EditableRangeStart.Id);
Assert.AreEqual(editableRange.Id, editableRangeStart.EditableRange.Id);
Assert.AreEqual(editableRangeEnd.Id, editableRange.EditableRangeEnd.Id);

// Her parçanın düğüm tiplerine bu şekilde ulaşabiliyoruz. Düzenlenebilir aralığın kendisi bir düğüm değildir,
// ancak bir başlangıç, bir bitiş ve bunların içerdiği içeriklerden oluşan bir varlık.
Assert.AreEqual(NodeType.EditableRangeStart, editableRangeStart.NodeType);
Assert.AreEqual(NodeType.EditableRangeEnd, editableRangeEnd.NodeType);

builder.Writeln("This paragraph is outside the editable range, and cannot be edited.");

doc.Save(ArtifactsDir + "EditableRange.CreateAndRemove.docx");

// Düzenlenebilir bir aralığı kaldırın. Aralık içindeki tüm düğümler bozulmadan kalacaktır.
editableRange.Remove();
```

### Ayrıca bakınız

* class [EditableRangeEnd](../../editablerangeend/)
* class [EditableRange](../)
* ad alanı [Aspose.Words](../../editablerange/)
* toplantı [Aspose.Words](../../../)


