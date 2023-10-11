---
title: FieldOptions.PreProcessCulture
second_title: Aspose.Words per .NET API Reference
description: FieldOptions proprietà. Ottiene o imposta le impostazioni cultura per preelaborare i valori dei campi.
type: docs
weight: 170
url: /it/net/aspose.words.fields/fieldoptions/preprocessculture/
---
## FieldOptions.PreProcessCulture property

Ottiene o imposta le impostazioni cultura per preelaborare i valori dei campi.

```csharp
public CultureInfo PreProcessCulture { get; set; }
```

### Osservazioni

Attualmente questa proprietà influisce solo sul valore del[`FieldDocProperty`](../../fielddocproperty/) campo.

Il valore predefinito è`nullo` . Quando questa proprietà è impostata su`nullo` , IL[`FieldDocProperty`](../../fielddocproperty/)il valore del campo è preprocessed con la lingua controllata da[`FieldUpdateCultureSource`](../fieldupdateculturesource/) proprietà.

### Esempi

Mostra come impostare la cultura di preelaborazione.

```csharp
Document doc = new Document(MyDir + "Document.docx");
DocumentBuilder builder = new DocumentBuilder(doc);

// Imposta la cultura in base alla quale alcuni campi formatteranno i valori visualizzati.
doc.FieldOptions.PreProcessCulture = new CultureInfo("de-DE");

Field field = builder.InsertField(" DOCPROPERTY CreateTime");

// Il campo DOCPROPERTY visualizzerà il risultato formattato in base alla cultura del preprocesso
// abbiamo impostato il tedesco. Il campo visualizzerà la data/ora utilizzando il formato "gg.mm.aaaa hh:mm".
Assert.IsTrue(Regex.Match(field.Result, @"\d{2}[.]\d{2}[.]\d{4} \d{2}[:]\d{2}").Success);

doc.FieldOptions.PreProcessCulture = CultureInfo.InvariantCulture;
field.Update();

// Dopo il passaggio alle impostazioni cultura invarianti, il campo DOCPROPERTY utilizzerà il formato "mm/gg/aaaa hh:mm".
Assert.IsTrue(Regex.Match(field.Result, @"\d{2}[/]\d{2}[/]\d{4} \d{2}[:]\d{2}").Success);
```

### Guarda anche

* class [FieldOptions](../)
* spazio dei nomi [Aspose.Words.Fields](../../fieldoptions/)
* assemblea [Aspose.Words](../../../)


