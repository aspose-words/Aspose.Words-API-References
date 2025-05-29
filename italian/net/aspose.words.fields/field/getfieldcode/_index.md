---
title: Field.GetFieldCode
linktitle: GetFieldCode
articleTitle: GetFieldCode
second_title: Aspose.Words per .NET
description: Scopri il metodo GetFieldCode, recupera facilmente il testo tra l'inizio e il separatore del campo, inclusi i codici dei campi figlio e i risultati. Migliora la tua efficienza di programmazione!
type: docs
weight: 110
url: /it/net/aspose.words.fields/field/getfieldcode/
---
## GetFieldCode() {#getfieldcode}

Restituisce il testo tra l'inizio del campo e il separatore di campo (o la fine del campo se non c'è un separatore). Sono inclusi sia il codice di campo che il risultato del campo dei campi figlio.

```csharp
public string GetFieldCode()
```

## Esempi

Mostra come inserire un campo in un documento utilizzando un codice di campo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Field field = builder.InsertField("DATE \\@ \"dddd, MMMM dd, yyyy\"");

Assert.AreEqual(FieldType.FieldDate, field.Type);
Assert.AreEqual("DATE \\@ \"dddd, MMMM dd, yyyy\"", field.GetFieldCode());

// Questo sovraccarico del metodo InsertField aggiorna automaticamente i campi inseriti.
Assert.True((DateTime.Today - DateTime.Parse(field.Result)).Days <= 1);
```

Mostra come ottenere il codice di campo di un campo.

```csharp
// Apre un documento che contiene un MERGEFIELD all'interno di un campo IF.
Document doc = new Document(MyDir + "Nested fields.docx");
FieldIf fieldIf = (FieldIf)doc.Range.Fields[0];

// Esistono due modi per ottenere il codice di campo di un campo:
// 1 - Ometti i suoi campi interni:
Assert.AreEqual(" IF  > 0 \" (surplus of ) \" \"\" ", fieldIf.GetFieldCode(false));

// 2 - Includi i suoi campi interni:
Assert.AreEqual($" IF \u0013 MERGEFIELD NetIncome \u0014\u0015 > 0 \" (surplus of \u0013 MERGEFIELD  NetIncome \\f $ \u0014\u0015) \" \"\" ",
    fieldIf.GetFieldCode(true));

// Per impostazione predefinita, il metodo GetFieldCode visualizza i campi interni.
Assert.AreEqual(fieldIf.GetFieldCode(), fieldIf.GetFieldCode(true));
```

### Guarda anche

* class [Field](../)
* spazio dei nomi [Aspose.Words.Fields](../../../aspose.words.fields/)
* assemblea [Aspose.Words](../../../)

---

## GetFieldCode(*bool*) {#getfieldcode_1}

Restituisce il testo tra l'inizio del campo e il separatore di campo (o la fine del campo se non c'è separatore).

```csharp
public string GetFieldCode(bool includeChildFieldCodes)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| includeChildFieldCodes | Boolean | `VERO` se i codici dei campi figlio devono essere inclusi. |

## Esempi

Mostra come ottenere il codice di campo di un campo.

```csharp
// Apre un documento che contiene un MERGEFIELD all'interno di un campo IF.
Document doc = new Document(MyDir + "Nested fields.docx");
FieldIf fieldIf = (FieldIf)doc.Range.Fields[0];

// Esistono due modi per ottenere il codice di campo di un campo:
// 1 - Ometti i suoi campi interni:
Assert.AreEqual(" IF  > 0 \" (surplus of ) \" \"\" ", fieldIf.GetFieldCode(false));

// 2 - Includi i suoi campi interni:
Assert.AreEqual($" IF \u0013 MERGEFIELD NetIncome \u0014\u0015 > 0 \" (surplus of \u0013 MERGEFIELD  NetIncome \\f $ \u0014\u0015) \" \"\" ",
    fieldIf.GetFieldCode(true));

// Per impostazione predefinita, il metodo GetFieldCode visualizza i campi interni.
Assert.AreEqual(fieldIf.GetFieldCode(), fieldIf.GetFieldCode(true));
```

### Guarda anche

* class [Field](../)
* spazio dei nomi [Aspose.Words.Fields](../../../aspose.words.fields/)
* assemblea [Aspose.Words](../../../)
