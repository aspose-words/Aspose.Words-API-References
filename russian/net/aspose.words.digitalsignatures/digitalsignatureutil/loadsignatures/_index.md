---
title: DigitalSignatureUtil.LoadSignatures
second_title: Справочник по API Aspose.Words для .NET
description: DigitalSignatureUtil метод. Загружает цифровые подписи из документа.
type: docs
weight: 10
url: /ru/net/aspose.words.digitalsignatures/digitalsignatureutil/loadsignatures/
---
## LoadSignatures(string) {#loadsignatures_1}

Загружает цифровые подписи из документа.

```csharp
public static DigitalSignatureCollection LoadSignatures(string fileName)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| fileName | String | Путь к документу. |

### Возвращаемое значение

Сбор цифровых подписей. Возвращает пустую коллекцию, если файл не подписан.

### Примеры

Показывает, как загружать подписи из документа с цифровой подписью.

```csharp
// Существует два способа загрузки коллекции цифровых подписей подписанного документа с использованием класса DigitalSignatureUtil.
// 1 - Загрузить из документа из локальной файловой системы имя файла:
DigitalSignatureCollection digitalSignatures = 
    DigitalSignatureUtil.LoadSignatures(MyDir + "Digitally signed.docx");

// Если эта коллекция не пуста, то мы можем проверить, что документ имеет цифровую подпись.
Assert.AreEqual(1, digitalSignatures.Count);

// 2 - Загрузить из документа из FileStream:
using (Stream stream = new FileStream(MyDir + "Digitally signed.docx", FileMode.Open))
{
    digitalSignatures = DigitalSignatureUtil.LoadSignatures(stream);
    Assert.AreEqual(1, digitalSignatures.Count);
}
```

Показывает, как удалить цифровые подписи из документа с цифровой подписью.

```csharp
// Существует два способа использования класса DigitalSignatureUtil для удаления цифровых подписей
// из подписанного документа, сохранив его неподписанную копию где-нибудь еще в локальной файловой системе.
// 1 - Определить расположение как подписанного документа, так и неподписанной копии по строкам имени файла:
DigitalSignatureUtil.RemoveAllSignatures(MyDir + "Digitally signed.docx",
    ArtifactsDir + "DigitalSignatureUtil.LoadAndRemove.FromString.docx");

// 2 - Определить расположение как подписанного документа, так и неподписанной копии по файловым потокам:
using (Stream streamIn = new FileStream(MyDir + "Digitally signed.docx", FileMode.Open))
{
    using (Stream streamOut = new FileStream(ArtifactsDir + "DigitalSignatureUtil.LoadAndRemove.FromStream.docx", FileMode.Create))
    {
        DigitalSignatureUtil.RemoveAllSignatures(streamIn, streamOut);
    }
}

// Убедитесь, что оба наших выходных документа не имеют цифровых подписей.
Assert.That(DigitalSignatureUtil.LoadSignatures(ArtifactsDir + "DigitalSignatureUtil.LoadAndRemove.FromString.docx"), Is.Empty);
Assert.That(DigitalSignatureUtil.LoadSignatures(ArtifactsDir + "DigitalSignatureUtil.LoadAndRemove.FromStream.docx"), Is.Empty);
```

### Смотрите также

* class [DigitalSignatureCollection](../../digitalsignaturecollection/)
* class [DigitalSignatureUtil](../)
* пространство имен [Aspose.Words.DigitalSignatures](../../digitalsignatureutil/)
* сборка [Aspose.Words](../../../)

---

## LoadSignatures(Stream) {#loadsignatures}

Загружает цифровые подписи из документа с использованием потока.

```csharp
public static DigitalSignatureCollection LoadSignatures(Stream stream)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| stream | Stream | Поток с документом. |

### Возвращаемое значение

Сбор цифровых подписей. Возвращает пустую коллекцию, если файл не подписан.

### Примеры

Показывает, как загружать подписи из документа с цифровой подписью.

```csharp
// Существует два способа загрузки коллекции цифровых подписей подписанного документа с использованием класса DigitalSignatureUtil.
// 1 - Загрузить из документа из локальной файловой системы имя файла:
DigitalSignatureCollection digitalSignatures = 
    DigitalSignatureUtil.LoadSignatures(MyDir + "Digitally signed.docx");

// Если эта коллекция не пуста, то мы можем проверить, что документ имеет цифровую подпись.
Assert.AreEqual(1, digitalSignatures.Count);

// 2 - Загрузить из документа из FileStream:
using (Stream stream = new FileStream(MyDir + "Digitally signed.docx", FileMode.Open))
{
    digitalSignatures = DigitalSignatureUtil.LoadSignatures(stream);
    Assert.AreEqual(1, digitalSignatures.Count);
}
```

### Смотрите также

* class [DigitalSignatureCollection](../../digitalsignaturecollection/)
* class [DigitalSignatureUtil](../)
* пространство имен [Aspose.Words.DigitalSignatures](../../digitalsignatureutil/)
* сборка [Aspose.Words](../../../)


