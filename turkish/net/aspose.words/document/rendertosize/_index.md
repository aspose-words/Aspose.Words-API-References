---
title: Document.RenderToSize
linktitle: RenderToSize
articleTitle: RenderToSize
second_title: .NET için Aspose.Words
description: Belge sayfalarını istediğiniz boyutlarda Grafik nesnelerine verimli bir şekilde dönüştürmek için RenderToSize yöntemini keşfedin. İşleme sürecinizi bugün geliştirin!
type: docs
weight: 740
url: /tr/net/aspose.words/document/rendertosize/
---
## Document.RenderToSize method

Bir belge sayfasını birGraphics nesneyi belirtilen bir boyuta taşı.

```csharp
public float RenderToSize(int pageIndex, Graphics graphics, float x, float y, float width, 
    float height)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| pageIndex | Int32 | 0 tabanlı sayfa indeksi. |
| graphics | Graphics | Hangi nesneye render yapılacağı. |
| x | Single | Oluşturulan sayfanın sol üst köşesinin X koordinatı (dünya birimleri cinsinden). |
| y | Single | İşlenen sayfanın sol üst köşesinin Y koordinatı (dünya birimleri cinsinden). |
| width | Single | İşlenen sayfanın kaplayabileceği maksimum genişlik (dünya birimi cinsinden). |
| height | Single | Oluşturulan sayfanın kaplayabileceği maksimum yükseklik (dünya birimi cinsinden). |

### Geri dönüş değeri

İşlenen sayfanın belirtilen boyuta uyması için otomatik olarak hesaplanan ölçek.

## Örnekler

Belgenin belirtilen bir konum ve boyutta (.NetStandard 2.0) bitmap olarak nasıl işleneceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

using (SKBitmap bitmap = new SKBitmap(700, 700))
{
    using (SKCanvas canvas = new SKCanvas(bitmap))
    {
        // Bu tuvali kullanarak oluşturacağımız sayfaya %70'lik bir ölçekleme faktörü uygulayalım.
        canvas.Scale(70);

        // Sayfayı sayfanın üst ve sol kenarlarından 0,5" uzağa yerleştirin.
        canvas.Translate(0.5f, 0.5f);

        // İşlenen sayfayı 10 derece döndür.
        canvas.RotateDegrees(10);

        // Bir dikdörtgen oluşturup çizin.
        SKRect rect = new SKRect(0f, 0f, 3f, 3f);
        canvas.DrawRect(rect, new SKPaint
        {
            Color = SKColors.Black,
            Style = SKPaintStyle.Stroke,
            StrokeWidth = 3f / 72f
        });

        // Belgenin ilk sayfasını yukarıdaki dikdörtgenle aynı boyutta oluştur.
        // Dikdörtgen bu sayfayı çerçeveleyecek.
        float returnedScale = doc.RenderToSize(0, canvas, 0f, 0f, 3f, 3f);

        Console.WriteLine("The image was rendered at {0:P0} zoom.", returnedScale);

        // Matrisi sıfırlayın ve ardından yeni bir ölçekleme ve çeviri kümesi uygulayın.
        canvas.ResetMatrix();
        canvas.Scale(5);
        canvas.Translate(10, 10);

        // Başka bir dikdörtgen oluştur.
        rect = new SKRect(0, 0, 50, 100);
        rect.Offset(90, 10);
        canvas.DrawRect(rect, new SKPaint
        {
            Color = SKColors.Black,
            Style = SKPaintStyle.Stroke,
            StrokeWidth = 1
        });

        // Yeni oluşturulan dikdörtgenin içindeki ilk sayfayı bir kez daha işle.
        doc.RenderToSize(0, canvas, 90, 10, 50, 100);

        using (SKFileWStream fs = new SKFileWStream(ArtifactsDir + "Rendering.RenderToSizeNetStandard2.png"))
        {
            bitmap.PeekPixels().Encode(fs, SKEncodedImageFormat.Png, 100);
        }
    }
}
```

Bir belgenin belirtilen konum ve boyutta bir bitmap'e nasıl dönüştürüleceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

using (Bitmap bmp = new Bitmap(700, 700))
{
    using (Graphics gr = Graphics.FromImage(bmp))
    {
        gr.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;

        // İnç değerini kullanmak için "PageUnit" özelliğini "GraphicsUnit.Inch" olarak ayarlayın
        // tanımlayacağımız herhangi bir dönüşüm ve boyut için ölçü birimi.
        gr.PageUnit = GraphicsUnit.Inch;

        // Çıktıyı kenardan 0,5" kaydır.
        gr.TranslateTransform(0.5f, 0.5f);

        // Çıktıyı 10 derece döndür.
        gr.RotateTransform(10);

        // 3"x3" boyutlarında bir dikdörtgen çizin.
        gr.DrawRectangle(new Pen(Color.Black, 3f / 72f), 0f, 0f, 3f, 3f);

        // Belgemizin ilk sayfasını dikdörtgenle aynı ölçülerde ve dönüşümle çizelim.
        // Dikdörtgen ilk sayfayı çerçeveleyecektir.
        float returnedScale = doc.RenderToSize(0, gr, 0f, 0f, 3f, 3f);

        // Bu, RenderToSize yönteminin belirtilen boyuta uyması için ilk sayfaya uyguladığı ölçekleme faktörüdür.
        Assert.AreEqual(0.2566f, returnedScale, 0.0001f);

        // Milimetreyi boyut olarak kullanmak için "PageUnit" özelliğini "GraphicsUnit.Millimeter" olarak ayarlayın
        // tanımlayacağımız herhangi bir dönüşüm ve boyut için ölçü birimi.
        gr.PageUnit = GraphicsUnit.Millimeter;

        // Önceki renderda kullandığımız dönüşümleri sıfırlıyoruz.
        gr.ResetTransform();

         // Başka bir dönüşüm kümesini uygula.
        gr.TranslateTransform(10, 10);
        gr.ScaleTransform(0.5f, 0.5f);
        gr.PageScale = 2f;

        // Başka bir dikdörtgen oluşturun ve bunu belgeden başka bir sayfayı çerçevelemek için kullanın.
        gr.DrawRectangle(new Pen(Color.Black, 1), 90, 10, 50, 100);
        doc.RenderToSize(1, gr, 90, 10, 50, 100);

        bmp.Save(ArtifactsDir + "Rendering.RenderToSize.png");
    }
}
```

### Ayrıca bakınız

* class [Document](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
