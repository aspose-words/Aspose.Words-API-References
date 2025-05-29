---
title: LayoutEnumerator.Rectangle
linktitle: Rectangle
articleTitle: Rectangle
second_title: .NET için Aspose.Words
description: LayoutEnumerator Rectangle özelliğini keşfedin. Sayfanın sol üst köşesine göre varlıkların kesin sınırlayıcı dikdörtgenlerini noktalar halinde alın.
type: docs
weight: 70
url: /tr/net/aspose.words.layout/layoutenumerator/rectangle/
---
## LayoutEnumerator.Rectangle property

Geçerli varlığın sınırlayıcı dikdörtgenini sayfanın sol üst köşesine göre döndürür (nokta cinsinden).

```csharp
public RectangleF Rectangle { get; }
```

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

* class [LayoutEnumerator](../)
* ad alanı [Aspose.Words.Layout](../../../aspose.words.layout/)
* toplantı [Aspose.Words](../../../)
