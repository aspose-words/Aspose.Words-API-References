---
title: RemoveField
second_title: Aspose.Words per .NET API Reference
description: Rimuove il campo modulo completo non solo il carattere speciale del campo modulo.
type: docs
weight: 240
url: /it/net/aspose.words.fields/formfield/removefield/
---
## FormField.RemoveField method

Rimuove il campo modulo completo, non solo il carattere speciale del campo modulo.

```csharp
public void RemoveField()
```

### Osservazioni

Se è presente un segnalibro associato al campo del modulo, il segnalibro non viene rimosso.

### Esempi

Mostra come eliminare un campo modulo.

```csharp
Document doc = new Document(MyDir + "Form fields.docx");

FormField formField = doc.Range.FormFields[3];
formField.RemoveField();
```

### Guarda anche

* class [FormField](../../formfield)
* spazio dei nomi [Aspose.Words.Fields](../../formfield)
* assemblea [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
