---
title: LoadOptions
linktitle: LoadOptions
articleTitle: LoadOptions
second_title: Aspose.Words для .NET
description: Откройте для себя конструктор LoadOptions, предназначенный для простой инициализации нового экземпляра со значениями по умолчанию для оптимальной производительности и эффективности.
type: docs
weight: 10
url: /ru/net/aspose.words.loading/loadoptions/loadoptions/
---
## LoadOptions() {#constructor}

Инициализирует новый экземпляр этого класса со значениями по умолчанию.

```csharp
public LoadOptions()
```

## Примеры

Показывает, как открыть HTML-документ с изображениями из потока, используя базовый URI.

```csharp
using (Stream stream = File.OpenRead(MyDir + "Document.html"))
{
    // Передать URI базовой папки при ее загрузке
    // чтобы можно было найти любые изображения с относительными URI в HTML-документе.
    LoadOptions loadOptions = new LoadOptions();
    loadOptions.BaseUri = ImageDir;

    Document doc = new Document(stream, loadOptions);

    // Убедитесь, что первая фигура документа содержит допустимое изображение.
    Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

    Assert.IsTrue(shape.IsImage);
    Assert.IsNotNull(shape.ImageData.ImageBytes);
    Assert.AreEqual(32.0, ConvertUtil.PointToPixel(shape.Width), 0.01);
    Assert.AreEqual(32.0, ConvertUtil.PointToPixel(shape.Height), 0.01);
}
```

### Смотрите также

* class [LoadOptions](../)
* пространство имен [Aspose.Words.Loading](../../../aspose.words.loading/)
* сборка [Aspose.Words](../../../)

---

## LoadOptions(*string*) {#constructor_2}

Ярлык для инициализации нового экземпляра этого класса с указанным паролем для загрузки зашифрованного документа.

```csharp
public LoadOptions(string password)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| password | String | Пароль для открытия зашифрованного документа. Может быть`нулевой` или пустая строка. |

## Примеры

Показывает, как загрузить зашифрованный документ Microsoft Word.

```csharp
Document doc;

// Aspose.Words выдает исключение, если мы пытаемся открыть зашифрованный документ без его пароля.
Assert.Throws<IncorrectPasswordException>(() => doc = new Document(MyDir + "Encrypted.docx"));

// При загрузке такого документа пароль передается конструктору документа с помощью объекта LoadOptions.
LoadOptions options = new LoadOptions("docPassword");

// Существует два способа загрузки зашифрованного документа с помощью объекта LoadOptions.
// 1 - Загрузить документ из локальной файловой системы по имени файла:
doc = new Document(MyDir + "Encrypted.docx", options);
// 2 - Загрузить документ из потока:
using (Stream stream = File.OpenRead(MyDir + "Encrypted.docx"))
{
    doc = new Document(stream, options);
}
```

### Смотрите также

* class [LoadOptions](../)
* пространство имен [Aspose.Words.Loading](../../../aspose.words.loading/)
* сборка [Aspose.Words](../../../)

---

## LoadOptions(*[LoadFormat](../../../aspose.words/loadformat/), string, string*) {#constructor_1}

Ярлык для инициализации нового экземпляра этого класса со свойствами, установленными на указанные значения.

```csharp
public LoadOptions(LoadFormat loadFormat, string password, string baseUri)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| loadFormat | LoadFormat | Формат загружаемого документа. |
| password | String | Пароль для открытия зашифрованного документа. Может быть`нулевой` или пустая строка. |
| baseUri | String | Строка, которая будет использоваться для преобразования относительных URI в абсолютные. Может быть`нулевой` или пустая строка. |

## Примеры

Показывает, как сохранить веб-страницу в виде файла .docx.

```csharp
const string url = "https://products.aspose.com/words/";

using (WebClient client = new WebClient())
{
    var bytes = client.DownloadData(url);
    using (MemoryStream stream = new MemoryStream(bytes))
    {
        // URL-адрес снова используется как baseUri, чтобы гарантировать правильность извлечения любых относительных путей к изображениям.
        LoadOptions options = new LoadOptions(LoadFormat.Html, "", url);

        // Загружаем HTML-документ из потока и передаем объект LoadOptions.
        Document doc = new Document(stream, options);

        // На этом этапе мы можем прочитать и отредактировать содержимое документа, а затем сохранить его в локальной файловой системе.
        doc.Save(ArtifactsDir + "Document.InsertHtmlFromWebPage.docx");
    }
}
```

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
