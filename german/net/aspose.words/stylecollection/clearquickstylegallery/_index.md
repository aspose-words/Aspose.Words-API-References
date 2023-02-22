---
title: StyleCollection.ClearQuickStyleGallery
second_title: Aspose.Words für .NET-API-Referenz
description: StyleCollection methode. Entfernt alle Stile aus dem SchnellstilGaleriebedienfeld.
type: docs
weight: 80
url: /de/net/aspose.words/stylecollection/clearquickstylegallery/
---
## StyleCollection.ClearQuickStyleGallery method

Entfernt alle Stile aus dem Schnellstil-Galeriebedienfeld.

```csharp
public void ClearQuickStyleGallery()
```

### Beispiele

Zeigt, wie Stile aus dem Bedienfeld "Stilgalerie" entfernt werden.

```csharp
Document doc = new Document();

// Beachten Sie, dass das Entfernen von Stilen vorerst nur mit dem DOCX-Format funktioniert.
doc.Styles.ClearQuickStyleGallery();

doc.Save(ArtifactsDir + "Styles.RemoveStylesFromStyleGallery.docx");
```

### Siehe auch

* class [StyleCollection](../)
* namensraum [Aspose.Words](../../stylecollection/)
* Montage [Aspose.Words](../../../)


