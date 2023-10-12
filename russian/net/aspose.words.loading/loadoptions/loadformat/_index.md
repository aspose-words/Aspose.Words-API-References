---
title: LoadOptions.LoadFormat
second_title: Справочник по API Aspose.Words для .NET
description: LoadOptions свойство. Указывает формат загружаемого документа. По умолчаниюAuto .
type: docs
weight: 90
url: /ru/net/aspose.words.loading/loadoptions/loadformat/
---
## LoadOptions.LoadFormat property

Указывает формат загружаемого документа. По умолчанию:Auto .

```csharp
public LoadFormat LoadFormat { get; set; }
```

### Примечания

Рекомендуется указатьAuto значение и позвольте Aspose.Words автоматически определить формат файла. Если вы знаете формат документа, который собираетесь загрузить, вы можете явно указать format , и это немного сократит время загрузки из-за накладных расходов, связанных с автоматическим определением формата. Если вы укажете явный формат загрузки, и он превратится Если это не так, будет активировано автоматическое обнаружение и будет предпринята вторая попытка загрузки файла.

### Примеры

Показывает, как указать базовый URI при открытии HTML-документа.

```csharp
// Предположим, мы хотим загрузить документ .html, содержащий изображение, связанное относительным URI.
// пока изображение находится в другом месте. В этом случае нам нужно будет преобразовать относительный URI в абсолютный.
 // Мы можем предоставить базовый URI, используя объект HtmlLoadOptions.
HtmlLoadOptions loadOptions = new HtmlLoadOptions(LoadFormat.Html, "", ImageDir);

Assert.AreEqual(LoadFormat.Html, loadOptions.LoadFormat);

Document doc = new Document(MyDir + "Missing image.html", loadOptions);

// Хотя изображение во входном .html было повреждено, наш собственный базовый URI помог нам восстановить ссылку.
Shape imageShape = (Shape)doc.GetChildNodes(NodeType.Shape, true)[0];
Assert.True(imageShape.IsImage);

// Этот выходной документ отобразит отсутствующее изображение.
doc.Save(ArtifactsDir + "HtmlLoadOptions.BaseUri.docx");
```

### Смотрите также

* enum [LoadFormat](../../../aspose.words/loadformat/)
* class [LoadOptions](../)
* пространство имен [Aspose.Words.Loading](../../loadoptions/)
* сборка [Aspose.Words](../../../)


