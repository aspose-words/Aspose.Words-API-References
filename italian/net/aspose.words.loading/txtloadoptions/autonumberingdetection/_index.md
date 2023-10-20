---
title: TxtLoadOptions.AutoNumberingDetection
linktitle: AutoNumberingDetection
articleTitle: AutoNumberingDetection
second_title: Aspose.Words per .NET
description: TxtLoadOptions AutoNumberingDetection proprietà. Ottiene o imposta un valore booleano che indica che il rilevamento automatico della numerazione verrà eseguito durante il caricamento di un documento. Il valore predefinito èVERO  in C#.
type: docs
weight: 20
url: /it/net/aspose.words.loading/txtloadoptions/autonumberingdetection/
---
## TxtLoadOptions.AutoNumberingDetection property

Ottiene o imposta un valore booleano che indica che il rilevamento automatico della numerazione verrà eseguito durante il caricamento di un documento. Il valore predefinito è`VERO` .

```csharp
public bool AutoNumberingDetection { get; set; }
```

## Esempi

Mostra come disattivare il rilevamento automatico della numerazione.

```csharp
TxtLoadOptions options = new TxtLoadOptions { AutoNumberingDetection = false };
Document doc = new Document(MyDir + "Number detection.txt", options);
```

### Guarda anche

* class [TxtLoadOptions](../)
* spazio dei nomi [Aspose.Words.Loading](../../../aspose.words.loading/)
* assemblea [Aspose.Words](../../../)
