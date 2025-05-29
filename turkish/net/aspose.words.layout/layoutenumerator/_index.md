---
title: LayoutEnumerator Class
linktitle: LayoutEnumerator
articleTitle: LayoutEnumerator
second_title: .NET için Aspose.Words
description: Verimli belge düzeni numaralandırması için Aspose.Words.Layout.LayoutEnumerator sınıfını keşfedin. Sayfa geometrisini, metni ve yapıyı zahmetsizce keşfedin!
type: docs
weight: 3790
url: /tr/net/aspose.words.layout/layoutenumerator/
---
## LayoutEnumerator class

Bir belgenin sayfa düzeni varlıklarını numaralandırır. Sayfa düzeni modelini incelemek için bu sınıfı kullanabilirsiniz. Mevcut özellikler tür, geometri, metin ve varlığın işlendiği sayfa dizini, ve genel yapı ve ilişkilerdir. Aşağıdakilerin birleşimini kullanın[`GetEntity`](../layoutcollector/getentity/) Ve[`Current`](./current/) Bir belge düğümüne karşılık gelen varlığa geçin.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Sabit Sayfa Biçimine Dönüştürme](https://docs.aspose.com/words/net/converting-to-fixed-page-format/) belgeleme makalesi.

```csharp
public class LayoutEnumerator
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [LayoutEnumerator](layoutenumerator/)(*[Document](../../aspose.words/document/)*) | Bu sınıfın yeni örneğini başlatır. |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Current](../../aspose.words.layout/layoutenumerator/current/) { get; set; } | Sayfa düzeni modelindeki geçerli konumu alır veya ayarlar. Bu özellik, geçerli düzen varlığına karşılık gelen opak bir nesne döndürür. |
| [Document](../../aspose.words.layout/layoutenumerator/document/) { get; } | Bu örneğin sıraladığı belgeyi alır. |
| [Item](../../aspose.words.layout/layoutenumerator/item/) { get; } | Varlığın adlandırılmış bir özelliğini alır. |
| [Kind](../../aspose.words.layout/layoutenumerator/kind/) { get; } | Mevcut varlığın türünü alır. Bu boş bir dize olabilir ancak asla`hükümsüz` . |
| [PageIndex](../../aspose.words.layout/layoutenumerator/pageindex/) { get; } | Geçerli varlığı içeren bir sayfanın 1 tabanlı dizinini alır. |
| [Rectangle](../../aspose.words.layout/layoutenumerator/rectangle/) { get; } | Geçerli varlığın sınırlayıcı dikdörtgenini sayfanın sol üst köşesine göre döndürür (nokta cinsinden). |
| [Text](../../aspose.words.layout/layoutenumerator/text/) { get; } | Mevcut span varlığının metnini alır. Diğer varlık türleri için atar. |
| [Type](../../aspose.words.layout/layoutenumerator/type/) { get; } | Mevcut varlığın türünü alır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [MoveFirstChild](../../aspose.words.layout/layoutenumerator/movefirstchild/)() | İlk alt varlığa geçer. |
| [MoveLastChild](../../aspose.words.layout/layoutenumerator/movelastchild/)() | Son alt varlığa gider. |
| [MoveNext](../../aspose.words.layout/layoutenumerator/movenext/)() | Görsel sıradaki bir sonraki kardeş varlığa gider. Sayfalar arasında bölünmüş bir paragrafın satırlarını yinelerken bu method bir sonraki sayfaya gitmez, bunun yerine aynı sayfadaki bir sonraki varlığa gider. |
| [MoveNextLogical](../../aspose.words.layout/layoutenumerator/movenextlogical/)() | Mantıksal bir sırayla bir sonraki kardeş varlığa gider. Sayfalar arasında bölünmüş bir paragrafın satırlarını yinelerken bu yöntem başka bir sayfada bulunsa bile bir sonraki satıra gider. |
| [MoveParent](../../aspose.words.layout/layoutenumerator/moveparent/#moveparent)() | Üst varlığa geçer. |
| [MoveParent](../../aspose.words.layout/layoutenumerator/moveparent/#moveparent_1)(*[LayoutEntityType](../layoutentitytype/)*) | Belirtilen türün üst varlığına gider. |
| [MovePrevious](../../aspose.words.layout/layoutenumerator/moveprevious/)() | Önceki kardeş varlığa geçer. |
| [MovePreviousLogical](../../aspose.words.layout/layoutenumerator/movepreviouslogical/)() | Mantıksal bir sırayla önceki kardeş varlığa gider. Sayfalar arasında bölünmüş bir paragrafın satırlarını yinelerken bu yöntem başka bir sayfada bulunsa bile önceki satıra gider. |
| [Reset](../../aspose.words.layout/layoutenumerator/reset/)() | Numaratör'ü belgenin ilk sayfasına taşır. |

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
