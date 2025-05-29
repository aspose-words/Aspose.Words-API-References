---
title: Field.IsDirty
linktitle: IsDirty
articleTitle: IsDirty
second_title: .NET için Aspose.Words
description: Alan verilerinizin doğru ve güncel kalmasını sağlamak, belge bütünlüğünü ve performansı artırmak için IsDirty özelliğini yönetin.
type: docs
weight: 40
url: /tr/net/aspose.words.fields/field/isdirty/
---
## Field.IsDirty property

Belgede yapılan diğer değişiklikler nedeniyle alanın geçerli sonucunun artık doğru (eski) olup olmadığını alır veya ayarlar.

```csharp
public bool IsDirty { get; set; }
```

## Örnekler

Alan sonucunu güncellemek için özel özelliğin nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Belgenin yerleşik "Yazar" özelliğine değer verin ve ardından bunu bir alanla görüntüleyin.
doc.BuiltInDocumentProperties.Author = "John Doe";
FieldAuthor field = (FieldAuthor)builder.InsertField(FieldType.FieldAuthor, true);

Assert.False(field.IsDirty);
Assert.AreEqual("John Doe", field.Result);

// Özelliği güncelle. Alan hala eski değeri gösteriyor.
doc.BuiltInDocumentProperties.Author = "John & Jane Doe";

Assert.AreEqual("John Doe", field.Result);

// Alanın değeri güncel olmadığından "kirli" olarak işaretleyebiliriz.
// Bu değer, alanı Field.Update() metoduyla manuel olarak güncelleyene kadar güncelliğini yitirecektir.
field.IsDirty = true;

using (MemoryStream docStream = new MemoryStream())
{
    // Bir güncelleme metodunu çağırmadan kaydedersek,
    // alan, çıktı belgesinde güncel olmayan değeri görüntülemeye devam edecektir.
    doc.Save(docStream, SaveFormat.Docx);

    // LoadOptions nesnesinin tüm alanları güncelleme seçeneği vardır
    // Belge yüklenirken "kirli" olarak işaretlendi.
    LoadOptions options = new LoadOptions();
    options.UpdateDirtyFields = updateDirtyFields;
    doc = new Document(docStream, options);

    Assert.AreEqual("John & Jane Doe", doc.BuiltInDocumentProperties.Author);

    field = (FieldAuthor)doc.Range.Fields[0];

    // Kirli alanların bu şekilde güncellenmesi, otomatik olarak "IsDirty" bayrağını false olarak ayarlar.
    if (updateDirtyFields)
    {
        Assert.AreEqual("John & Jane Doe", field.Result);
        Assert.False(field.IsDirty);
    }
    else
    {
        Assert.AreEqual("John Doe", field.Result);
        Assert.True(field.IsDirty);
    }
}
```

### Ayrıca bakınız

* class [Field](../)
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)
