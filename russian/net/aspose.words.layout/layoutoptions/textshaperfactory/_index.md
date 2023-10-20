---
title: LayoutOptions.TextShaperFactory
linktitle: TextShaperFactory
articleTitle: TextShaperFactory
second_title: Aspose.Words для .NET
description: LayoutOptions TextShaperFactory свойство. Получает или устанавливаетITextShaperFactory реализация используемая для функций рендеринга расширенной типографики на С#.
type: docs
weight: 100
url: /ru/net/aspose.words.layout/layoutoptions/textshaperfactory/
---
## LayoutOptions.TextShaperFactory property

Получает или устанавливает[`ITextShaperFactory`](../../../aspose.words.shaping/itextshaperfactory/) реализация, используемая для функций рендеринга расширенной типографики.

```csharp
public ITextShaperFactory TextShaperFactory { get; set; }
```

## Примеры

Показывает, как поддерживать функции OpenType с помощью механизма формирования текста HarfBuzz.

```csharp
Document doc = new Document(MyDir + "OpenType text shaping.docx");

// Aspose.Words может использовать внешние объекты формирователя текста,
// которые представляют шрифты и вычисляют информацию о формировании текста.
// Фабрика формирователя текста необходима для документов, использующих несколько шрифтов.
// Когда установлен заводской формирователь текста, макет использует функции OpenType.
// Свойство Instance возвращает статический объект BasicTextShaperCache, обертывающий HarfBuzzTextShaperFactory.
doc.LayoutOptions.TextShaperFactory = HarfBuzzTextShaperFactory.Instance;

// В настоящее время формирование текста выполняется при экспорте в форматы PDF или XPS.
doc.Save(ArtifactsDir + "Document.OpenType.pdf");
```

### Смотрите также

* interface [ITextShaperFactory](../../../aspose.words.shaping/itextshaperfactory/)
* class [LayoutOptions](../)
* пространство имен [Aspose.Words.Layout](../../../aspose.words.layout/)
* сборка [Aspose.Words](../../../)
