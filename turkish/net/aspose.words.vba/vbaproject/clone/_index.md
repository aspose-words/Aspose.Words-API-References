---
title: VbaProject.Clone
second_title: Aspose.Words for .NET API Referansı
description: VbaProject yöntem. Bir kopyasını gerçekleştirirVbaProject .
type: docs
weight: 70
url: /tr/net/aspose.words.vba/vbaproject/clone/
---
## VbaProject.Clone method

Bir kopyasını gerçekleştirir[`VbaProject`](../) .

```csharp
public VbaProject Clone()
```

### Geri dönüş değeri

Klonlanmış[`VbaProject`](../).

### Örnekler

Bir VBA projesinin ve modülünün nasıl derinlemesine klonlanacağını gösterir.

```csharp
Document doc = new Document(MyDir + "VBA project.docm");
Document destDoc = new Document();

VbaProject copyVbaProject = doc.VbaProject.Clone();
destDoc.VbaProject = copyVbaProject;

// Hedef belgede zaten "Modül1" adında bir modülümüz var
// çünkü onu projeyle birlikte klonladık. Modülü çıkarmamız gerekecek.
VbaModule oldVbaModule = destDoc.VbaProject.Modules["Module1"];
VbaModule copyVbaModule = doc.VbaProject.Modules["Module1"].Clone();
destDoc.VbaProject.Modules.Remove(oldVbaModule);
destDoc.VbaProject.Modules.Add(copyVbaModule);

destDoc.Save(ArtifactsDir + "VbaProject.CloneVbaProject.docm");
```

### Ayrıca bakınız

* class [VbaProject](../)
* ad alanı [Aspose.Words.Vba](../../vbaproject/)
* toplantı [Aspose.Words](../../../)


