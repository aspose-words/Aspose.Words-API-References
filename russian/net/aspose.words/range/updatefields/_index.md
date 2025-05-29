---
title: Range.UpdateFields
linktitle: UpdateFields
articleTitle: UpdateFields
second_title: Aspose.Words для .NET
description: Улучшайте свои документы без особых усилий с помощью метода Range UpdateFields, который быстро и эффективно обновляет значения полей для повышения точности.
type: docs
weight: 130
url: /ru/net/aspose.words/range/updatefields/
---
## Range.UpdateFields method

Обновляет значения полей документа в этом диапазоне.

```csharp
public void UpdateFields()
```

## Примечания

Когда вы открываете, изменяете и затем сохраняете документ, Aspose.Words не обновляет поля автоматически, а сохраняет их нетронутыми. Поэтому обычно вам нужно вызвать этот метод перед сохранением, если вы изменили document программно и хотите убедиться, что в сохраненном документе отображаются правильные (вычисленные) значения полей.

После выполнения слияния почты нет необходимости обновлять поля, поскольку слияние почты является разновидностью обновления полей и автоматически обновляет все поля в документе.

Этот метод не обновляет все типы полей. Подробный список поддерживаемых типов полей см. в Руководстве программиста.

Этот метод не обновляет поля, связанные с алгоритмами макета страницы (например, PAGE, PAGES, PAGEREF). Поля, связанные с макетом страницы, обновляются при отображении документа или вызове[`UpdatePageLayout`](../../document/updatepagelayout/).

Для обновления полей во всем документе используйте[`UpdateFields`](../../document/updatefields/).

## Примеры

Показывает, как обновить все поля в диапазоне.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertField(" DOCPROPERTY Category");
builder.InsertBreak(BreakType.SectionBreakEvenPage);
builder.InsertField(" DOCPROPERTY Category");

// Вышеуказанные поля DOCPROPERTY будут отображать значение этого встроенного свойства документа.
doc.BuiltInDocumentProperties.Category = "MyCategory";

// Если мы обновим значение свойства документа, нам потребуется обновить все поля DOCPROPERTY, чтобы отобразить его.
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
