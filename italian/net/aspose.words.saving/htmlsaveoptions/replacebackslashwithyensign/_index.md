---
title: HtmlSaveOptions.ReplaceBackslashWithYenSign
linktitle: ReplaceBackslashWithYenSign
articleTitle: ReplaceBackslashWithYenSign
second_title: Aspose.Words per .NET
description: Scopri come la proprietà HtmlSaveOptions ReplaceBackslashWithYenSign migliora l'output HTML convertendo le barre rovesciate nel simbolo dello yen. Valore predefinito false.
type: docs
weight: 420
url: /it/net/aspose.words.saving/htmlsaveoptions/replacebackslashwithyensign/
---
## HtmlSaveOptions.ReplaceBackslashWithYenSign property

Specifica se i caratteri barra rovesciata devono essere sostituiti con il segno yen. Il valore predefinito è`falso` .

```csharp
public bool ReplaceBackslashWithYenSign { get; set; }
```

## Osservazioni

Per impostazione predefinita, Aspose.Words imita il comportamento di MS Word e non sostituisce i caratteri barra rovesciata con il simbolo dello yen nei documenti HTML generati. Tuttavia, le versioni precedenti di Aspose.Words eseguivano tali sostituzioni in alcuni scenari. Questo flag consente la retrocompatibilità con le versioni precedenti di Aspose.Words.

## Esempi

Mostra come sostituire i caratteri barra rovesciata con il simbolo yen (Html).

```csharp
Document doc = new Document(MyDir + "Korean backslash symbol.docx");

// Per impostazione predefinita, Aspose.Words imita il comportamento di MS Word e non sostituisce i caratteri barra rovesciata con il segno di yen in
// documenti HTML generati. Tuttavia, le versioni precedenti di Aspose.Words eseguivano tali sostituzioni in alcuni
// scenari. Questo flag consente la retrocompatibilità con le versioni precedenti di Aspose.Words.
HtmlSaveOptions saveOptions = new HtmlSaveOptions();
saveOptions.ReplaceBackslashWithYenSign = true;

doc.Save(ArtifactsDir + "HtmlSaveOptions.ReplaceBackslashWithYenSign.html", saveOptions);
```

### Guarda anche

* class [HtmlSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
