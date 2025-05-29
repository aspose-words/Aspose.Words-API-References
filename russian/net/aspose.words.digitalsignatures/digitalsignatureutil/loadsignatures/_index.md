---
title: DigitalSignatureUtil.LoadSignatures
linktitle: LoadSignatures
articleTitle: LoadSignatures
second_title: Aspose.Words для .NET
description: Легко загружайте цифровые подписи из ваших документов с помощью метода DigitalSignatureUtil LoadSignatures. Улучшите свой рабочий процесс сегодня!
type: docs
weight: 10
url: /ru/net/aspose.words.digitalsignatures/digitalsignatureutil/loadsignatures/
---
## LoadSignatures(*string*) {#loadsignatures_1}

Загружает цифровые подписи из документа.

```csharp
public static DigitalSignatureCollection LoadSignatures(string fileName)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| fileName | String | Путь к документу. |

### Возвращаемое значение

Коллекция цифровых подписей. Возвращает пустую коллекцию, если файл не подписан.

## Примеры

Показывает, как загрузить подписи из документа с цифровой подписью.

```csharp
// Существует два способа загрузки коллекции цифровых подписей подписанного документа с использованием класса DigitalSignatureUtil.
// 1 - Загрузка из документа из локальной файловой системы имя файла:
DigitalSignatureCollection digitalSignatures = 
    DigitalSignatureUtil.LoadSignatures(MyDir + "Digitally signed.docx");

// Если эта коллекция непустая, то мы можем проверить, имеет ли документ цифровую подпись.
Assert.AreEqual(1, digitalSignatures.Count);

// 2 - Загрузка из документа из FileStream:
using (Stream stream = new FileStream(MyDir + "Digitally signed.docx", FileMode.Open))
{
    digitalSignatures = DigitalSignatureUtil.LoadSignatures(stream);
    Assert.AreEqual(1, digitalSignatures.Count);
}
```

Показывает, как удалить цифровые подписи из документа с цифровой подписью.

```csharp
// Существует два способа использования класса DigitalSignatureUtil для удаления цифровых подписей
// из подписанного документа, сохранив его неподписанную копию где-нибудь в другом месте локальной файловой системы.
// 1 - Определить местоположение как подписанного документа, так и неподписанной копии по строкам имени файла:
DigitalSignatureUtil.RemoveAllSignatures(MyDir + "Digitally signed.docx",
    ArtifactsDir + "DigitalSignatureUtil.LoadAndRemove.FromString.docx");

// 2 - Определить местоположение как подписанного документа, так и неподписанной копии по файловым потокам:
using (Stream streamIn = new FileStream(MyDir + "Digitally signed.docx", FileMode.Open))
{
    using (Stream streamOut = new FileStream(ArtifactsDir + "DigitalSignatureUtil.LoadAndRemove.FromStream.docx", FileMode.Create))
    {
        DigitalSignatureUtil.RemoveAllSignatures(streamIn, streamOut);
    }
}

// Проверяем, что оба наших выходных документа не имеют цифровых подписей.
Assert.AreEqual(0, DigitalSignatureUtil.LoadSignatures(ArtifactsDir + "DigitalSignatureUtil.LoadAndRemove.FromString.docx").Count);
Assert.AreEqual(0, DigitalSignatureUtil.LoadSignatures(ArtifactsDir + "DigitalSignatureUtil.LoadAndRemove.FromStream.docx").Count);
```

### Смотрите также

* class [DigitalSignatureCollection](../../digitalsignaturecollection/)
* class [DigitalSignatureUtil](../)
* пространство имен [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* сборка [Aspose.Words](../../../)

---

## LoadSignatures(*Stream*) {#loadsignatures}

Загружает цифровые подписи из документа с помощью stream.

```csharp
public static DigitalSignatureCollection LoadSignatures(Stream stream)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| stream | Stream | Трансляция документа. |

### Возвращаемое значение

Коллекция цифровых подписей. Возвращает пустую коллекцию, если файл не подписан.

## Примеры

Показывает, как загрузить подписи из документа с цифровой подписью.

```csharp
// Существует два способа загрузки коллекции цифровых подписей подписанного документа с использованием класса DigitalSignatureUtil.
// 1 - Загрузка из документа из локальной файловой системы имя файла:
DigitalSignatureCollection digitalSignatures = 
    DigitalSignatureUtil.LoadSignatures(MyDir + "Digitally signed.docx");

// Если эта коллекция непустая, то мы можем проверить, имеет ли документ цифровую подпись.
Assert.AreEqual(1, digitalSignatures.Count);

// 2 - Загрузка из документа из FileStream:
using (Stream stream = new FileStream(MyDir + "Digitally signed.docx", FileMode.Open))
{
    digitalSignatures = DigitalSignatureUtil.LoadSignatures(stream);
    Assert.AreEqual(1, digitalSignatures.Count);
}
```

### Смотрите также

* class [DigitalSignatureCollection](../../digitalsignaturecollection/)
* class [DigitalSignatureUtil](../)
* пространство имен [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* сборка [Aspose.Words](../../../)
