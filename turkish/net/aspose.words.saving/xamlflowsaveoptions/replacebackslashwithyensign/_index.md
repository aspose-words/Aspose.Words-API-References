---
title: XamlFlowSaveOptions.ReplaceBackslashWithYenSign
linktitle: ReplaceBackslashWithYenSign
articleTitle: ReplaceBackslashWithYenSign
second_title: .NET için Aspose.Words
description: XamlFlowSaveOptions' ReplaceBackslashWithYenSign özelliğinin ters eğik çizgileri yen işaretlerine dönüştürerek veri biçimlendirmenizi nasıl geliştirdiğini keşfedin. Varsayılan, false.
type: docs
weight: 50
url: /tr/net/aspose.words.saving/xamlflowsaveoptions/replacebackslashwithyensign/
---
## XamlFlowSaveOptions.ReplaceBackslashWithYenSign property

Ters eğik çizgi karakterlerinin yen işaretleriyle değiştirilip değiştirilmeyeceğini belirtir. Varsayılan değer`YANLIŞ` .

```csharp
public bool ReplaceBackslashWithYenSign { get; set; }
```

## Notlar

Varsayılan olarak, Aspose.Words MS Word'ün davranışını taklit eder ve ters eğik çizgi karakterlerini oluşturulan XAML belgelerinde yen işaretleriyle değiştirmez. Ancak, Aspose.Words'ün önceki sürümleri belirli senaryolarında bu tür değiştirmeler gerçekleştirmiştir. Bu bayrak, Aspose.Words'ün önceki sürümleriyle geriye dönük uyumluluğu etkinleştirir.

## Örnekler

Ters eğik çizgi karakterlerinin yen işaretleriyle nasıl değiştirileceğini gösterir (Xaml).

```csharp
Document doc = new Document(MyDir + "Korean backslash symbol.docx");

// Varsayılan olarak, Aspose.Words MS Word'ün davranışını taklit eder ve ters eğik çizgi karakterlerini yen işaretleriyle değiştirmez.
// HTML belgeleri oluşturuldu. Ancak, Aspose.Words'ün önceki sürümleri bu tür değişiklikleri belirli durumlarda gerçekleştirdi
// senaryolar. Bu bayrak Aspose.Words'ün önceki sürümleriyle geriye dönük uyumluluğu etkinleştirir.
XamlFlowSaveOptions saveOptions = new XamlFlowSaveOptions();
saveOptions.ReplaceBackslashWithYenSign = true;

doc.Save(ArtifactsDir + "HtmlSaveOptions.ReplaceBackslashWithYenSign.xaml", saveOptions);
```

### Ayrıca bakınız

* class [XamlFlowSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
