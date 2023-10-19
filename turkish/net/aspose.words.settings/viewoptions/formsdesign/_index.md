---
title: ViewOptions.FormsDesign
linktitle: FormsDesign
articleTitle: FormsDesign
second_title: Aspose.Words for .NET
description: ViewOptions FormsDesign mülk. Belgenin form tasarımı modunda olup olmadığını belirtir C#'da.
type: docs
weight: 30
url: /tr/net/aspose.words.settings/viewoptions/formsdesign/
---
## ViewOptions.FormsDesign property

Belgenin form tasarımı modunda olup olmadığını belirtir.

```csharp
public bool FormsDesign { get; set; }
```

## Notlar

Şu anda yalnızca WordML biçimindeki belgeler için çalışmaktadır.

## Örnekler

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
* ad alanı [Aspose.Words.Settings](../../../aspose.words.settings/)
* toplantı [Aspose.Words](../../../)
