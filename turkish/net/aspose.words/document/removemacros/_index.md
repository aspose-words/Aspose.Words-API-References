---
title: Document.RemoveMacros
linktitle: RemoveMacros
articleTitle: RemoveMacros
second_title: .NET için Aspose.Words
description: Daha temiz bir belge için Document RemoveMacros yöntemi ile VBA projenizden tüm makroları, araç çubuklarını ve özel komut ayarlarını zahmetsizce kaldırın.
type: docs
weight: 720
url: /tr/net/aspose.words/document/removemacros/
---
## Document.RemoveMacros method

Belgeden tüm makroları (VBA projesi) ve araç çubuklarını ve komut özelleştirmelerini kaldırır.

```csharp
public void RemoveMacros()
```

## Notlar

Bir belgeden tüm makroları kaldırarak belgenin hiçbir makro virüsü içermediğinden emin olabilirsiniz.

## Örnekler

Bir belgeden tüm makroların nasıl kaldırılacağını gösterir.

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
