---
title: FieldCollection Class
linktitle: FieldCollection
articleTitle: FieldCollection
second_title: Aspose.Words for .NET
description: Aspose.Words.Fields.FieldCollection sınıf. Bir koleksiyonField belirtilen aralıktaki alanları temsil eden nesneler C#'da.
type: docs
weight: 1690
url: /tr/net/aspose.words.fields/fieldcollection/
---
## FieldCollection class

Bir koleksiyon[`Field`](../field/) belirtilen aralıktaki alanları temsil eden nesneler.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Alanlarla Çalışmak](https://docs.aspose.com/words/net/working-with-fields/) dokümantasyon makalesi.

```csharp
public class FieldCollection : IEnumerable<Field>
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Count](../../aspose.words.fields/fieldcollection/count/) { get; } | Koleksiyondaki alanların sayısını döndürür. |
| [Item](../../aspose.words.fields/fieldcollection/item/) { get; } | Belirtilen dizindeki bir alanı döndürür. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [Clear](../../aspose.words.fields/fieldcollection/clear/)() | Bu koleksiyondaki tüm alanları belgeden ve bu koleksiyonun kendisinden kaldırır. |
| [GetEnumerator](../../aspose.words.fields/fieldcollection/getenumerator/)() | Bir numaralandırıcı nesnesini döndürür. |
| [Remove](../../aspose.words.fields/fieldcollection/remove/)(*[Field](../field/)*) | Belirtilen alanı bu koleksiyondan ve belgeden kaldırır. |
| [RemoveAt](../../aspose.words.fields/fieldcollection/removeat/)(*int*) | Belirtilen dizindeki bir alanı bu koleksiyondan ve belgeden kaldırır. |

## Notlar

Bu koleksiyonun bir örneği, belirtilen aralıkta başlayan alanları yineler.

`FieldCollection` koleksiyon, içerdiği alanlara sahip değildir; yalnızca alanlardan oluşan bir seçimdir.

`FieldCollection` koleksiyon "canlıdır", yani oluşturulduğu object düğümünün alt öğelerinde yapılan değişiklikler, koleksiyon tarafından döndürülen alanlara anında yansıtılır.`FieldCollection` özellikleri ve yöntemleri.

## Örnekler

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

// Aşağıda alanları bir alan koleksiyonundan kaldırmanın dört yolu verilmiştir.
// 1 - Kendini kaldıracak bir alan edinin:
fields[0].Remove();
Assert.AreEqual(5, fields.Count);

// 2 - Kaldırma yöntemine ilettiğimiz bir alanı kaldırmak için koleksiyonu alın:
Field lastField = fields[3];
fields.Remove(lastField);
Assert.AreEqual(4, fields.Count);

// 3 - Bir dizindeki koleksiyondan bir alanı kaldırın:
fields.RemoveAt(2);
Assert.AreEqual(3, fields.Count);

// 4 - Koleksiyondaki tüm alanları tek seferde kaldırın:
fields.Clear();
Assert.AreEqual(0, fields.Count);
```

Bir alan koleksiyonuyla nasıl çalışılacağını gösterir.

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

    // Alan koleksiyonu üzerinde yineleme yapın ve içerikleri yazdırıp yazın
    // özel bir ziyaretçi uygulaması kullanarak her alanın.
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
/// Alan bilgilerini yazdıran ziyaretçi uygulamasını belgeleyin.
/// </summary>
public class FieldVisitor : DocumentVisitor
{
    public FieldVisitor()
    {
        mBuilder = new StringBuilder();
    }

    /// <summary>
    /// Ziyaretçinin biriktirdiği belgenin düz metnini alır.
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
    /// Belgede FieldSeparator düğümüyle karşılaşıldığında çağrılır.
    /// </summary>
    public override VisitorAction VisitFieldSeparator(FieldSeparator fieldSeparator)
    {
        mBuilder.AppendLine("\tFound separator: " + fieldSeparator.GetText());

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Belgede FieldEnd düğümüyle karşılaşıldığında çağrılır.
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
