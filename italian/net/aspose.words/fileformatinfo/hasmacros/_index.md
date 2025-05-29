---
title: FileFormatInfo.HasMacros
linktitle: HasMacros
articleTitle: HasMacros
second_title: Aspose.Words per .NET
description: Scopri se il tuo documento include macro VBA con la proprietà FileFormatInfo HasMacros. Garantisci la sicurezza e la funzionalità del documento oggi stesso!
type: docs
weight: 30
url: /it/net/aspose.words/fileformatinfo/hasmacros/
---
## FileFormatInfo.HasMacros property

Restituisce`VERO` se questo documento contiene macro VBA.

```csharp
public bool HasMacros { get; }
```

## Esempi

Mostra come verificare la presenza di macro VBA senza caricare il documento.

```csharp
FileFormatInfo fileFormatInfo = FileFormatUtil.DetectFileFormat(MyDir + "Macro.docm");
Assert.IsTrue(fileFormatInfo.HasMacros);
```

### Guarda anche

* class [FileFormatInfo](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
