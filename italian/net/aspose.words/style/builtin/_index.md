---
title: Style.BuiltIn
second_title: Aspose.Words per .NET API Reference
description: Style proprietà. Vero se questo stile è uno degli stili incorporati in MS Word.
type: docs
weight: 40
url: /it/net/aspose.words/style/builtin/
---
## Style.BuiltIn property

Vero se questo stile è uno degli stili incorporati in MS Word.

```csharp
public bool BuiltIn { get; }
```

### Esempi

Mostra come differenziare gli stili personalizzati dagli stili incorporati.

```csharp
Document doc = new Document();

// Quando creiamo un documento utilizzando Microsoft Word o a livello di codice utilizzando Aspose.Words,
// il documento verrà fornito con una raccolta di stili da applicare al testo per modificarne l'aspetto.
// Possiamo accedere a questi stili integrati tramite la raccolta "Stili" del documento.
// Questi stili avranno tutti il flag "BuiltIn" impostato su "true".
Style style = doc.Styles["Emphasis"];

Assert.True(style.BuiltIn);

// Crea uno stile personalizzato e aggiungilo alla raccolta.
// Gli stili personalizzati come questo avranno il flag "BuiltIn" impostato su "false".
style = doc.Styles.Add(StyleType.Character, "MyStyle");
style.Font.Color = Color.Navy;
style.Font.Name = "Courier New";

Assert.False(style.BuiltIn);
```

### Guarda anche

* class [Style](../)
* spazio dei nomi [Aspose.Words](../../style/)
* assemblea [Aspose.Words](../../../)


