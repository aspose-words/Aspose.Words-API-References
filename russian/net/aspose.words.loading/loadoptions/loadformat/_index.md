---
title: LoadOptions.LoadFormat
linktitle: LoadFormat
articleTitle: LoadFormat
second_title: Aspose.Words для .NET
description: Откройте для себя свойство LoadOptions LoadFormat, чтобы легко указать форматы документов. Оптимизируйте загрузку с помощью настройки Auto по умолчанию для бесперебойной работы.
type: docs
weight: 90
url: /ru/net/aspose.words.loading/loadoptions/loadformat/
---
## LoadOptions.LoadFormat property

Указывает формат документа для загрузки. Значение по умолчанию:Auto .

```csharp
public LoadFormat LoadFormat { get; set; }
```

## Примечания

Рекомендуется указатьAuto значение и позвольте Aspose.Words определить формат файла автоматически. Если вы знаете формат документа, который собираетесь загрузить, вы можете указать format явно, и это немного сократит время загрузки за счет накладных расходов, связанных с автоматическим определением формата. Если вы укажете явный формат загрузки и он окажется неверным, будет вызвано автоматическое определение и будет сделана вторая попытка загрузить файл.

## Примеры

Показывает, как указать базовый URI при открытии HTML-документа.

```csharp
// Предположим, мы хотим загрузить документ .html, содержащий изображение, связанное с помощью относительного URI
// пока изображение находится в другом месте. В этом случае нам нужно будет преобразовать относительный URI в абсолютный.
 // Мы можем предоставить базовый URI с помощью объекта HtmlLoadOptions.
HtmlLoadOptions loadOptions = new HtmlLoadOptions(LoadFormat.Html, "", ImageDir);

Assert.AreEqual(LoadFormat.Html, loadOptions.LoadFormat);

Document doc = new Document(MyDir + "Missing image.html", loadOptions);

// Хотя изображение во входном .html-файле было повреждено, наш базовый URI помог нам восстановить ссылку.
Shape imageShape = (Shape)doc.GetChildNodes(NodeType.Shape, true)[0];
Assert.True(imageShape.IsImage);

// Этот выходной документ будет отображать отсутствующее изображение.
doc.Save(ArtifactsDir + "HtmlLoadOptions.BaseUri.docx");
```

### Смотрите также

* enum [LoadFormat](../../../aspose.words/loadformat/)
* class [LoadOptions](../)
* пространство имен [Aspose.Words.Loading](../../../aspose.words.loading/)
* сборка [Aspose.Words](../../../)
