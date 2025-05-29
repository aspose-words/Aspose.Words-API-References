---
title: Field.Remove
linktitle: Remove
articleTitle: Remove
second_title: .NET için Aspose.Words
description: Alanları Alan Kaldırma yöntemiyle belgelerden zahmetsizce kaldırın. Kesin düğüm dönüşleri alın ve boş alanları sorunsuz bir şekilde işleyin. İş akışınızı optimize edin!
type: docs
weight: 120
url: /tr/net/aspose.words.fields/field/remove/
---
## Field.Remove method

Alanı belgeden kaldırır. Alanın hemen ardından bir düğüm döndürür. Alanın sonu, üst düğümünün son alt 'siyse, üst paragrafını döndürür. Alan zaten kaldırılmışsa, şunu döndürür`hükümsüz` .

```csharp
public Node Remove()
```

## Örnekler

Bir alan koleksiyonundan alanların nasıl kaldırılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertField(" DATE \\@ \"dddd, d MMMM yyyy\" ");
builder.InsertField(" TIME ");
builder.InsertField(" REVNUM ");
builder.InsertField(" AUTHOR  \"John Doe\" ");
builder.InsertField(" SUBJECT \"My Subject\" ");
builder.InsertField(" QUOTE \"Hello world!\" ");
doc.UpdateFields();

FieldCollection fields = doc.Range.Fields;

Assert.AreEqual(6, fields.Count);

// Aşağıda bir alan koleksiyonundan alanları kaldırmanın dört yolu bulunmaktadır.
// 1 - Bir alanın kendisini kaldırmasını sağla:
fields[0].Remove();
Assert.AreEqual(5, fields.Count);

// 2 - Kaldırma yöntemine geçirdiğimiz bir alanı kaldırmak için koleksiyonu edinin:
Field lastField = fields[3];
fields.Remove(lastField);
Assert.AreEqual(4, fields.Count);

// 3 - Bir dizindeki bir koleksiyondan bir alanı kaldır:
fields.RemoveAt(2);
Assert.AreEqual(3, fields.Count);

// 4 - Koleksiyondaki tüm alanları aynı anda kaldır:
fields.Clear();
Assert.AreEqual(0, fields.Count);
```

PRIVATE alanlarının nasıl işleneceğini gösterir.

```csharp
public void FieldPrivate()
{
    // .docx formatına dönüştürdüğümüz Corel WordPerfect belgesini açalım.
    Document doc = new Document(MyDir + "Field sample - PRIVATE.docx");

    // Yüklediğimiz WordPerfect 5.x/6.x belgeleri PRIVATE alanları içerebilir.
    // Microsoft Word, yükleme/kaydetme işlemleri sırasında ÖZEL alanları korur,
    // ancak bunlar için hiçbir işlevsellik sağlamaz.
    FieldPrivate field = (FieldPrivate)doc.Range.Fields[0];

    Assert.AreEqual(" PRIVATE \"My value\" ", field.GetFieldCode());
    Assert.AreEqual(FieldType.FieldPrivate, field.Type);

    // Ayrıca bir belge oluşturucu kullanarak ÖZEL alanlar da ekleyebiliriz.
    DocumentBuilder builder = new DocumentBuilder(doc);
    builder.InsertField(FieldType.FieldPrivate, true);

    // Bu alanlar hassas bilgileri korumak için uygun bir yol değildir.
    // WordPerfect'in eski sürümleriyle geriye dönük uyumluluk şart olmadığı sürece,
    // bu alanları güvenli bir şekilde kaldırabiliriz. Bunu bir DocumentVisiitor uygulaması kullanarak yapabiliriz.
    Assert.AreEqual(2, doc.Range.Fields.Count);

    FieldPrivateRemover remover = new FieldPrivateRemover();
    doc.Accept(remover);

    Assert.AreEqual(2, remover.GetFieldsRemovedCount());
    Assert.AreEqual(0, doc.Range.Fields.Count);
}

/// <summary>
/// Karşılaşılan tüm PRIVATE alanlarını kaldırır.
/// </summary>
public class FieldPrivateRemover : DocumentVisitor
{
    public FieldPrivateRemover()
    {
        mFieldsRemovedCount = 0;
    }

    public int GetFieldsRemovedCount()
    {
        return mFieldsRemovedCount;
    }

    /// <summary>
    /// Belgede bir FieldEnd düğümüyle karşılaşıldığında çağrılır.
    /// Eğer düğüm PRIVATE alanına aitse, tüm alan kaldırılır.
    /// </summary>
    public override VisitorAction VisitFieldEnd(FieldEnd fieldEnd)
    {
        if (fieldEnd.FieldType == FieldType.FieldPrivate)
        {
            fieldEnd.GetField().Remove();
            mFieldsRemovedCount++;
        }

        return VisitorAction.Continue;
    }

    private int mFieldsRemovedCount;
}
```

### Ayrıca bakınız

* class [Node](../../../aspose.words/node/)
* class [Field](../)
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)
