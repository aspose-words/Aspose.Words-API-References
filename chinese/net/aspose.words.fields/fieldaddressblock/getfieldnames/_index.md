---
title: FieldAddressBlock.GetFieldNames
linktitle: GetFieldNames
articleTitle: GetFieldNames
second_title: Aspose.Words for .NET
description: 探索 FieldAddressBlock 中的 GetFieldNames 方法。轻松检索邮件合并字段名称，增强您的文档自动化流程。
type: docs
weight: 70
url: /zh/net/aspose.words.fields/fieldaddressblock/getfieldnames/
---
## FieldAddressBlock.GetFieldNames method

返回该字段使用的邮件合并字段名称的集合。

```csharp
public string[] GetFieldNames()
```

## 例子

显示如何获取字段使用的邮件合并字段名称。

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

### 也可以看看

* class [FieldAddressBlock](../)
* 命名空间 [Aspose.Words.Fields](../../../aspose.words.fields/)
* 部件 [Aspose.Words](../../../)
