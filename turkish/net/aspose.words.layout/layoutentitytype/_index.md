---
title: LayoutEntityType Enum
linktitle: LayoutEntityType
articleTitle: LayoutEntityType
second_title: Aspose.Words for .NET
description: Aspose.Words.Layout.LayoutEntityType Sıralama. Düzen varlıklarının türleri C#'da.
type: docs
weight: 3330
url: /tr/net/aspose.words.layout/layoutentitytype/
---
## LayoutEntityType enumeration

Düzen varlıklarının türleri.

```csharp
[Flags]
public enum LayoutEntityType
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| None | `0` | Varsayılan değer. |
| Page | `1` | Bir belgenin sayfasını temsil eder. Sayfada şunlar olabilir:Column ,HeaderFooter VeComment alt varlıklar. |
| Column | `2` | Bir sayfadaki metnin bir sütununu temsil eder. Sütun, aşağıdaki öğelerle aynı alt öğelere sahip olabilir:Cell , artıFootnote ,Endnote VeNoteSeparator varlıklar. |
| Row | `8` | Bir tablo satırını temsil eder. Satırın sahip olabileceğiCell alt varlıklar olarak. |
| Cell | `10` | Bir tablo hücresini temsil eder. Hücrenin sahip olabileceğiLine VeRow alt varlıklar. |
| Line | `20` | Metin ve satır içi nesnelerin karakter satırını temsil eder. Satırda şunlar olabilir:Span alt varlıklar. |
| Span | `40` | Bir satırdaki bir veya daha fazla karakteri temsil eder. Bu, alan başlangıç/bitiş işaretçileri, yer imleri ve yorumlar gibi özel karakterleri içerir. Span'ın alt varlıkları olmayabilir. |
| Footnote | `100` | Dipnot içeriği için yer tutucuyu temsil eder. Dipnotta şunlar olabilir:Note alt varlıklar. |
| Endnote | `200` | Son not içeriği için yer tutucuyu temsil eder. Son notta şunlar olabilir:Note alt varlıklar. |
| Note | `4000` | Not içeriği için yer tutucuyu temsil eder. Notta şunlar olabilir:Line VeRow alt varlıklar. |
| HeaderFooter | `400` | Bir sayfadaki üstbilgi/altbilgi içeriği için yer tutucuyu temsil eder. HeaderFooter'da şunlar bulunabilir:Line VeRow alt varlıklar. |
| TextBox | `800` | Bir şeklin içindeki metin alanını temsil eder. Metin kutusu şunları içerebilir:Line VeRow alt varlıklar. |
| Comment | `1000` | Yorum içeriği için yer tutucuyu temsil eder. Yorumda şunlar olabilir:Line VeRow alt varlıklar. |
| NoteSeparator | `2000` | Dipnot/sonnot ayırıcısını temsil eder. Not Ayırıcıda şunlar olabilir:Line VeRow alt varlıklar. |

## Örnekler

Bir belgenin düzen varlıkları arasında geçiş yapma yollarını gösterir.

```csharp
public void LayoutEnumerator()
{
    // Çeşitli düzen varlıkları içeren bir belge açın.
    // Düzen varlıkları, LayoutEntityType numaralandırmasında yer alan sayfalar, hücreler, satırlar, çizgiler ve diğer nesnelerdir.
    // Her düzen varlığının belge gövdesinde kapladığı dikdörtgen bir alan vardır.
    Document doc = new Document(MyDir + "Layout entities.docx");

    // Bu varlıkları bir ağaç gibi geçebilecek bir numaralandırıcı oluşturun.
    LayoutEnumerator layoutEnumerator = new LayoutEnumerator(doc);

    Assert.AreEqual(doc, layoutEnumerator.Document);

    layoutEnumerator.MoveParent(LayoutEntityType.Page);

    Assert.AreEqual(LayoutEntityType.Page, layoutEnumerator.Type);
    Assert.Throws<InvalidOperationException>(() => Console.WriteLine(layoutEnumerator.Text));

    // Numaralandırıcının ilk düzen öğesinde olacağından emin olmak için bu yöntemi çağırabiliriz.
    layoutEnumerator.Reset();

    // Düzen numaralandırıcının düzen öğelerini çaprazlamaya nasıl devam edeceğini belirleyen iki sıra vardır
    // birden fazla sayfaya yayılan varlıklarla karşılaştığında.
    // 1 - Görsel sırayla:
    // Bir varlığın birden fazla sayfaya yayılan alt öğeleri arasında dolaşırken,
    // sayfa düzeni önceliklidir ve bu sayfadaki diğer alt öğelere geçip bir sonraki sayfadakilerden kaçınırız.
    Console.WriteLine("Traversing from first to last, elements between pages separated:");
    TraverseLayoutForward(layoutEnumerator, 1);

    // Numaralandırıcımız artık koleksiyonun sonunda. Başlangıca geri dönmek için düzen varlıklarını geriye doğru hareket ettirebiliriz.
    Console.WriteLine("Traversing from last to first, elements between pages separated:");
    TraverseLayoutBackward(layoutEnumerator, 1);

    // 2 - Mantıksal sırayla:
    // Bir varlığın birden fazla sayfaya yayılan alt öğeleri arasında dolaşırken,
    // numaralandırıcı tüm alt varlıklar arasında geçiş yapmak için sayfalar arasında hareket edecektir.
    Console.WriteLine("Traversing from first to last, elements between pages mixed:");
    TraverseLayoutForwardLogical(layoutEnumerator, 1);

    Console.WriteLine("Traversing from last to first, elements between pages mixed:");
    TraverseLayoutBackwardLogical(layoutEnumerator, 1);
}

