---
title: Style.BuiltIn
linktitle: BuiltIn
articleTitle: BuiltIn
second_title: Aspose.Words per .NET
description: Scopri se uno stile è un'opzione integrata in MS Word. Migliora il design dei tuoi documenti con la nostra guida completa agli stili integrati di Word!
type: docs
weight: 40
url: /it/net/aspose.words/style/builtin/
---
## Style.BuiltIn property

Vero se questo stile è uno degli stili predefiniti in MS Word.

```csharp
public bool BuiltIn { get; }
```

## Esempi

Mostra come distinguere gli stili personalizzati dagli stili predefiniti.

```csharp
Document doc = new Document();

// Quando creiamo un documento utilizzando Microsoft Word o a livello di programmazione utilizzando Aspose.Words,
// il documento verrà fornito con una raccolta di stili da applicare al testo per modificarne l'aspetto.
// Possiamo accedere a questi stili incorporati tramite la raccolta "Stili" del documento.
// Tutti questi stili avranno il flag "BuiltIn" impostato su "true".
Style style = doc.Styles["Emphasis"];

Assert.True(style.BuiltIn);

// Crea uno stile personalizzato e aggiungilo alla collezione.
 // Stili personalizzati come questo avranno il flag "BuiltIn" impostato su "false".
style = doc.Styles.Add(StyleType.Character, "MyStyle");
style.Font.Color = Color.Navy;
style.Font.Name = "Courier New";

Assert.False(style.BuiltIn);
```

### Guarda anche

* class [Style](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
