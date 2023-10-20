---
title: Range.UpdateFields
linktitle: UpdateFields
articleTitle: UpdateFields
second_title: Aspose.Words для .NET
description: Range UpdateFields метод. Обновляет значения полей документа в этом диапазоне на С#.
type: docs
weight: 120
url: /ru/net/aspose.words/range/updatefields/
---
## Range.UpdateFields method

Обновляет значения полей документа в этом диапазоне.

```csharp
public void UpdateFields()
```

## Примечания

Когда вы открываете, изменяете и затем сохраняете документ, Aspose.Words не обновляет поля автоматически, он сохраняет их нетронутыми. Поэтому обычно вам нужно вызвать этот метод перед сохранением, если вы изменили document программно и хотите убедиться, что правильные (вычисленные) значения полей появятся в сохраненном документе.

Нет необходимости обновлять поля после выполнения слияния почты, поскольку слияние почты является своего рода полем update и автоматически обновляет все поля в документе.

Этот метод не обновляет все типы полей. Подробный список поддерживаемых типов полей см. в Руководстве программиста.

Этот метод не обновляет поля, связанные с алгоритмами макета страницы (например, PAGE, PAGES, PAGEREF). Поля, связанные с макетом страницы, обновляются при визуализации документа или вызове.[`UpdatePageLayout`](../../document/updatepagelayout/).

Чтобы обновить поля во всем документе, используйте[`UpdateFields`](../../document/updatefields/).

## Примеры

Показывает, как обновить все поля в диапазоне.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertField(" DOCPROPERTY Category");
builder.InsertBreak(BreakType.SectionBreakEvenPage);
builder.InsertField(" DOCPROPERTY Category");

// В приведенных выше полях DOCPROPERTY будет отображаться значение этого встроенного свойства документа.
doc.BuiltInDocumentProperties.Category = "MyCategory";

// Если мы обновим значение свойства документа, нам нужно будет обновить все поля DOCPROPERTY, чтобы отобразить его.
Assert.AreEqual(string.Empty, doc.Range.Fields[0].Result);
Assert.AreEqual(string.Empty, doc.Range.Fields[1].Result);

// Обновляем все поля, находящиеся в диапазоне первого раздела.
doc.FirstSection.Range.UpdateFields();

Assert.AreEqual("MyCategory", doc.Range.Fields[0].Result);
Assert.AreEqual(string.Empty, doc.Range.Fields[1].Result);
```

### Смотрите также

* class [Range](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
