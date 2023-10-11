---
title: Class LayoutEnumerator
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Layout.LayoutEnumerator sınıf. Bir belgenin sayfa düzeni varlıklarını numaralandırır. Sayfa düzeni modeli üzerinde gezinmek için bu sınıfı kullanabilirsiniz. Kullanılabilir özellikler arasında tür geometri metin ve varlığın oluşturulduğu sayfa dizini ve ayrıca genel yapı ve ilişkiler bulunur. Şunların kombinasyonunu kullanınGetEntity VeCurrent belge düğümüne karşılık gelen varlığa gidin.
type: docs
weight: 3340
url: /tr/net/aspose.words.layout/layoutenumerator/
---
## LayoutEnumerator class

Bir belgenin sayfa düzeni varlıklarını numaralandırır. Sayfa düzeni modeli üzerinde gezinmek için bu sınıfı kullanabilirsiniz. Kullanılabilir özellikler arasında tür, geometri, metin ve varlığın oluşturulduğu sayfa dizini, ve ayrıca genel yapı ve ilişkiler bulunur. Şunların kombinasyonunu kullanın:[`GetEntity`](../layoutcollector/getentity/) Ve[`Current`](./current/) belge düğümüne karşılık gelen varlığa gidin.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Sabit Sayfa Formatına Dönüştürme](https://docs.aspose.com/words/net/converting-to-fixed-page-format/) dokümantasyon makalesi.

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
| [Document](../../aspose.words.layout/layoutenumerator/document/) { get; } | Bu örneğin numaralandırdığı belgeyi alır. |
| [Item](../../aspose.words.layout/layoutenumerator/item/) { get; } | Varlığın adlandırılmış bir özelliğini alır. |
| [Kind](../../aspose.words.layout/layoutenumerator/kind/) { get; } | Geçerli varlığın türünü alır. Bu boş bir dize olabilir ama asla`hükümsüz` . |
| [PageIndex](../../aspose.words.layout/layoutenumerator/pageindex/) { get; } | Geçerli varlığı içeren bir sayfanın 1 tabanlı dizinini alır. |
| [Rectangle](../../aspose.words.layout/layoutenumerator/rectangle/) { get; } | Geçerli varlığın sınırlayıcı dikdörtgenini sayfanın sol üst köşesine göre (nokta cinsinden) döndürür. |
| [Text](../../aspose.words.layout/layoutenumerator/text/) { get; } | Geçerli yayılma varlığının metnini alır. Diğer varlık türleri için fırlatmalar. |
| [Type](../../aspose.words.layout/layoutenumerator/type/) { get; } | Geçerli varlığın türünü alır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [MoveFirstChild](../../aspose.words.layout/layoutenumerator/movefirstchild/)() | İlk alt varlığa gider. |
| [MoveLastChild](../../aspose.words.layout/layoutenumerator/movelastchild/)() | Son alt varlığa gider. |
| [MoveNext](../../aspose.words.layout/layoutenumerator/movenext/)() | Görsel sırayla bir sonraki kardeş varlığa geçer. Sayfalara bölünmüş bir paragrafın satırları yinelenirken bu method sonraki sayfaya geçmez, bunun yerine aynı sayfadaki sonraki varlığa geçer. |
| [MoveNextLogical](../../aspose.words.layout/layoutenumerator/movenextlogical/)() | Mantıksal bir sırayla sonraki kardeş varlığa geçer. Sayfalara bölünmüş bir paragrafın satırları yinelenirken, bu method başka bir sayfada bulunsa bile bir sonraki satıra geçer. |
| [MoveParent](../../aspose.words.layout/layoutenumerator/moveparent/#moveparent)() | Üst varlığa gider. |
| [MoveParent](../../aspose.words.layout/layoutenumerator/moveparent/#moveparent_1)(LayoutEntityType) | Belirtilen türdeki üst varlığa gider. |
| [MovePrevious](../../aspose.words.layout/layoutenumerator/moveprevious/)() | Önceki kardeş varlığa gider. |
| [MovePreviousLogical](../../aspose.words.layout/layoutenumerator/movepreviouslogical/)() | Mantıksal bir sırayla önceki kardeş varlığa gider. Sayfalara bölünmüş bir paragrafın satırları yinelenirken, bu method başka bir sayfada bulunsa bile önceki satıra gider. |
| [Reset](../../aspose.words.layout/layoutenumerator/reset/)() | Numaralandırıcıyı belgenin ilk sayfasına taşır. |

### Örnekler

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


