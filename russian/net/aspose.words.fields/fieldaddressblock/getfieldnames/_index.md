---
title: FieldAddressBlock.GetFieldNames
linktitle: GetFieldNames
articleTitle: GetFieldNames
second_title: Aspose.Words для .NET
description: Откройте для себя метод GetFieldNames в FieldAddressBlock. Легко извлекайте имена полей слияния, чтобы улучшить процесс автоматизации документов.
type: docs
weight: 70
url: /ru/net/aspose.words.fields/fieldaddressblock/getfieldnames/
---
## FieldAddressBlock.GetFieldNames method

Возвращает коллекцию имен полей слияния, используемых полем.

```csharp
public string[] GetFieldNames()
```

## Примеры

Показывает, как получить имена полей слияния, используемые полем.

```csharp
Document doc = new Document(MyDir + "Field sample - ADDRESSBLOCK.docx");

string[] addressFieldsExpect =
{
    "Company", "First Name", "Middle Name", "Last Name", "Suffix", "Address 1", "City", "State",
    "Country or Region", "Postal Code"
};

FieldAddressBlock addressBlockField = (FieldAddressBlock) doc.Range.Fields[0];
string[] addressBlockFieldNames = addressBlockField.GetFieldNames();
```

### Смотрите также

* class [FieldAddressBlock](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
