---
title: FormField.RemoveField
linktitle: RemoveField
articleTitle: RemoveField
second_title: Aspose.Words per .NET
description: Rimuovi senza sforzo interi campi del modulo con il metodo RemoveField di FormField, migliorando la chiarezza e l'organizzazione del tuo documento.
type: docs
weight: 240
url: /it/net/aspose.words.fields/formfield/removefield/
---
## FormField.RemoveField method

Rimuove il campo modulo completo, non solo il carattere speciale del campo modulo.

```csharp
public void RemoveField()
```

## Osservazioni

Se al campo del modulo è associato un segnalibro, il segnalibro non viene rimosso.

## Esempi

Mostra come eliminare un campo del modulo.

```csharp
Document doc = new Document(MyDir + "Form fields.docx");

FormField formField = doc.Range.FormFields[3];
formField.RemoveField();
```

### Guarda anche

* class [FormField](../)
* spazio dei nomi [Aspose.Words.Fields](../../../aspose.words.fields/)
* assemblea [Aspose.Words](../../../)
