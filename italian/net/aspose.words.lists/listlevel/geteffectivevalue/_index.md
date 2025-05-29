---
title: ListLevel.GetEffectiveValue
linktitle: GetEffectiveValue
articleTitle: GetEffectiveValue
second_title: Aspose.Words per .NET
description: Scopri il metodo GetEffectiveValue di ListLevel per recuperare facilmente le rappresentazioni stringa degli elementi di un elenco. Personalizza con NumberStyle e opzioni di formato!
type: docs
weight: 190
url: /it/net/aspose.words.lists/listlevel/geteffectivevalue/
---
## ListLevel.GetEffectiveValue method

Segnala la rappresentazione in formato stringa del[`ListLevel`](../)oggetto per l'indice specificato dell'elemento dell'elenco. I parametri specificano l'[`NumberStyle`](../../../aspose.words/numberstyle/) e una stringa di formato opzionale utilizzata quandoCustom è specificato.

```csharp
public static string GetEffectiveValue(int index, NumberStyle numberStyle, 
    string customNumberStyleFormat)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| index | Int32 | L'indice dell'elemento dell'elenco (deve essere compreso tra 1 e 32767). |
| numberStyle | NumberStyle | Il[`NumberStyle`](../../../aspose.words/numberstyle/) del[`ListLevel`](../) oggetto. |
| customNumberStyleFormat | String | La stringa di formato facoltativa utilizzata quandoCustom è specificato (ad esempio "a, ç, ĝ, ..."). In altri casi, questo parametro deve essere`null` o vuoto. |

### Valore di ritorno

La rappresentazione della stringa[`ListLevel`](../) oggetto, descritto dal*numberStyle* parametro and il*customNumberStyleFormat* parametro, nell'elemento dell'elenco nella posizione determinata dal*index* parametro.

### Eccezioni

| eccezione | condizione |
| --- | --- |
| ArgumentException | *customNumberStyleFormat* È`null` o vuoto quando il*numberStyle* è personalizzato.-o- *customNumberStyleFormat* non è`null` o vuoto quando il*numberStyle* non è personalizzato.-o- *customNumberStyleFormat* non è valido. |
| ArgumentOutOfRangeException | l'indice è fuori intervallo. |

## Esempi

Mostra come ottenere il formato per un elenco con lo stile numerico personalizzato.

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
