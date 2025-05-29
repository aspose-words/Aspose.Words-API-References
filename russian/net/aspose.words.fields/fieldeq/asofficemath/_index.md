---
title: FieldEQ.AsOfficeMath
linktitle: AsOfficeMath
articleTitle: AsOfficeMath
second_title: Aspose.Words для .NET
description: Преобразуйте поля EQ с помощью метода AsOfficeMath FieldEQ, легко преобразуя их в объекты Office Math для бесшовной интеграции документов.
type: docs
weight: 20
url: /ru/net/aspose.words.fields/fieldeq/asofficemath/
---
## FieldEQ.AsOfficeMath method

Возвращает объект Office Math, соответствующий полю EQ.

```csharp
public OfficeMath AsOfficeMath()
```

### Возвращаемое значение

Возврат`нулевой` если код поля пуст или недействителен, в противном случае[`OfficeMath`](../../../aspose.words.math/officemath/) экземпляр.

## Примеры

Показывает, как заменить поле EQ на Office Math.

```csharp
Document doc = new Document(MyDir + "Field sample - EQ.docx");
FieldEQ fieldEQ = doc.Range.Fields.OfType<FieldEQ>().First();

OfficeMath officeMath = fieldEQ.AsOfficeMath();

fieldEQ.Start.ParentNode.InsertBefore(officeMath, fieldEQ.Start);
fieldEQ.Remove();

doc.Save(ArtifactsDir + "Field.EQAsOfficeMath.docx");
```

### Смотрите также

* class [OfficeMath](../../../aspose.words.math/officemath/)
* class [FieldEQ](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