/// <summary>
/// LayoutEnumerator'ın düzen varlığı koleksiyonunu baştan sona numaralandırın,
/// derinlik öncelikli bir şekilde ve "Görsel" sırayla.
/// </summary>
private static void TraverseLayoutForward(LayoutEnumerator layoutEnumerator, int depth)
{
    do
    {
        PrintCurrentEntity(layoutEnumerator, depth);

        if (layoutEnumerator.MoveFirstChild())
        {
            TraverseLayoutForward(layoutEnumerator, depth + 1);
            layoutEnumerator.MoveParent();
        }
    } while (layoutEnumerator.MoveNext());
}

/// <summary>
/// LayoutEnumerator'ın düzen varlığı koleksiyonunu baştan sona numaralandırın,
/// derinlik öncelikli bir şekilde ve "Görsel" sırayla.
/// </summary>
private static void TraverseLayoutBackward(LayoutEnumerator layoutEnumerator, int depth)
{
    do
    {
        PrintCurrentEntity(layoutEnumerator, depth);

        if (layoutEnumerator.MoveLastChild())
        {
            TraverseLayoutBackward(layoutEnumerator, depth + 1);
            layoutEnumerator.MoveParent();
        }
    } while (layoutEnumerator.MovePrevious());
}

/// <summary>
/// LayoutEnumerator'ın düzen varlığı koleksiyonunu baştan sona numaralandırın,
/// derinlik öncelikli bir şekilde ve "Mantıksal" sırayla.
/// </summary>
private static void TraverseLayoutForwardLogical(LayoutEnumerator layoutEnumerator, int depth)
{
    do
    {
        PrintCurrentEntity(layoutEnumerator, depth);

        if (layoutEnumerator.MoveFirstChild())
        {
            TraverseLayoutForwardLogical(layoutEnumerator, depth + 1);
            layoutEnumerator.MoveParent();
        }
    } while (layoutEnumerator.MoveNextLogical());
}

/// <summary>
/// LayoutEnumerator'ın düzen varlığı koleksiyonunu baştan sona numaralandırın,
/// derinlik öncelikli bir şekilde ve "Mantıksal" sırayla.
/// </summary>
private static void TraverseLayoutBackwardLogical(LayoutEnumerator layoutEnumerator, int depth)
{
    do
    {
        PrintCurrentEntity(layoutEnumerator, depth);

        if (layoutEnumerator.MoveLastChild())
        {
            TraverseLayoutBackwardLogical(layoutEnumerator, depth + 1);
            layoutEnumerator.MoveParent();
        }
    } while (layoutEnumerator.MovePreviousLogical());
}

/// <summary>
/// Metni sekme karakterleriyle girintilerken, LayoutEnumerator'ın geçerli varlığı hakkındaki bilgileri konsola yazdırın
/// yapıcı LayoutEnumerator örneğinde sağladığımız kök düğüme göre derinliğine dayalı.
/// Sonda işlediğimiz dikdörtgen, varlığın belgede kapladığı alanı ve konumu temsil eder.
/// </summary>
private static void PrintCurrentEntity(LayoutEnumerator layoutEnumerator, int indent)
{
    string tabs = new string('\t', indent);

    Console.WriteLine(layoutEnumerator.Kind == string.Empty
        ? $"{tabs}-> Entity type: {layoutEnumerator.Type}"
        : $"{tabs}-> Entity type & kind: {layoutEnumerator.Type}, {layoutEnumerator.Kind}");

    // Yalnızca yayılma alanları metin içerebilir.
    if (layoutEnumerator.Type == LayoutEntityType.Span)
        Console.WriteLine($"{tabs}   Span contents: \"{layoutEnumerator.Text}\"");

    RectangleF leRect = layoutEnumerator.Rectangle;
    Console.WriteLine($"{tabs}   Rectangle dimensions {leRect.Width}x{leRect.Height}, X={leRect.X} Y={leRect.Y}");
    Console.WriteLine($"{tabs}   Page {layoutEnumerator.PageIndex}");
}
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Layout](../../aspose.words.layout/)
* toplantı [Aspose.Words](../../)
