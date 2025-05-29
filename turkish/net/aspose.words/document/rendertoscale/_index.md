---
title: Document.RenderToScale
linktitle: RenderToScale
articleTitle: RenderToScale
second_title: .NET için Aspose.Words
description: En iyi görsel sonuçlar için belge sayfalarını istediğiniz ölçekte Grafik nesnelerine verimli bir şekilde dönüştürmek üzere RenderToScale yöntemini keşfedin.
type: docs
weight: 730
url: /tr/net/aspose.words/document/rendertoscale/
---
## Document.RenderToScale method

Bir belge sayfasını birGraphics belirli bir ölçeğe göre nesne.

```csharp
public SizeF RenderToScale(int pageIndex, Graphics graphics, float x, float y, float scale)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| pageIndex | Int32 | 0 tabanlı sayfa indeksi. |
| graphics | Graphics | Hangi nesneye render yapılacağı. |
| x | Single | Oluşturulan sayfanın sol üst köşesinin X koordinatı (dünya birimleri cinsinden). |
| y | Single | İşlenen sayfanın sol üst köşesinin Y koordinatı (dünya birimleri cinsinden). |
| scale | Single | Sayfanın görüntülenmesi için ölçek (1.0 = %100). |

### Geri dönüş değeri

İşlenen sayfanın genişliği ve yüksekliği (dünya birimleri cinsinden).

## Örnekler

Bir belgenin her bir sayfasının grafik olarak nasıl oluşturulacağını ve tüm sayfaların küçük resimlerinin yer aldığı tek bir görselin nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Küçük resimlerle dolduracağımız satır ve sütun sayısını hesaplayın.
const int thumbColumns = 2;
int thumbRows = doc.PageCount / thumbColumns;
int remainder = doc.PageCount % thumbColumns;

if (remainder > 0)
    thumbRows++;

// Küçük resimleri ilk sayfanın boyutuna göre ölçeklendirin.
const float scale = 0.25f;
Size thumbSize = doc.GetPageInfo(0).GetSizeInPixels(scale, 96);

// Tüm küçük resimleri içerecek olan görüntünün boyutunu hesaplayın.
int imgWidth = thumbSize.Width * thumbColumns;
int imgHeight = thumbSize.Height * thumbRows;

using (Bitmap img = new Bitmap(imgWidth, imgHeight))
{
    using (Graphics gr = Graphics.FromImage(img))
    {
        gr.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;

        // Varsayılan olarak şeffaf olan arka planı beyazla doldur.
        gr.FillRectangle(new SolidBrush(Color.White), 0, 0, imgWidth, imgHeight);

        for (int pageIndex = 0; pageIndex < doc.PageCount; pageIndex++)
        {
            int rowIdx = pageIndex / thumbColumns;
            int columnIdx = pageIndex % thumbColumns;

            // Küçük resmin nerede görünmesini istediğimizi belirtiyoruz.
            float thumbLeft = columnIdx * thumbSize.Width;
            float thumbTop = rowIdx * thumbSize.Height;

            // Bir sayfayı küçük resim olarak oluşturun ve ardından aynı boyutta bir dikdörtgenin içine yerleştirin.
            SizeF size = doc.RenderToScale(pageIndex, gr, thumbLeft, thumbTop, scale);
            gr.DrawRectangle(Pens.Black, thumbLeft, thumbTop, size.Width, size.Height);
        }

        img.Save(ArtifactsDir + "Rendering.Thumbnails.png");
    }
}
```

Tüm sayfaların küçük resimlerini içeren tek bir görüntü oluşturmak için ayrı sayfaları grafiklere dönüştürür (.NetStandard 2.0).

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Küçük resimlerle dolduracağımız satır ve sütun sayısını hesaplayın.
const int thumbnailColumnsNum = 2;
int thumbRows = doc.PageCount / thumbnailColumnsNum;
int remainder = doc.PageCount % thumbnailColumnsNum;

if (remainder > 0)
    thumbRows++;

 // Küçük resimleri ilk sayfanın boyutuna göre ölçeklendirin.
const float scale = 0.25f;
Size thumbSize = doc.GetPageInfo(0).GetSizeInPixels(scale, 96);

// Tüm küçük resimleri içerecek olan görüntünün boyutunu hesaplayın.
int imgWidth = thumbSize.Width * thumbnailColumnsNum;
int imgHeight = thumbSize.Height * thumbRows;

using (SKBitmap bitmap = new SKBitmap(imgWidth, imgHeight))
{
    using (SKCanvas canvas = new SKCanvas(bitmap))
    {
        // Varsayılan olarak şeffaf olan arka planı beyazla doldur.
        canvas.Clear(SKColors.White);

        for (int pageIndex = 0; pageIndex < doc.PageCount; pageIndex++)
        {
            int rowIdx = pageIndex / thumbnailColumnsNum;
            int columnIdx = pageIndex % thumbnailColumnsNum;

            // Küçük resmin nerede görünmesini istediğimizi belirtiyoruz.
            float thumbLeft = columnIdx * thumbSize.Width;
            float thumbTop = rowIdx * thumbSize.Height;

            SizeF size = doc.RenderToScale(pageIndex, canvas, thumbLeft, thumbTop, scale);

            // Bir sayfayı küçük resim olarak oluşturun ve ardından aynı boyutta bir dikdörtgenin içine yerleştirin.
            SKRect rect = new SKRect(0, 0, size.Width, size.Height);
            rect.Offset(thumbLeft, thumbTop);
            canvas.DrawRect(rect, new SKPaint
            {
                Color = SKColors.Black,
                Style = SKPaintStyle.Stroke
            });
        }

        using (SKFileWStream fs = new SKFileWStream(ArtifactsDir + "Rendering.CreateThumbnailsNetStandard2.png"))
        {
            bitmap.PeekPixels().Encode(fs, SKEncodedImageFormat.Png, 100);
        }
    }
}
```

### Ayrıca bakınız

* class [Document](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
