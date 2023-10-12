---
title: Class ComHelper
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.ComHelper сорт. Предоставляет методы COMклиентам для загрузки документа в Aspose.Words.
type: docs
weight: 220
url: /ru/net/aspose.words/comhelper/
---
## ComHelper class

Предоставляет методы COM-клиентам для загрузки документа в Aspose.Words.

```csharp
public class ComHelper
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [ComHelper](comhelper/)() | Инициализирует новый экземпляр этого класса. |

## Методы

| Имя | Описание |
| --- | --- |
| [Open](../../aspose.words/comhelper/open/#open)(Stream) | Разрешает загрузку COM-приложения.[`Document`](../document/) из потока. |
| [Open](../../aspose.words/comhelper/open/#open_1)(string) | Позволяет COM-приложению загружать[`Document`](../document/) из файла. |
| [OpenIStream](../../aspose.words/comhelper/openistream/)(IStream) | Позволяет COM-приложению загружать[`Document`](../document/) из объекта IStream. |

### Примечания

Использовать`ComHelper` класс для загрузки документа из файла или потока в [`Document`](../document/) объект в COM-приложении.

[`Document`](../document/) Класс предоставляет конструктор по умолчанию для создания нового документа document , а также предоставляет перегруженные конструкторы для загрузки документа из файла или потока. Если вы используете Aspose.Words из приложения .NET, вы можете использовать все[`Document`](../document/) напрямую, но если вы используете Aspose.Words из COM-приложения, только по умолчанию.[`Document`](../document/) конструктор имеется.

### Примеры

```csharp
[VBScript]

Dim helper
Set helper = CreateObject("Aspose.Words.ComHelper")

Dim doc
Set doc = helper.Open(fileName)
```

Показывает, как открывать документы с помощью класса ComHelper.

```csharp
// Класс ComHelper позволяет нам загружать документы из COM-клиентов.
ComHelper comHelper = new ComHelper();

// 1 - Использование локального системного имени файла:
Document doc = comHelper.Open(MyDir + "Document.docx");

Assert.AreEqual("Hello World!\r\rHello Word!\r\r\rHello World!", doc.GetText().Trim());

// 2 - Из потока:
using (FileStream stream = new FileStream(MyDir + "Document.docx", FileMode.Open))
{
    doc = comHelper.Open(stream);

    Assert.AreEqual("Hello World!\r\rHello Word!\r\r\rHello World!", doc.GetText().Trim());
}
```

### Смотрите также

* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)


