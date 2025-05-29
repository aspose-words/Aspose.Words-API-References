---
title: CommentDisplayMode Enum
linktitle: CommentDisplayMode
articleTitle: CommentDisplayMode
second_title: .NET için Aspose.Words
description: Optimize edilmiş belge yorum oluşturma için Aspose.Words.Layout.CommentDisplayMode enum'unu keşfedin. Belgenizin netliğini ve sunumunu bugün geliştirin!
type: docs
weight: 3740
url: /tr/net/aspose.words.layout/commentdisplaymode/
---
## CommentDisplayMode enumeration

Belge yorumları için işleme modunu belirtir.

```csharp
public enum CommentDisplayMode
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Hide | `0` | Hiçbir belge yorumu oluşturulmadı. |
| ShowInBalloons | `1` | Belge yorumlarını kenar boşluğundaki balonlarda işler. Bu varsayılan değerdir. |
| ShowInAnnotations | `2` | Belge yorumlarını açıklamalarda işler. Bu yalnızca Pdf formatı için kullanılabilir. |

## Örnekler

Bir belgeyi işlenmiş biçime kaydederken yorumların nasıl gösterileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");

Comment comment = new Comment(doc, "John Doe", "J.D.", DateTime.Now);
comment.SetText("My comment.");
builder.CurrentParagraph.AppendChild(comment);

// ShowInAnnotations yalnızca Pdf1.7 ve Pdf1.5 formatlarında kullanılabilir.
// Diğer formatlarda Hide'a benzer şekilde çalışacaktır.
doc.LayoutOptions.CommentDisplayMode = CommentDisplayMode.ShowInAnnotations;

doc.Save(ArtifactsDir + "Document.ShowCommentsInAnnotations.pdf");

// Belge sayfa düzeninin yeniden oluşturulması gerektiğini unutmayın (Document.UpdatePageLayout() yöntemi aracılığıyla)
// Document.LayoutOptions değerleri değiştirildikten sonra.
doc.LayoutOptions.CommentDisplayMode = CommentDisplayMode.ShowInBalloons;
doc.UpdatePageLayout();

doc.Save(ArtifactsDir + "Document.ShowCommentsInBalloons.pdf");
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Layout](../../aspose.words.layout/)
* toplantı [Aspose.Words](../../)
