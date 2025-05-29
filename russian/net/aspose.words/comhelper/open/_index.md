---
title: ComHelper.Open
linktitle: Open
articleTitle: Open
second_title: Aspose.Words для .NET
description: Откройте для себя бесшовную интеграцию с помощью метода Open ComHelper, обеспечивающего легкую загрузку документов из файлов для ваших COM-приложений.
type: docs
weight: 20
url: /ru/net/aspose.words/comhelper/open/
---
## Open(*string*) {#open_1}

Позволяет приложению COM загружать[`Document`](../../document/) из файла .

```csharp
public Document Open(string fileName)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| fileName | String | Имя файла документа для загрузки. |

### Возвращаемое значение

А[`Document`](../../document/) объект, представляющий документ Word.

## Примечания

Этот метод аналогичен вызову[`Document`](../../document/) конструктор с параметром имени файла.

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

* class [Document](../../document/)
* class [ComHelper](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)

---

## Open(*Stream*) {#open}

Позволяет загружать COM-приложение[`Document`](../../document/) из потока.

```csharp
public Document Open(Stream stream)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| stream | Stream | Объект потока .NET, содержащий документ для загрузки. |

### Возвращаемое значение

А[`Document`](../../document/) объект, представляющий документ Word.

## Примечания

Этот метод аналогичен вызову[`Document`](../../document/) конструктор с параметром потока.

## Примеры

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

* class [Document](../../document/)
* class [ComHelper](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
