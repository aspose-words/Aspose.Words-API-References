---
title: FormField.RemoveField
linktitle: RemoveField
articleTitle: RemoveField
second_title: Aspose.Words for .NET
description: FormField RemoveField yöntem. Yalnızca form alanı özel karakterini değil tüm form alanını kaldırır C#'da.
type: docs
weight: 240
url: /tr/net/aspose.words.fields/formfield/removefield/
---
## FormField.RemoveField method

Yalnızca form alanı özel karakterini değil, tüm form alanını kaldırır.

```csharp
public void RemoveField()
```

## Notlar

Form alanıyla ilişkilendirilmiş bir yer imi varsa yer imi kaldırılmaz.

## Örnekler

Bir form alanının nasıl silineceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Form fields.docx");

FormField formField = doc.Range.FormFields[3];
formField.RemoveField();
```

### Ayrıca bakınız

* class [FormField](../)
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)
