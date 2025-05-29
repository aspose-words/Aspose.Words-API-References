---
title: VbaModule.Clone
linktitle: Clone
articleTitle: Clone
second_title: .NET için Aspose.Words
description: Clone yöntemiyle VbaModule'ünüzü zahmetsizce çoğaltın. Bu güçlü özellik ile kodlama sürecinizi kolaylaştırın ve üretkenliğinizi artırın.
type: docs
weight: 50
url: /tr/net/aspose.words.vba/vbamodule/clone/
---
## VbaModule.Clone method

Bir kopyasını gerçekleştirir[`VbaModule`](../) .

```csharp
public VbaModule Clone()
```

### Geri dönüş değeri

Klonlanmış[`VbaModule`](../).

## Örnekler

Bir VBA projesinin ve modülünün nasıl derin klonlanacağını gösterir.

```csharp
Document doc = new Document(MyDir + "VBA project.docm");
Document destDoc = new Document();

VbaProject copyVbaProject = doc.VbaProject.Clone();
destDoc.VbaProject = copyVbaProject;

// Hedef belgede zaten "Module1" adında bir modülümüz var
// çünkü onu projeyle birlikte klonladık. Modülü kaldırmamız gerekecek.
VbaModule oldVbaModule = destDoc.VbaProject.Modules["Module1"];
VbaModule copyVbaModule = doc.VbaProject.Modules["Module1"].Clone();
destDoc.VbaProject.Modules.Remove(oldVbaModule);
destDoc.VbaProject.Modules.Add(copyVbaModule);

destDoc.Save(ArtifactsDir + "VbaProject.CloneVbaProject.docm");
```

### Ayrıca bakınız

* class [VbaModule](../)
* ad alanı [Aspose.Words.Vba](../../../aspose.words.vba/)
* toplantı [Aspose.Words](../../../)
