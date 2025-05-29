---
title: FormField.RemoveField
linktitle: RemoveField
articleTitle: RemoveField
second_title: Aspose.Words für .NET
description: Entfernen Sie mühelos ganze Formularfelder mit der FormField RemoveField-Methode und verbessern Sie so die Übersichtlichkeit und Organisation Ihres Dokuments.
type: docs
weight: 240
url: /de/net/aspose.words.fields/formfield/removefield/
---
## FormField.RemoveField method

Entfernt das komplette Formularfeld, nicht nur die Sonderzeichen im Formularfeld.

```csharp
public void RemoveField()
```

## Bemerkungen

Wenn dem Formularfeld ein Lesezeichen zugeordnet ist, wird das Lesezeichen nicht entfernt.

## Beispiele

Zeigt, wie ein Formularfeld gelöscht wird.

```csharp
Document doc = new Document(MyDir + "Form fields.docx");

FormField formField = doc.Range.FormFields[3];
formField.RemoveField();
```

### Siehe auch

* class [FormField](../)
* namensraum [Aspose.Words.Fields](../../../aspose.words.fields/)
* Montage [Aspose.Words](../../../)
