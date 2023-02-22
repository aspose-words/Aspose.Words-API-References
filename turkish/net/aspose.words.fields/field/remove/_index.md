---
title: Field.Remove
second_title: Aspose.Words for .NET API Referansı
description: Field yöntem. Alanı belgeden kaldırır. Alandan hemen sonra bir düğüm döndürür. Alanın sonu üst düğümünün son çocuğu ise üst paragrafını döndürür. Alan zaten kaldırılmışsa döner hükümsüz .
type: docs
weight: 120
url: /tr/net/aspose.words.fields/field/remove/
---
## Field.Remove method

Alanı belgeden kaldırır. Alandan hemen sonra bir düğüm döndürür. Alanın sonu, üst düğümünün son çocuğu ise, üst paragrafını döndürür. Alan zaten kaldırılmışsa, döner **hükümsüz** .

```csharp
public Node Remove()
```

### Örnekler

Alan koleksiyonundan alanların nasıl kaldırılacağını gösterir.

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

// Bir alan koleksiyonundan alanları kaldırmanın dört yolu aşağıdadır.
// 1 - Kendisini kaldırmak için bir alan alın:
fields[0].Remove();
Assert.AreEqual(5, fields.Count);

// 2 - Kaldırma yöntemine ilettiğimiz bir alanı kaldırmak için koleksiyonu alın:
Field lastField = fields[3];
fields.Remove(lastField);
Assert.AreEqual(4, fields.Count);

// 3 - Bir dizindeki koleksiyondan bir alanı kaldırın:
fields.RemoveAt(2);
Assert.AreEqual(3, fields.Count);

// 4 - Koleksiyondaki tüm alanları bir kerede kaldırın:
fields.Clear();
Assert.AreEqual(0, fields.Count);
```

ÖZEL alanların nasıl işleneceğini gösterir.

```csharp
{
    // .docx formatına çevirdiğimiz Corel WordPerfect belgesini açın.
    Document doc = new Document(MyDir + "Field sample - PRIVATE.docx");

    // Yüklediğimiz gibi WordPerfect 5.x/6.x belgeleri ÖZEL alanlar içerebilir.
    // Microsoft Word, yükleme/kaydetme işlemleri sırasında ÖZEL alanları korur,
    // ama onlar için hiçbir işlevsellik sağlamaz.
    FieldPrivate field = (FieldPrivate)doc.Range.Fields[0];

    Assert.AreEqual(" PRIVATE \"My value\" ", field.GetFieldCode());
    Assert.AreEqual(FieldType.FieldPrivate, field.Type);

    // Belge oluşturucu kullanarak ÖZEL alanlar da ekleyebiliriz.
    DocumentBuilder builder = new DocumentBuilder(doc);
    builder.InsertField(FieldType.FieldPrivate, true);

    // Bu alanlar, hassas bilgileri korumanın uygun bir yolu değildir.
    // WordPerfect'in eski sürümleriyle geriye dönük uyumluluk gerekli olmadıkça,
    // bu alanları güvenle kaldırabiliriz. Bunu bir DocumentVisiitor uygulaması kullanarak yapabiliriz.
    Assert.AreEqual(2, doc.Range.Fields.Count);

    FieldPrivateRemover remover = new FieldPrivateRemover();
    doc.Accept(remover);

    Assert.AreEqual(2, remover.GetFieldsRemovedCount());
    Assert.AreEqual(0, doc.Range.Fields.Count);
}

/// <summary>
/// Karşılaşılan tüm ÖZEL alanları kaldırır.
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
    /// Düğüm bir ÖZEL alana aitse, tüm alan kaldırılır.
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
* ad alanı [Aspose.Words.Fields](../../field/)
* toplantı [Aspose.Words](../../../)


