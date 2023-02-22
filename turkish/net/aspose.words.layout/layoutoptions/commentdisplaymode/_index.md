---
title: LayoutOptions.CommentDisplayMode
second_title: Aspose.Words for .NET API Referansı
description: LayoutOptions mülk. Yorumların oluşturulma şeklini alır veya ayarlar. Varsayılan değerShowInBalloons .
type: docs
weight: 30
url: /tr/net/aspose.words.layout/layoutoptions/commentdisplaymode/
---
## LayoutOptions.CommentDisplayMode property

Yorumların oluşturulma şeklini alır veya ayarlar. Varsayılan değerShowInBalloons .

```csharp
public CommentDisplayMode CommentDisplayMode { get; set; }
```

### Notlar

için revizyonların balonlarda gösterilmediğini unutmayın.ShowInAnnotations .

### Örnekler

Bir belgeyi işlenmiş bir formatta kaydederken yorumların nasıl gösterileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");

Comment comment = new Comment(doc, "John Doe", "J.D.", DateTime.Now);
comment.SetText("My comment.");
builder.CurrentParagraph.AppendChild(comment);

// ShowInAnnotations yalnızca Pdf1.7 ve Pdf1.5 formatlarında mevcuttur.
// Diğer formatlarda, Gizle'ye benzer şekilde çalışacaktır.
doc.LayoutOptions.CommentDisplayMode = CommentDisplayMode.ShowInAnnotations;

doc.Save(ArtifactsDir + "Document.ShowCommentsInAnnotations.pdf");

// Belge sayfa düzenini yeniden oluşturmanın gerekli olduğunu unutmayın (Document.UpdatePageLayout() yöntemi aracılığıyla)
// Document.LayoutOptions değerlerini değiştirdikten sonra.
doc.LayoutOptions.CommentDisplayMode = CommentDisplayMode.ShowInBalloons;
doc.UpdatePageLayout();

doc.Save(ArtifactsDir + "Document.ShowCommentsInBalloons.pdf");
```

### Ayrıca bakınız

* enum [CommentDisplayMode](../../commentdisplaymode/)
* class [LayoutOptions](../)
* ad alanı [Aspose.Words.Layout](../../layoutoptions/)
* toplantı [Aspose.Words](../../../)


