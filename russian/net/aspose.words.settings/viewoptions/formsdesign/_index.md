---
title: ViewOptions.FormsDesign
linktitle: FormsDesign
articleTitle: FormsDesign
second_title: Aspose.Words для .NET
description: Узнайте, как ViewOptions FormsDesign улучшает работу с документами, переключая режим разработки форм для удобного редактирования и настройки.
type: docs
weight: 30
url: /ru/net/aspose.words.settings/viewoptions/formsdesign/
---
## ViewOptions.FormsDesign property

Указывает, находится ли документ в режиме разработки форм.

```csharp
public bool FormsDesign { get; set; }
```

## Примечания

В настоящее время работает только для документов в формате WordML.

## Примеры

Показывает, как включить/отключить режим разработки форм.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Установите свойство "FormsDesign" в значение "false", чтобы режим разработки форм оставался отключенным.
// Установите свойство «FormsDesign» в значение «true», чтобы включить режим разработки форм.
doc.ViewOptions.FormsDesign = useFormsDesign;

doc.Save(ArtifactsDir + "ViewOptions.FormsDesign.xml");

Assert.AreEqual(useFormsDesign,
    File.ReadAllText(ArtifactsDir + "ViewOptions.FormsDesign.xml").Contains("<w:formsDesign />"));
```

### Смотрите также

* class [ViewOptions](../)
* пространство имен [Aspose.Words.Settings](../../../aspose.words.settings/)
* сборка [Aspose.Words](../../../)
