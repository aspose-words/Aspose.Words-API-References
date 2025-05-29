---
title: FieldOptions.PreProcessCulture
linktitle: PreProcessCulture
articleTitle: PreProcessCulture
second_title: Aspose.Words per .NET
description: Scopri come FieldOptions PreProcessCulture migliora l'elaborazione dei dati personalizzando le culture dei valori dei campi per una maggiore accuratezza ed efficienza.
type: docs
weight: 170
url: /it/net/aspose.words.fields/fieldoptions/preprocessculture/
---
## FieldOptions.PreProcessCulture property

Ottiene o imposta la cultura per preelaborare i valori dei campi.

```csharp
public CultureInfo PreProcessCulture { get; set; }
```

## Osservazioni

Attualmente questa proprietà influisce solo sul valore dell'[`FieldDocProperty`](../../fielddocproperty/) campo.

Il valore predefinito è`null` Quando questa proprietà è impostata su`null` , IL[`FieldDocProperty`](../../fielddocproperty/) il valore del campo è preprocessed con la cultura controllata da[`FieldUpdateCultureSource`](../fieldupdateculturesource/) proprietà.

## Esempi

Mostra come impostare la cultura di pre-elaborazione.

```csharp
Document doc = new Document(MyDir + "Document.docx");
DocumentBuilder builder = new DocumentBuilder(doc);

// Imposta la cultura in base alla quale alcuni campi formatteranno i loro valori visualizzati.
doc.FieldOptions.PreProcessCulture = new CultureInfo("de-DE");

Field field = builder.InsertField(" DOCPROPERTY CreateTime");

// Il campo DOCPROPERTY visualizzerà il risultato formattato in base alla cultura di pre-elaborazione
// abbiamo impostato il tedesco. Il campo visualizzerà la data/ora nel formato "gg.mm.aaaa hh:mm".
Assert.IsTrue(Regex.Match(field.Result, @"\d{2}[.]\d{2}[.]\d{4} \d{2}[:]\d{2}").Success);

doc.FieldOptions.PreProcessCulture = CultureInfo.InvariantCulture;
field.Update();

// Dopo il passaggio alla cultura invariante, il campo DOCPROPERTY utilizzerà il formato "mm/gg/aaaa hh:mm".
Assert.IsTrue(Regex.Match(field.Result, @"\d{2}[/]\d{2}[/]\d{4} \d{2}[:]\d{2}").Success);
```

### Guarda anche

* class [FieldOptions](../)
* spazio dei nomi [Aspose.Words.Fields](../../../aspose.words.fields/)
* assemblea [Aspose.Words](../../../)
