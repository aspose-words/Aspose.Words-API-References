---
title: RevisionOptions.InsertCellColor
linktitle: InsertCellColor
articleTitle: InsertCellColor
second_title: .NET için Aspose.Words
description: RevisionOptions'daki InsertCellColor özelliğiyle elektronik tablonuzu özelleştirin. Eklenen hücreler için tercih ettiğiniz rengi seçin—varsayılan mavidir!
type: docs
weight: 50
url: /tr/net/aspose.words.layout/revisionoptions/insertcellcolor/
---
## RevisionOptions.InsertCellColor property

Eklenen hücreler için kullanılacak rengin belirtilmesine olanak tanırInsertion . Varsayılan değerBlue .

```csharp
public RevisionColor InsertCellColor { get; set; }
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
