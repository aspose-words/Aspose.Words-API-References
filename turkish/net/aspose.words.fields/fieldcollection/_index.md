---
title: FieldCollection Class
linktitle: FieldCollection
articleTitle: FieldCollection
second_title: .NET için Aspose.Words
description: Belirtilen belge aralıkları içindeki Alan nesnelerini yönetmek ve belge otomasyonunuzu geliştirmek için güçlü bir sınıf olan Aspose.Words.FieldCollection'ı keşfedin.
type: docs
weight: 2100
url: /tr/net/aspose.words.fields/fieldcollection/
---
## FieldCollection class

Bir koleksiyon[`Field`](../field/) belirtilen aralıktaki alanları temsil eden nesneler.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Alanlarla Çalışma](https://docs.aspose.com/words/net/working-with-fields/) belgeleme makalesi.

```csharp
public class FieldCollection : IEnumerable<Field>
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Count](../../aspose.words.fields/fieldcollection/count/) { get; } | Koleksiyondaki alanların sayısını döndürür. |
| [Item](../../aspose.words.fields/fieldcollection/item/) { get; } | Belirtilen dizinde bir alan döndürür. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [Clear](../../aspose.words.fields/fieldcollection/clear/)() | Bu koleksiyonun tüm alanlarını belgeden ve bu koleksiyonun kendisinden kaldırır. |
| [GetEnumerator](../../aspose.words.fields/fieldcollection/getenumerator/)() | Bir numaralandırıcı nesnesi döndürür. |
| [Remove](../../aspose.words.fields/fieldcollection/remove/)(*[Field](../field/)*) | Belirtilen alanı bu koleksiyondan ve belgeden kaldırır. |
| [RemoveAt](../../aspose.words.fields/fieldcollection/removeat/)(*int*) | Belirtilen dizindeki bir alanı bu koleksiyondan ve belgeden kaldırır. |

## Notlar

Bu koleksiyonun bir örneği, belirtilen aralıkta başlayan alanları yineler.

The`FieldCollection` koleksiyon, içerdiği alanlara sahip değildir, yalnızca alanların bir seçimidir.

The`FieldCollection` koleksiyon "canlıdır", yani oluşturulduğu object düğümünün çocuklarında yapılan değişiklikler, tarafından döndürülen alanlara hemen yansıtılır`FieldCollection` özellikleri ve yöntemleri.

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

Alan koleksiyonlarıyla nasıl çalışılacağını gösterir.

```csharp
public void FieldCollection()
{
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

    // Alan koleksiyonu üzerinde yineleme yapın ve içerikleri ve türü yazdırın
    // her alanın özel ziyaretçi uygulamasını kullanarak.
    FieldVisitor fieldVisitor = new FieldVisitor();

    using (IEnumerator<Field> fieldEnumerator = fields.GetEnumerator())
    {
        while (fieldEnumerator.MoveNext())
        {
            if (fieldEnumerator.Current != null)
            {
                fieldEnumerator.Current.Start.Accept(fieldVisitor);
                fieldEnumerator.Current.Separator?.Accept(fieldVisitor);
                fieldEnumerator.Current.End.Accept(fieldVisitor);
            }
            else
            {
                Console.WriteLine("There are no fields in the document.");
            }
        }
    }

    Console.WriteLine(fieldVisitor.GetText());
}

/// <summary>
/// Alan bilgilerini yazdıran belge ziyaretçisi uygulaması.
/// </summary>
public class FieldVisitor : DocumentVisitor
{
    public FieldVisitor()
    {
        mBuilder = new StringBuilder();
    }

    /// <summary>
    /// Ziyaretçinin topladığı belgenin düz metnini alır.
    /// </summary>
    public string GetText()
    {
        return mBuilder.ToString();
    }

    /// <summary>
    /// Belgede bir FieldStart düğümüyle karşılaşıldığında çağrılır.
    /// </summary>
    public override VisitorAction VisitFieldStart(FieldStart fieldStart)
    {
        mBuilder.AppendLine("Found field: " + fieldStart.FieldType);
        mBuilder.AppendLine("\tField code: " + fieldStart.GetField().GetFieldCode());
        mBuilder.AppendLine("\tDisplayed as: " + fieldStart.GetField().Result);

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Belgede bir FieldSeparator düğümüyle karşılaşıldığında çağrılır.
    /// </summary>
    public override VisitorAction VisitFieldSeparator(FieldSeparator fieldSeparator)
    {
        mBuilder.AppendLine("\tFound separator: " + fieldSeparator.GetText());

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Belgede bir FieldEnd düğümüyle karşılaşıldığında çağrılır.
    /// </summary>
    public override VisitorAction VisitFieldEnd(FieldEnd fieldEnd)
    {
        mBuilder.AppendLine("End of field: " + fieldEnd.FieldType);

        return VisitorAction.Continue;
    }

    private readonly StringBuilder mBuilder;
}
```

### Ayrıca bakınız

* class [Field](../field/)
* ad alanı [Aspose.Words.Fields](../../aspose.words.fields/)
* toplantı [Aspose.Words](../../)
