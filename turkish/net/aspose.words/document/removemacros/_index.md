---
title: Document.RemoveMacros
linktitle: RemoveMacros
articleTitle: RemoveMacros
second_title: Aspose.Words for .NET
description: Document RemoveMacros yöntem. Tüm makroların VBA projesinin yanı sıra araç çubuklarını ve komut özelleştirmelerini belgeden kaldırır C#'da.
type: docs
weight: 670
url: /tr/net/aspose.words/document/removemacros/
---
## Document.RemoveMacros method

Tüm makroların (VBA projesinin) yanı sıra araç çubuklarını ve komut özelleştirmelerini belgeden kaldırır.

```csharp
public void RemoveMacros()
```

## Notlar

Bir belgedeki tüm makroları kaldırarak, belgenin makro virüsü içermediğinden emin olabilirsiniz.

## Örnekler

Bir belgedeki tüm makroların nasıl kaldırılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Macro.docm");

Assert.IsTrue(doc.HasMacros);
Assert.AreEqual("Project", doc.VbaProject.Name);

// Belgenin VBA projesini tüm makrolarıyla birlikte kaldırın.
doc.RemoveMacros();

Assert.IsFalse(doc.HasMacros);
Assert.Null(doc.VbaProject);
```

### Ayrıca bakınız

* class [Document](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
