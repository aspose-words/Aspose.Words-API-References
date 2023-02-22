---
title: ViewOptions.FormsDesign
second_title: Aspose.Words for .NET API Referansı
description: ViewOptions mülk. Belgenin form tasarım modunda olup olmadığını belirtir.
type: docs
weight: 30
url: /tr/net/aspose.words.settings/viewoptions/formsdesign/
---
## ViewOptions.FormsDesign property

Belgenin form tasarım modunda olup olmadığını belirtir.

```csharp
public bool FormsDesign { get; set; }
```

### Notlar

Şu anda yalnızca WordML biçimindeki belgeler için çalışır.

### Örnekler

Form tasarım modunun nasıl etkinleştirileceğini/devre dışı bırakılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Form tasarım modunu devre dışı bırakmak için "FormsDesign" özelliğini "false" olarak ayarlayın.
// Form tasarım modunu etkinleştirmek için "FormsDesign" özelliğini "true" olarak ayarlayın.
doc.ViewOptions.FormsDesign = useFormsDesign;

doc.Save(ArtifactsDir + "ViewOptions.FormsDesign.xml");

Assert.AreEqual(useFormsDesign,
    File.ReadAllText(ArtifactsDir + "ViewOptions.FormsDesign.xml").Contains("<w:formsDesign />"));
```

### Ayrıca bakınız

* class [ViewOptions](../)
* ad alanı [Aspose.Words.Settings](../../viewoptions/)
* toplantı [Aspose.Words](../../../)


