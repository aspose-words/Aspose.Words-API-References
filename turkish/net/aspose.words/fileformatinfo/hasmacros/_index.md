---
title: FileFormatInfo.HasMacros
linktitle: HasMacros
articleTitle: HasMacros
second_title: .NET için Aspose.Words
description: Belgenizin FileFormatInfo HasMacros özelliğiyle VBA makroları içerip içermediğini keşfedin. Belge güvenliğini ve işlevselliğini bugün sağlayın!
type: docs
weight: 30
url: /tr/net/aspose.words/fileformatinfo/hasmacros/
---
## FileFormatInfo.HasMacros property

Geri Döndürür`doğru` eğer bu belge bir VBA makrosu içeriyorsa.

```csharp
public bool HasMacros { get; }
```

## Örnekler

Belgeyi yüklemeden VBA makro varlığının nasıl kontrol edileceğini gösterir.

```csharp
FileFormatInfo fileFormatInfo = FileFormatUtil.DetectFileFormat(MyDir + "Macro.docm");
Assert.IsTrue(fileFormatInfo.HasMacros);
```

### Ayrıca bakınız

* class [FileFormatInfo](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
