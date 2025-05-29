---
title: LayoutEntityType Enum
linktitle: LayoutEntityType
articleTitle: LayoutEntityType
second_title: .NET için Aspose.Words
description: Gelişmiş belge biçimlendirme ve sorunsuz entegrasyon için çeşitli düzen varlık türlerini içeren Aspose.Words.Layout.LayoutEntityType enum'unu keşfedin.
type: docs
weight: 3780
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
| Page | `1` | Bir belgenin sayfasını temsil eder. Sayfa şu özelliklere sahip olabilir:Column ,HeaderFooter VeComment çocuk varlıklar. |
| Column | `2` | Bir sayfadaki metin sütununu temsil eder. Sütun, aynı alt varlıklara sahip olabilirCell , artıFootnote ,Endnote VeNoteSeparator varlıklar. |
| Row | `8` | Bir tablo satırını temsil eder. Satır şunlardan biri olabilir:Cell çocuk varlıklar olarak. |
| Cell | `10` | Bir tablo hücresini temsil eder. Hücre şu özelliklere sahip olabilir:Line VeRow çocuk varlıklar. |
| Line | `20` | Metin ve satır içi nesnelerin karakter satırını temsil eder. Satır,Span çocuk varlıklar. |
| Span | `40` | Bir satırdaki bir veya daha fazla karakteri temsil eder. Bu, alan başlangıç/bitiş işaretçileri, yer imleri ve yorumlar gibi özel karakterleri içerir. Span'in alt varlıkları olamaz. |
| Footnote | `100` | Dipnot içeriği için yer tutucuyu temsil eder. Dipnot,Note çocuk varlıklar. |
| Endnote | `200` | Son not içeriği için yer tutucuyu temsil eder. Son not şunları içerebilir:Note çocuk varlıklar. |
| Note | `4000` | Not içeriği için yer tutucuyu temsil eder. Not şunları içerebilir:Line VeRow çocuk varlıklar. |
| HeaderFooter | `400` | Bir sayfadaki üstbilgi/altbilgi içeriği için yer tutucuyu temsil eder. HeaderFooter,Line VeRow çocuk varlıklar. |
| TextBox | `800` | Bir şeklin içindeki metin alanını temsil eder. Metin kutusu olabilirLine VeRow çocuk varlıklar. |
| Comment | `1000` | Yorum içeriği için yer tutucuyu temsil eder. Yorum,Line VeRow çocuk varlıklar. |
| NoteSeparator | `2000` | Dipnot/sonnot ayırıcısını temsil eder. NoteSeparator şu şekilde olabilir:Line VeRow çocuk varlıklar. |

## Örnekler

Bir belgenin düzen varlıkları arasında gezinmenin yollarını gösterir.

```csharp
public void LayoutEnumerator()
{
    // Çeşitli düzen varlıkları içeren bir belgeyi açın.
    // Düzen varlıkları, LayoutEntityType enum'unda yer alan sayfalar, hücreler, satırlar, çizgiler ve diğer nesnelerdir.
    // Her düzen varlığının, belge gövdesinde kapladığı dikdörtgen bir alanı vardır.
    Document doc = new Document(MyDir + "Layout entities.docx");

    // Bu varlıkları bir ağaç gibi dolaşabilen bir numaratör oluşturun.
    LayoutEnumerator layoutEnumerator = new LayoutEnumerator(doc);

    Assert.AreEqual(doc, layoutEnumerator.Document);

    layoutEnumerator.MoveParent(LayoutEntityType.Page);

    Assert.AreEqual(LayoutEntityType.Page, layoutEnumerator.Type);
    Assert.Throws<InvalidOperationException>(() => Console.WriteLine(layoutEnumerator.Text));

    // Numaratörün ilk düzen varlığında olacağından emin olmak için bu metodu çağırabiliriz.
    layoutEnumerator.Reset();

    // Düzen numaralandırıcısının düzen varlıklarını dolaşmaya nasıl devam edeceğini belirleyen iki düzen vardır
    // birden fazla sayfaya yayılan varlıklarla karşılaştığında.
    // 1 - Görsel sırayla:
    // Birden fazla sayfaya yayılan bir varlığın alt öğeleri arasında hareket ederken,
    // sayfa düzeni önceliklidir ve bu sayfadaki diğer alt öğelere geçeriz ve bir sonraki sayfadakilerden kaçınırız.
    Console.WriteLine("Traversing from first to last, elements between pages separated:");
    TraverseLayoutForward(layoutEnumerator, 1);

    // Sayıcımız artık koleksiyonun sonunda. Başlangıca geri dönmek için düzen varlıklarını geriye doğru dolaşabiliriz.
    Console.WriteLine("Traversing from last to first, elements between pages separated:");
    TraverseLayoutBackward(layoutEnumerator, 1);

    // 2 - Mantıksal sırayla:
    // Birden fazla sayfaya yayılan bir varlığın alt öğeleri arasında hareket ederken,
    // numaratör tüm alt varlıkları dolaşmak için sayfalar arasında hareket edecektir.
    Console.WriteLine("Traversing from first to last, elements between pages mixed:");
    TraverseLayoutForwardLogical(layoutEnumerator, 1);

    Console.WriteLine("Traversing from last to first, elements between pages mixed:");
    TraverseLayoutBackwardLogical(layoutEnumerator, 1);
}

/// <summary>
/// layoutEnumerator'ın düzen varlık koleksiyonunu baştan sona numaralandırın,
/// derinlemesine ve "Görsel" düzende.
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
/// layoutEnumerator'ın düzen varlık koleksiyonunu arkadan öne doğru numaralandırın,
/// derinlemesine ve "Görsel" düzende.
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
/// layoutEnumerator'ın düzen varlık koleksiyonunu baştan sona numaralandırın,
/// derinlemesine ve "Mantıksal" bir düzende.
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
/// layoutEnumerator'ın düzen varlık koleksiyonunu arkadan öne doğru numaralandırın,
/// derinlemesine ve "Mantıksal" bir düzende.
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
/// Konsola layoutEnumerator'ın geçerli varlığı hakkında bilgi yazdırın, metni sekme karakterleriyle girintileyin
/// LayoutEnumerator örneğinde sağladığımız kök düğüme göre derinliğine göre.
/// Son olarak işlediğimiz dikdörtgen, varlığın belgede kapladığı alanı ve konumu temsil eder.
/// </summary>
private static void PrintCurrentEntity(LayoutEnumerator layoutEnumerator, int indent)
{
    string tabs = new string('\t', indent);

    Console.WriteLine(layoutEnumerator.Kind == string.Empty
        ? $"{tabs}-> Entity type: {layoutEnumerator.Type}"
        : $"{tabs}-> Entity type & kind: {layoutEnumerator.Type}, {layoutEnumerator.Kind}");

    // Sadece span'lar metin içerebilir.
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
