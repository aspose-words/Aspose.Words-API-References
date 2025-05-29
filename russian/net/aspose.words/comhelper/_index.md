---
title: ComHelper Class
linktitle: ComHelper
articleTitle: ComHelper
second_title: Aspose.Words для .NET
description: Разблокируйте бесшовную интеграцию документов с Aspose.Words.ComHelper. Легко загружайте и управляйте документами для клиентов COM с помощью мощных функций.
type: docs
weight: 410
url: /ru/net/aspose.words/comhelper/
---
## ComHelper class

Предоставляет методы для клиентов COM для загрузки документа в Aspose.Words.

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
| [Open](../../aspose.words/comhelper/open/#open)(*Stream*) | Позволяет загружать COM-приложение[`Document`](../document/) из потока. |
| [Open](../../aspose.words/comhelper/open/#open_1)(*string*) | Позволяет приложению COM загружать[`Document`](../document/) из файла . |
| [OpenIStream](../../aspose.words/comhelper/openistream/)(*IStream*) | Позволяет приложению COM загружать[`Document`](../document/) из объекта IStream. |

## Примечания

Используйте`ComHelper` класс для загрузки документа из файла или потока в [`Document`](../document/) объект в COM-приложении.

The[`Document`](../document/) класс предоставляет конструктор по умолчанию для создания нового документа , а также предоставляет перегруженные конструкторы для загрузки документа из файла или потока. Если вы используете Aspose.Words из приложения .NET, вы можете использовать все[`Document`](../document/) конструкторы напрямую, но если вы используете Aspose.Words из приложения COM, только по умолчанию[`Document`](../document/) Конструктор доступен.

## Примеры

```csharp
[VBScript]

Dim helper
Set helper = CreateObject("Aspose.Words.ComHelper")

Dim doc
Set doc = helper.Open(fileName)
```

Показывает, как открывать документы с помощью класса ComHelper.

```csharp
// Класс ComHelper позволяет нам загружать документы из клиентов COM.
ComHelper comHelper = new ComHelper();

// 1 - Использование имени файла локальной системы:
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
