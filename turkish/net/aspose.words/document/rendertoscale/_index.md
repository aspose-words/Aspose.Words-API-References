---
title: Document.RenderToScale
second_title: Aspose.Words for .NET API Referansı
description: Document yöntem. Bir belge sayfasını birGraphics belirtilen ölçeğe itiraz.
type: docs
weight: 700
url: /tr/net/aspose.words/document/rendertoscale/
---
## Document.RenderToScale method

Bir belge sayfasını birGraphics belirtilen ölçeğe itiraz.

```csharp
public SizeF RenderToScale(int pageIndex, Graphics graphics, float x, float y, float scale)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| pageIndex | Int32 | 0 tabanlı sayfa dizini. |
| graphics | Graphics | Oluşturulacak nesne. |
| x | Single | İşlenen sayfanın sol üst köşesinin X koordinatı (dünya birimleri cinsinden). |
| y | Single | İşlenen sayfanın sol üst köşesinin Y koordinatı (dünya birimleri cinsinden). |
| scale | Single | Sayfayı oluşturma ölçeği (1,0, %100'dür). |

### Geri dönüş değeri

İşlenen sayfanın genişliği ve yüksekliği (dünya birimleri cinsinden).

### Örnekler

Tüm sayfaların küçük resimleriyle tek bir görüntü oluşturmak için bir belgenin ayrı ayrı sayfalarının grafiklere nasıl dönüştürüleceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Küçük resimlerle dolduracağımız satır ve sütun sayısını hesaplayın.
const int thumbColumns = 2;
int thumbRows = Math.DivRem(doc.PageCount, thumbColumns, out int remainder);

if (remainder > 0)
    thumbRows++;

// Küçük resimleri ilk sayfanın boyutuna göre ölçeklendirin.
const float scale = 0.25f;
Size thumbSize = doc.GetPageInfo(0).GetSizeInPixels(scale, 96);

// Tüm küçük resimleri içerecek görselin boyutunu hesaplayın.
int imgWidth = thumbSize.Width * thumbColumns;
int imgHeight = thumbSize.Height * thumbRows;

using (Bitmap img = new Bitmap(imgWidth, imgHeight))
{
    using (Graphics gr = Graphics.FromImage(img))
    {
        gr.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;

        // Varsayılan olarak şeffaf olan arka planı beyazla doldurun.
        gr.FillRectangle(new SolidBrush(Color.White), 0, 0, imgWidth, imgHeight);

        for (int pageIndex = 0; pageIndex < doc.PageCount; pageIndex++)
        {
            int rowIdx = Math.DivRem(pageIndex, thumbColumns, out int columnIdx);

            // Küçük resmin nerede görünmesini istediğimizi belirtin.
            float thumbLeft = columnIdx * thumbSize.Width;
            float thumbTop = rowIdx * thumbSize.Height;

            // Bir sayfayı küçük resim olarak işleyin ve ardından onu aynı boyutta bir dikdörtgenin içine çerçeveleyin.
            SizeF size = doc.RenderToScale(pageIndex, gr, thumbLeft, thumbTop, scale);
            gr.DrawRectangle(Pens.Black, thumbLeft, thumbTop, size.Width, size.Height);
        }

        img.Save(ArtifactsDir + "Rendering.Thumbnails.png");
    }
}
```

Tüm sayfaların küçük resimlerini içeren tek bir görüntü oluşturmak için ayrı ayrı sayfaları grafiklere dönüştürür (.NetStandard 2.0).

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Küçük resimlerle dolduracağımız satır ve sütun sayısını hesaplayın.
const int thumbnailColumnsNum = 2;
int thumbRows = Math.DivRem(doc.PageCount, thumbnailColumnsNum, out int remainder);

if (remainder > 0)
    thumbRows++;

 // Küçük resimleri ilk sayfanın boyutuna göre ölçeklendirin.
const float scale = 0.25f;
Size thumbSize = doc.GetPageInfo(0).GetSizeInPixels(scale, 96);

// Tüm küçük resimleri içerecek görselin boyutunu hesaplayın.
int imgWidth = thumbSize.Width * thumbnailColumnsNum;
int imgHeight = thumbSize.Height * thumbRows;

using (SKBitmap bitmap = new SKBitmap(imgWidth, imgHeight))
{
    using (SKCanvas canvas = new SKCanvas(bitmap))
    {
        // Varsayılan olarak şeffaf olan arka planı beyazla doldurun.
        canvas.Clear(SKColors.White);

        for (int pageIndex = 0; pageIndex < doc.PageCount; pageIndex++)
        {
            int rowIdx = Math.DivRem(pageIndex, thumbnailColumnsNum, out int columnIdx);

            // Küçük resmin nerede görünmesini istediğimizi belirtin.
            float thumbLeft = columnIdx * thumbSize.Width;
            float thumbTop = rowIdx * thumbSize.Height;

            SizeF size = doc.RenderToScale(pageIndex, canvas, thumbLeft, thumbTop, scale);

            // Bir sayfayı küçük resim olarak işleyin ve ardından onu aynı boyutta bir dikdörtgenin içine çerçeveleyin.
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
* ad alanı [Aspose.Words](../../document/)
* toplantı [Aspose.Words](../../../)


