---
title: LayoutOptions.CommentDisplayMode
linktitle: CommentDisplayMode
articleTitle: CommentDisplayMode
second_title: .NET için Aspose.Words
description: Yorum oluşturmayı özelleştirmek için LayoutOptions CommentDisplayMode özelliğini keşfedin. ShowInBalloons gibi seçeneklerle kullanıcı deneyimini geliştirmek için kolayca ayarlayın.
type: docs
weight: 30
url: /tr/net/aspose.words.layout/layoutoptions/commentdisplaymode/
---
## LayoutOptions.CommentDisplayMode property

Yorumların işlenme şeklini alır veya ayarlar. Varsayılan değerShowInBalloons .

```csharp
public CommentDisplayMode CommentDisplayMode { get; set; }
```

## Notlar

Düzeltmelerin balonlarda işlenmediğini unutmayınShowInAnnotations .

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

* enum [CommentDisplayMode](../../commentdisplaymode/)
* class [LayoutOptions](../)
* ad alanı [Aspose.Words.Layout](../../../aspose.words.layout/)
* toplantı [Aspose.Words](../../../)
