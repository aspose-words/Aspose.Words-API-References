---
title: LayoutOptions.TextShaperFactory
linktitle: TextShaperFactory
articleTitle: TextShaperFactory
second_title: Aspose.Words для .NET
description: Откройте для себя свойство LayoutOptions TextShaperFactory для расширенной типографики. Улучшите рендеринг с помощью настраиваемых реализаций ITextShaperFactory.
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

Демонстрирует, как поддерживать функции OpenType с помощью движка формирования текста HarfBuzz.

```csharp
Document doc = new Document(MyDir + "OpenType text shaping.docx");

// Aspose.Words может использовать внешние объекты текстового формирователя,
// которые представляют шрифты и вычисляют информацию о форме текста.
// Фабрика формирователей текста необходима для документов, использующих несколько шрифтов.
// При заводской настройке формирователя текста макет использует функции OpenType.
// Свойство Instance возвращает статический объект BasicTextShaperCache, оборачивающий HarfBuzzTextShaperFactory.
doc.LayoutOptions.TextShaperFactory = HarfBuzzTextShaperFactory.Instance;

// В настоящее время выполняется формирование текста при экспорте в форматы PDF или XPS.
doc.Save(ArtifactsDir + "Document.OpenType.pdf");
```

### Смотрите также

* interface [ITextShaperFactory](../../../aspose.words.shaping/itextshaperfactory/)
* class [LayoutOptions](../)
* пространство имен [Aspose.Words.Layout](../../../aspose.words.layout/)
* сборка [Aspose.Words](../../../)
