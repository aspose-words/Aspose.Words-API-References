---
title: DocumentBuilder.StartEditableRange
linktitle: StartEditableRange
articleTitle: StartEditableRange
second_title: .NET için Aspose.Words
description: DocumentBuilder StartEditableRange yönteminin, sorunsuz içerik yönetimi için düzenlenebilir aralık başlangıçlarını işaretleyerek belge düzenlemeyi nasıl geliştirdiğini keşfedin.
type: docs
weight: 670
url: /tr/net/aspose.words/documentbuilder/starteditablerange/
---
## DocumentBuilder.StartEditableRange method

Belgedeki geçerli konumu düzenlenebilir bir aralık başlangıcı olarak işaretler.

```csharp
public EditableRangeStart StartEditableRange()
```

### Geri dönüş değeri

Az önce oluşturulan düzenlenebilir aralık başlangıç düğümü.

## Notlar

Bir belgedeki düzenlenebilir aralık herhangi bir aralığı kapsayabilir ve örtüşebilir. Geçerli bir düzenlenebilir aralık oluşturmak için her ikisini de çağırmanız gerekir `StartEditableRange` Ve[`EndEditableRange`](../endeditablerange/) veya[`EndEditableRange`](../endeditablerange/) Yöntemler.

Kötü oluşturulmuş düzenlenebilir aralık, belge kaydedilirken yok sayılacaktır.

## Örnekler

İç içe düzenlenebilir aralıkların nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();
doc.Protect(ProtectionType.ReadOnly, "MyPassword");

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world! Since we have set the document's protection level to read-only, " +
                "we cannot edit this paragraph without the password.");

// İç içe iki düzenlenebilir aralık oluştur.
EditableRangeStart outerEditableRangeStart = builder.StartEditableRange();
builder.Writeln("This paragraph inside the outer editable range and can be edited.");

EditableRangeStart innerEditableRangeStart = builder.StartEditableRange();
builder.Writeln("This paragraph inside both the outer and inner editable ranges and can be edited.");

// Şu anda, belge oluşturucunun düğüm ekleme imleci birden fazla devam eden düzenlenebilir aralıkta.
// Bu durumda düzenlenebilir bir aralığı sonlandırmak istediğimizde,
// EditableRangeStart düğümünü geçirerek hangi aralıkların sonlandırılmasını istediğimizi belirtmemiz gerekiyor.
builder.EndEditableRange(innerEditableRangeStart);

builder.Writeln("This paragraph inside the outer editable range and can be edited.");

builder.EndEditableRange(outerEditableRangeStart);

builder.Writeln("This paragraph is outside any editable ranges, and cannot be edited.");

// Bir metin bölgesinin belirtilen gruplara sahip iki örtüşen düzenlenebilir aralığı varsa,
// Her iki grup tarafından hariç tutulan kullanıcıların birleşik grubunun bunu düzenlemesi engellenir.
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

* class [EditableRangeStart](../../editablerangestart/)
* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
