---
title: LayoutEnumerator.MovePreviousLogical
linktitle: MovePreviousLogical
articleTitle: MovePreviousLogical
second_title: Aspose.Words for .NET
description: LayoutEnumerator MovePreviousLogical yöntem. Mantıksal bir sırayla önceki kardeş varlığa gider. Sayfalara bölünmüş bir paragrafın satırları yinelenirken bu method başka bir sayfada bulunsa bile önceki satıra gider C#'da.
type: docs
weight: 160
url: /tr/net/aspose.words.layout/layoutenumerator/movepreviouslogical/
---
## LayoutEnumerator.MovePreviousLogical method

Mantıksal bir sırayla önceki kardeş varlığa gider. Sayfalara bölünmüş bir paragrafın satırları yinelenirken, bu method başka bir sayfada bulunsa bile önceki satıra gider.

```csharp
public bool MovePreviousLogical()
```

## Notlar

Hepsinin olduğunu unutmayınSpan varlıklar birbirine bağlanır, böylece[`Current`](../current/) varlığı aralıklıdır, bu yöntemin tekrar tekrar çağrılması belgenin tüm hikayesini yineleyecektir.

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

* class [LayoutEnumerator](../)
* ad alanı [Aspose.Words.Layout](../../../aspose.words.layout/)
* toplantı [Aspose.Words](../../../)
