---
title: VbaProject.Clone
linktitle: Clone
articleTitle: Clone
second_title: .NET için Aspose.Words
description: VbaProject'inizi Clone yöntemiyle zahmetsizce çoğaltın. İş akışınızı geliştirin ve proje yönetimini bugün kolaylaştırın!
type: docs
weight: 80
url: /tr/net/aspose.words.vba/vbaproject/clone/
---
## VbaProject.Clone method

Bir kopyasını gerçekleştirir[`VbaProject`](../) .

```csharp
public VbaProject Clone()
```

### Geri dönüş değeri

Klonlanmış[`VbaProject`](../).

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

* class [VbaProject](../)
* ad alanı [Aspose.Words.Vba](../../../aspose.words.vba/)
* toplantı [Aspose.Words](../../../)
