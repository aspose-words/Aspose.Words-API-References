---
title: StyleCollection.ClearQuickStyleGallery
linktitle: ClearQuickStyleGallery
articleTitle: ClearQuickStyleGallery
second_title: .NET için Aspose.Words
description: StyleCollection'ın ClearQuickStyleGallery yöntemi ile Hızlı Stil Galerinizden stilleri zahmetsizce temizleyin. Tasarım sürecinizi bugün basitleştirin!
type: docs
weight: 80
url: /tr/net/aspose.words/stylecollection/clearquickstylegallery/
---
## StyleCollection.ClearQuickStyleGallery method

Hızlı Stil Galerisi panelinden tüm stilleri kaldırır.

```csharp
public void ClearQuickStyleGallery()
```

## Örnekler

Stil Galerisi panelinden stillerin nasıl kaldırılacağını gösterir.

```csharp
Document doc = new Document();
// Stil kaldırma işleminin şimdilik yalnızca DOCX formatıyla çalıştığını unutmayın.
doc.Styles.ClearQuickStyleGallery();

doc.Save(ArtifactsDir + "Styles.RemoveStylesFromStyleGallery.docx");
```

### Ayrıca bakınız

* class [StyleCollection](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
