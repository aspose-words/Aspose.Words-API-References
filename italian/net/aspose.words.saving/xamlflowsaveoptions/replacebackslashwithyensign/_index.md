---
title: XamlFlowSaveOptions.ReplaceBackslashWithYenSign
linktitle: ReplaceBackslashWithYenSign
articleTitle: ReplaceBackslashWithYenSign
second_title: Aspose.Words per .NET
description: Scopri come la proprietà ReplaceBackslashWithYenSign di XamlFlowSaveOptions migliora la formattazione dei dati convertendo le barre rovesciate nel simbolo dello yen. Valore predefinito: false.
type: docs
weight: 50
url: /it/net/aspose.words.saving/xamlflowsaveoptions/replacebackslashwithyensign/
---
## XamlFlowSaveOptions.ReplaceBackslashWithYenSign property

Specifica se i caratteri barra rovesciata devono essere sostituiti con il segno yen. Il valore predefinito è`falso` .

```csharp
public bool ReplaceBackslashWithYenSign { get; set; }
```

## Osservazioni

Per impostazione predefinita, Aspose.Words imita il comportamento di MS Word e non sostituisce i caratteri barra rovesciata con il simbolo yen nei documenti XAML generati. Tuttavia, le versioni precedenti di Aspose.Words eseguivano tali sostituzioni in alcuni scenari. Questo flag consente la retrocompatibilità con le versioni precedenti di Aspose.Words.

## Esempi

Mostra come sostituire i caratteri barra rovesciata con il simbolo yen (Xaml).

```csharp
Document doc = new Document(MyDir + "Korean backslash symbol.docx");

// Per impostazione predefinita, Aspose.Words imita il comportamento di MS Word e non sostituisce i caratteri barra rovesciata con il segno di yen in
// documenti HTML generati. Tuttavia, le versioni precedenti di Aspose.Words eseguivano tali sostituzioni in alcuni
// scenari. Questo flag consente la retrocompatibilità con le versioni precedenti di Aspose.Words.
XamlFlowSaveOptions saveOptions = new XamlFlowSaveOptions();
saveOptions.ReplaceBackslashWithYenSign = true;

doc.Save(ArtifactsDir + "HtmlSaveOptions.ReplaceBackslashWithYenSign.xaml", saveOptions);
```

### Guarda anche

* class [XamlFlowSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
