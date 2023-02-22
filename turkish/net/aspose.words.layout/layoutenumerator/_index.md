---
title: Class LayoutEnumerator
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Layout.LayoutEnumerator sınıf. Bir belgenin sayfa yerleşimi varlıklarını numaralandırır. Sayfa yerleşimi modelinde gezinmek için bu sınıfı kullanabilirsiniz. Mevcut özellikler varlığın oluşturulduğu tür geometri metin ve sayfa dizinidir ve ayrıca genel yapı ve ilişkiler. Şunların kombinasyonunu kullanınGetEntity veCurrent bir belge düğümüne karşılık gelen varlığa taşıyın.
type: docs
weight: 3140
url: /tr/net/aspose.words.layout/layoutenumerator/
---
## LayoutEnumerator class

Bir belgenin sayfa yerleşimi varlıklarını numaralandırır. Sayfa yerleşimi modelinde gezinmek için bu sınıfı kullanabilirsiniz. Mevcut özellikler, varlığın oluşturulduğu tür, geometri, metin ve sayfa dizinidir, ve ayrıca genel yapı ve ilişkiler. Şunların kombinasyonunu kullanın[`GetEntity`](../layoutcollector/getentity/) ve[`Current`](./current/) bir belge düğümüne karşılık gelen varlığa taşıyın.

