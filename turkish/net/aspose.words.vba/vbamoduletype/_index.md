---
title: Enum VbaModuleType
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Vba.VbaModuleType Sıralama. Bir VBA projesindeki modelin türünü belirtir.
type: docs
weight: 6260
url: /tr/net/aspose.words.vba/vbamoduletype/
---
## VbaModuleType enumeration

Bir VBA projesindeki modelin türünü belirtir.

```csharp
public enum VbaModuleType
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| DocumentModule | `0` | Bir belgeyle ilişkilendirilmiş gömülü makrolar ve programlı erişim işlemleri için bir modül belirten bir VBA proje öğesi türü . |
| ProceduralModule | `1` | Alt yordamlar ve işlevler koleksiyonu. |
| ClassModule | `2` | Yeni bir nesnenin tanımını içeren bir modül. Bir sınıfın her örneği yeni bir nesne oluşturur, ve modülde tanımlanan prosedürler nesnenin özellikleri ve yöntemleri olur. |
| DesignerModule | `3` | Projeye kayıtlı bir ActiveX denetiminin yöntemlerini ve özelliklerini genişleten bir VBA modülü. |

### Örnekler

Makroları kullanarak bir VBA projesinin nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();

// Yeni bir VBA projesi oluşturun.
VbaProject project = new VbaProject();
project.Name = "Aspose.Project";
doc.VbaProject = project;

// Yeni bir modül oluşturun ve bir makro kaynak kodu belirleyin.
VbaModule module = new VbaModule();
module.Name = "Aspose.Module";
module.Type = VbaModuleType.ProceduralModule;
module.SourceCode = "New source code";

// Modülü VBA projesine ekleyin.
doc.VbaProject.Modules.Add(module);

doc.Save(ArtifactsDir + "VbaProject.CreateVBAMacros.docm");
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Vba](../../aspose.words.vba/)
* toplantı [Aspose.Words](../../)


