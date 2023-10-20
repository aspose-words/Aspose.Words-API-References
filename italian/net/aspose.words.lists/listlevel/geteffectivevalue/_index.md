---
title: ListLevel.GetEffectiveValue
linktitle: GetEffectiveValue
articleTitle: GetEffectiveValue
second_title: Aspose.Words per .NET
description: ListLevel GetEffectiveValue metodo. Riporta la rappresentazione in stringa del fileListLeveloggetto per lindice specificato dellelemento dellelenco. I parametri specificano ilNumberStyle e un formato opzionale string utilizzato quandoCustom è specificato in C#.
type: docs
weight: 190
url: /it/net/aspose.words.lists/listlevel/geteffectivevalue/
---
## ListLevel.GetEffectiveValue method

Riporta la rappresentazione in stringa del file[`ListLevel`](../)oggetto per l'indice specificato dell'elemento dell'elenco. I parametri specificano il[`NumberStyle`](../../../aspose.words/numberstyle/) e un formato opzionale string utilizzato quandoCustom è specificato.

```csharp
public static string GetEffectiveValue(int index, NumberStyle numberStyle, 
    string customNumberStyleFormat)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| index | Int32 | L'indice dell'elemento dell'elenco (deve essere compreso tra 1 e 32767). |
| numberStyle | NumberStyle | Il[`NumberStyle`](../../../aspose.words/numberstyle/) del[`ListLevel`](../) oggetto. |
| customNumberStyleFormat | String | La stringa di formato opzionale utilizzata quandoCustom è specificato (es. "a, ç, ĝ, ..."). Negli altri casi questo parametro deve essere`nullo` o vuoto. |

### Valore di ritorno

La rappresentazione di stringa di[`ListLevel`](../) oggetto, descritto da*numberStyle* parametro e il*customNumberStyleFormat* parametro, nella voce di elenco nella posizione determinata dal*index* parametro.

### Eccezioni

| eccezione | condizione |
| --- | --- |
| ArgumentException | *customNumberStyleFormat* È`nullo` o vuoto quando il*numberStyle* è personalizzato.-o- *customNumberStyleFormat* non è`nullo` o vuoto quando il*numberStyle* non è personalizzato.-o- *customNumberStyleFormat* non è valido. |
| ArgumentOutOfRangeException | l'indice è fuori intervallo. |

## Esempi

Mostra come ottenere il formato di un elenco con lo stile numero personalizzato.

```csharp
Document doc = new Document(MyDir + "List with leading zero.docx");

ListLevel listLevel = doc.FirstSection.Body.Paragraphs[0].ListFormat.ListLevel;

string customNumberStyleFormat = string.Empty;

if (listLevel.NumberStyle == NumberStyle.Custom)
    customNumberStyleFormat = listLevel.CustomNumberStyleFormat;

Assert.AreEqual("001, 002, 003, ...", customNumberStyleFormat);

// Possiamo ottenere il valore per l'indice specificato dell'elemento dell'elenco.
Assert.AreEqual("iv", ListLevel.GetEffectiveValue(4, NumberStyle.LowercaseRoman, null));
Assert.AreEqual("005", ListLevel.GetEffectiveValue(5, NumberStyle.Custom, customNumberStyleFormat));
```

### Guarda anche

* enum [NumberStyle](../../../aspose.words/numberstyle/)
* class [ListLevel](../)
* spazio dei nomi [Aspose.Words.Lists](../../../aspose.words.lists/)
* assemblea [Aspose.Words](../../../)