```csharp
public class LayoutEnumerator
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [LayoutEnumerator](layoutenumerator/)(Document) | Bu sınıfın yeni örneğini başlatır. |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Current](../../aspose.words.layout/layoutenumerator/current/) { get; set; } | Sayfa düzeni modelindeki geçerli konumu alır veya ayarlar. Bu özellik, geçerli düzen varlığına karşılık gelen opak bir nesne döndürür. |
| [Document](../../aspose.words.layout/layoutenumerator/document/) { get; } | Bu örneğin numaralandırıldığı belgeyi alır. |
| [Kind](../../aspose.words.layout/layoutenumerator/kind/) { get; } | Geçerli varlığın türünü alır. Bu boş bir dize olabilir ama asla null. |
| [PageIndex](../../aspose.words.layout/layoutenumerator/pageindex/) { get; } | Geçerli varlığı içeren bir sayfanın 1 tabanlı dizinini alır. |
| [Rectangle](../../aspose.words.layout/layoutenumerator/rectangle/) { get; } | Sayfanın sol üst köşesine göre geçerli varlığın sınırlayıcı dikdörtgenini döndürür (nokta olarak). |
| [Text](../../aspose.words.layout/layoutenumerator/text/) { get; } | Geçerli yayılma varlığının metnini alır. Diğer varlık türleri için atar. |
| [Type](../../aspose.words.layout/layoutenumerator/type/) { get; } | Geçerli varlığın türünü alır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [MoveFirstChild](../../aspose.words.layout/layoutenumerator/movefirstchild/)() | İlk alt varlığa gider. |
| [MoveLastChild](../../aspose.words.layout/layoutenumerator/movelastchild/)() | Son alt varlığa gider. |
| [MoveNext](../../aspose.words.layout/layoutenumerator/movenext/)() | Görsel sırayla sonraki kardeş varlığa gider. Sayfalar arasında bölünmüş bir paragrafın satırlarını yinelerken bu method sonraki sayfaya değil, aynı sayfadaki sonraki varlığa taşınır. |
| [MoveNextLogical](../../aspose.words.layout/layoutenumerator/movenextlogical/)() | Mantıksal bir sırayla sonraki kardeş varlığa gider. Sayfalar arasında bölünmüş bir paragrafın satırlarını yinelerken bu method başka bir sayfada bulunsa bile bir sonraki satıra taşınır. |
| [MoveParent](../../aspose.words.layout/layoutenumerator/moveparent/#moveparent)() | Üst varlığa gider. |
| [MoveParent](../../aspose.words.layout/layoutenumerator/moveparent/#moveparent_1)(LayoutEntityType) | Belirtilen türün üst varlığına gider. |
| [MovePrevious](../../aspose.words.layout/layoutenumerator/moveprevious/)() | Önceki kardeş varlığa gider. |
| [MovePreviousLogical](../../aspose.words.layout/layoutenumerator/movepreviouslogical/)() | Mantıksal bir sırayla önceki kardeş varlığa gider. Sayfalar arasında bölünmüş bir paragrafın satırlarını yinelerken bu method başka bir sayfada bulunsa bile önceki satıra taşınır. |
| [Reset](../../aspose.words.layout/layoutenumerator/reset/)() | Numaralandırıcıyı belgenin ilk sayfasına taşır. |

### Örnekler

Bir belgenin yerleşim varlıklarını geçmenin yollarını gösterir.

```csharp
public void LayoutEnumerator()
{
    // Çeşitli düzen varlıkları içeren bir belge açın.
    // Mizanpaj varlıkları, LayoutEntityType enum'a dahil edilen sayfalar, hücreler, satırlar, çizgiler ve diğer nesnelerdir.
    // Her yerleşim öğesinin belge gövdesinde kapladığı dikdörtgen bir alan vardır.
    Document doc = new Document(MyDir + "Layout entities.docx");

    // Bu varlıkları bir ağaç gibi dolaşabilen bir numaralandırıcı oluşturun.
    LayoutEnumerator layoutEnumerator = new LayoutEnumerator(doc);

    Assert.AreEqual(doc, layoutEnumerator.Document);

    layoutEnumerator.MoveParent(LayoutEntityType.Page);

    Assert.AreEqual(LayoutEntityType.Page, layoutEnumerator.Type);
    Assert.Throws<InvalidOperationException>(() => Console.WriteLine(layoutEnumerator.Text));

    // Numaralandırıcının ilk düzen varlığında olacağından emin olmak için bu yöntemi çağırabiliriz.
    layoutEnumerator.Reset();

    // Yerleşim numaralandırıcısının yerleşim varlıklarını nasıl geçeceğini belirleyen iki sipariş vardır.
    // birden çok sayfaya yayılan varlıklarla karşılaştığında.
    // 1 - Görsel sırayla:
    // Bir varlığın birden çok sayfaya yayılan alt öğeleri arasında gezinirken,
    // sayfa düzeni önceliklidir ve bu sayfadaki diğer alt öğelere geçeriz ve sonrakilerden kaçınırız.
    Console.WriteLine("Traversing from first to last, elements between pages separated:");
    TraverseLayoutForward(layoutEnumerator, 1);

    // Numaralandırıcımız artık koleksiyonun sonunda. Başa dönmek için yerleşim varlıklarını geriye doğru hareket ettirebiliriz.
    Console.WriteLine("Traversing from last to first, elements between pages separated:");
    TraverseLayoutBackward(layoutEnumerator, 1);

    // 2 - Mantıksal sırayla:
    // Bir varlığın birden çok sayfaya yayılan alt öğeleri arasında gezinirken,
    // numaralandırıcı, tüm alt varlıklar arasında geçiş yapmak için sayfalar arasında hareket edecektir.
    Console.WriteLine("Traversing from first to last, elements between pages mixed:");
    TraverseLayoutForwardLogical(layoutEnumerator, 1);

    Console.WriteLine("Traversing from last to first, elements between pages mixed:");
    TraverseLayoutBackwardLogical(layoutEnumerator, 1);
}

/// <summary>
/// layoutEnumerator'ın layout varlık koleksiyonunu önden arkaya numaralandırın,
/// önce derinlemesine ve "Görsel" sırayla.
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
/// önce derinlemesine ve "Görsel" sırayla.
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
/// layoutEnumerator'ın layout varlık koleksiyonunu önden arkaya numaralandırın,
/// önce derinlemesine ve "Mantıksal" sırayla.
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
/// önce derinlemesine ve "Mantıksal" sırayla.
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
/// Metni sekme karakterleriyle girintilerken layoutEnumerator'ın mevcut varlığı hakkındaki bilgileri konsola yazdırın
/// yapıcı LayoutEnumerator örneğinde sağladığımız kök düğüme göre derinliğine göre.
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


