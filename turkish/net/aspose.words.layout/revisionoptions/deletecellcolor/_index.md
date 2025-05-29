---
title: RevisionOptions.DeleteCellColor
linktitle: DeleteCellColor
articleTitle: DeleteCellColor
second_title: .NET için Aspose.Words
description: RevisionOptions DeleteCellColor özelliğiyle elektronik tablonuzu özelleştirin. Silinen hücreler için kolayca benzersiz bir renk ayarlayın, netliği ve organizasyonu artırın.
type: docs
weight: 20
url: /tr/net/aspose.words.layout/revisionoptions/deletecellcolor/
---
## RevisionOptions.DeleteCellColor property

Silinen hücreler için kullanılacak rengin belirlenmesine olanak tanırDeletion . Varsayılan değerPink .

```csharp
public RevisionColor DeleteCellColor { get; set; }
```

## Örnekler

Ekle/sil hücre revizyon renginin nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Cell revisions.docx");

doc.LayoutOptions.RevisionOptions.InsertCellColor = RevisionColor.LightBlue;
doc.LayoutOptions.RevisionOptions.DeleteCellColor = RevisionColor.DarkRed;

doc.Save(ArtifactsDir + "Revision.RevisionCellColor.pdf");
```

### Ayrıca bakınız

* enum [RevisionColor](../../revisioncolor/)
* class [RevisionOptions](../)
* ad alanı [Aspose.Words.Layout](../../../aspose.words.layout/)
* toplantı [Aspose.Words](../../../)
