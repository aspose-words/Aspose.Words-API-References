---
title: StyleCollection.ClearQuickStyleGallery
second_title: Aspose.Words for .NET API Referansı
description: StyleCollection yöntem. Hızlı Stil Galerisi panelinden tüm stilleri kaldırır.
type: docs
weight: 80
url: /tr/net/aspose.words/stylecollection/clearquickstylegallery/
---
## StyleCollection.ClearQuickStyleGallery method

Hızlı Stil Galerisi panelinden tüm stilleri kaldırır.

```csharp
public void ClearQuickStyleGallery()
```

### Örnekler

Stil Galerisi panelinden stillerin nasıl kaldırılacağını gösterir.

```csharp
Document doc = new Document();

// Silme stillerinin şimdilik sadece DOCX formatı ile çalıştığını unutmayın.
doc.Styles.ClearQuickStyleGallery();

doc.Save(ArtifactsDir + "Styles.RemoveStylesFromStyleGallery.docx");
```

### Ayrıca bakınız

* class [StyleCollection](../)
* ad alanı [Aspose.Words](../../stylecollection/)
* toplantı [Aspose.Words](../../../)


