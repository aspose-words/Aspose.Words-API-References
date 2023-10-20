---
title: DocumentBuilder.StartEditableRange
linktitle: StartEditableRange
articleTitle: StartEditableRange
second_title: Aspose.Words for .NET
description: DocumentBuilder StartEditableRange yöntem. Düzenlenebilir aralık başlangıcı olarak belgedeki geçerli konumu işaretler C#'da.
type: docs
weight: 630
url: /tr/net/aspose.words/documentbuilder/starteditablerange/
---
## DocumentBuilder.StartEditableRange method

Düzenlenebilir aralık başlangıcı olarak belgedeki geçerli konumu işaretler.

```csharp
public EditableRangeStart StartEditableRange()
```

### Geri dönüş değeri

Yeni oluşturulan düzenlenebilir aralık başlangıç düğümü.

## Notlar

Bir belgedeki düzenlenebilir aralık herhangi bir aralıkla örtüşebilir ve kapsanabilir. Geçerli bir düzenlenebilir aralık oluşturmak için her ikisini de çağırmanız gerekir`StartEditableRange` Ve[`EndEditableRange`](../endeditablerange/) veya[`EndEditableRange`](../endeditablerange/) yöntemler.

Belge kaydedildiğinde, kötü biçimlendirilmiş düzenlenebilir aralık göz ardı edilecektir.

## Örnekler

İç içe düzenlenebilir aralıkların nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();
doc.Protect(ProtectionType.ReadOnly, "MyPassword");

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world! Since we have set the document's protection level to read-only, " +
                "we cannot edit this paragraph without the password.");

// İç içe geçmiş iki düzenlenebilir aralık oluşturun.
EditableRangeStart outerEditableRangeStart = builder.StartEditableRange();
builder.Writeln("This paragraph inside the outer editable range and can be edited.");

EditableRangeStart innerEditableRangeStart = builder.StartEditableRange();
builder.Writeln("This paragraph inside both the outer and inner editable ranges and can be edited.");

// Şu anda, belge oluşturucunun düğüm ekleme imleci birden fazla devam eden düzenlenebilir aralıktadır.
// Bu durumda düzenlenebilir bir aralığı sonlandırmak istediğimizde,
// EditableRangeStart düğümünü geçerek hangi aralıkları bitirmek istediğimizi belirtmemiz gerekiyor.
builder.EndEditableRange(innerEditableRangeStart);

builder.Writeln("This paragraph inside the outer editable range and can be edited.");

builder.EndEditableRange(outerEditableRangeStart);

builder.Writeln("This paragraph is outside any editable ranges, and cannot be edited.");

// Metnin bir bölgesinde belirtilen gruplarla çakışan iki düzenlenebilir aralık varsa,
// her iki grup tarafından hariç tutulan birleştirilmiş kullanıcı grubunun onu düzenlemesi engellenir.
outerEditableRangeStart.EditableRange.EditorGroup = EditorType.Everyone;
innerEditableRangeStart.EditableRange.EditorGroup = EditorType.Contributors;

doc.Save(ArtifactsDir + "EditableRange.Nested.docx");
```

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

* class [EditableRangeStart](../../editablerangestart/)
* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
