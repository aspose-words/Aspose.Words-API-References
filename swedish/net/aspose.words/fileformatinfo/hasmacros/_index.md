---
title: FileFormatInfo.HasMacros
linktitle: HasMacros
articleTitle: HasMacros
second_title: Aspose.Words för .NET
description: Ta reda på om ditt dokument innehåller VBA-makron med egenskapen FileFormatInfo HasMacros. Säkerställ dokumentsäkerhet och funktionalitet idag!
type: docs
weight: 30
url: /sv/net/aspose.words/fileformatinfo/hasmacros/
---
## FileFormatInfo.HasMacros property

Returer`sann` om det här dokumentet innehåller VBA-makro.

```csharp
public bool HasMacros { get; }
```

## Exempel

Visar hur man kontrollerar närvaron av VBA-makro utan att ladda dokumentet.

```csharp
FileFormatInfo fileFormatInfo = FileFormatUtil.DetectFileFormat(MyDir + "Macro.docm");
Assert.IsTrue(fileFormatInfo.HasMacros);
```

### Se även

* class [FileFormatInfo](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
