---
title: LayoutOptions.TextShaperFactory
second_title: Справочник по API Aspose.Words для .NET
description: LayoutOptions свойство. Получает или устанавливаетITextShaperFactory реализация используемая для функций рендеринга Advanced Typography.
type: docs
weight: 90
url: /ru/net/aspose.words.layout/layoutoptions/textshaperfactory/
---
## LayoutOptions.TextShaperFactory property

Получает или устанавливает[`ITextShaperFactory`](../../../aspose.words.shaping/itextshaperfactory/) реализация, используемая для функций рендеринга Advanced Typography.

```csharp
public ITextShaperFactory TextShaperFactory { get; set; }
```

### Примеры

Показывает, как поддерживать функции OpenType с помощью механизма формирования текста HarfBuzz.

```csharp
Document doc = new Document(MyDir + "OpenType text shaping.docx");

// Aspose.Words может использовать внешние объекты формирователя текста,
// которые представляют шрифты и вычисляют информацию о формировании текста.
// Фабрика формирователя текста необходима для документов, использующих несколько шрифтов.
// При заводских настройках формирователя текста в макете используются функции OpenType.
// Свойство Instance возвращает статический объект BasicTextShaperCache, обертывающий HarfBuzzTextShaperFactory.
doc.LayoutOptions.TextShaperFactory = HarfBuzzTextShaperFactory.Instance;

// В настоящее время выполняется формирование текста при экспорте в форматы PDF или XPS.
doc.Save(ArtifactsDir + "Document.OpenType.pdf");
```

### Смотрите также

* interface [ITextShaperFactory](../../../aspose.words.shaping/itextshaperfactory/)
* class [LayoutOptions](../)
* пространство имен [Aspose.Words.Layout](../../layoutoptions/)
* сборка [Aspose.Words](../../../)


