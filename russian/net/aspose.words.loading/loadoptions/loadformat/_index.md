---
title: LoadOptions.LoadFormat
second_title: Справочник по API Aspose.Words для .NET
description: LoadOptions свойство. Указывает формат загружаемого документа. Значение по умолчаниюAuto .
type: docs
weight: 90
url: /ru/net/aspose.words.loading/loadoptions/loadformat/
---
## LoadOptions.LoadFormat property

Указывает формат загружаемого документа. Значение по умолчанию:Auto .

```csharp
public LoadFormat LoadFormat { get; set; }
```

### Примечания

Рекомендуется указатьAutoзначение и позволить Aspose.Words определить формат файла автоматически. Если вы знаете формат документа, который собираетесь загрузить, вы можете явно указать формат , и это немного сократит время загрузки за счет накладных расходов, связанных с автоматическим определением формата. Если вы укажете явный формат загрузки, ошибочно, будет запущено автоматическое определение и будет предпринята попытка second загрузить файл.

### Примеры

Показывает, как указать базовый URI при открытии html-документа.

```csharp
// Предположим, мы хотим загрузить документ .html, содержащий изображение, связанное относительным URI
// пока изображение находится в другом месте. В этом случае нам нужно будет преобразовать относительный URI в абсолютный.
 // Мы можем предоставить базовый URI, используя объект HtmlLoadOptions.
HtmlLoadOptions loadOptions = new HtmlLoadOptions(LoadFormat.Html, "", ImageDir);

Assert.AreEqual(LoadFormat.Html, loadOptions.LoadFormat);

Document doc = new Document(MyDir + "Missing image.html", loadOptions);

// Хотя изображение во входном .html было повреждено, наш собственный базовый URI помог нам восстановить ссылку.
Shape imageShape = (Shape)doc.GetChildNodes(NodeType.Shape, true)[0];
Assert.True(imageShape.IsImage);

// Этот выходной документ будет отображать отсутствующее изображение.
doc.Save(ArtifactsDir + "HtmlLoadOptions.BaseUri.docx");
```

### Смотрите также

* enum [LoadFormat](../../../aspose.words/loadformat/)
* class [LoadOptions](../)
* пространство имен [Aspose.Words.Loading](../../loadoptions/)
* сборка [Aspose.Words](../../../)


