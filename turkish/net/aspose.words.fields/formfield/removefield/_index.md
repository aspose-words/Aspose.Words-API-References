---
title: FormField.RemoveField
linktitle: RemoveField
articleTitle: RemoveField
second_title: .NET için Aspose.Words
description: FormField RemoveField yöntemi ile tüm form alanlarını zahmetsizce kaldırın, belgenizin netliğini ve organizasyonunu artırın.
type: docs
weight: 240
url: /tr/net/aspose.words.fields/formfield/removefield/
---
## FormField.RemoveField method

Sadece form alanı özel karakterini değil, tüm form alanını kaldırır.

```csharp
public void RemoveField()
```

## Notlar

Form alanıyla ilişkili bir yer imi varsa, yer imi kaldırılmaz.

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
