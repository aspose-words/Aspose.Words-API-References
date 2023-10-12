---
title: Class DigitalSignatureUtil
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.DigitalSignatures.DigitalSignatureUtil сорт. Предоставляет методы для подписания документа.
type: docs
weight: 410
url: /ru/net/aspose.words.digitalsignatures/digitalsignatureutil/
---
## DigitalSignatureUtil class

Предоставляет методы для подписания документа.

Чтобы узнать больше, посетите[Работа с цифровыми подписями](https://docs.aspose.com/words/net/working-with-digital-signatures/) статья документации.

```csharp
public static class DigitalSignatureUtil
```

## Методы

| Имя | Описание |
| --- | --- |
| static [LoadSignatures](../../aspose.words.digitalsignatures/digitalsignatureutil/loadsignatures/#loadsignatures)(Stream) | Загружает цифровые подписи из документа с помощью потока. |
| static [LoadSignatures](../../aspose.words.digitalsignatures/digitalsignatureutil/loadsignatures/#loadsignatures_1)(string) | Загружает цифровые подписи из документа. |
| static [RemoveAllSignatures](../../aspose.words.digitalsignatures/digitalsignatureutil/removeallsignatures/#removeallsignatures)(Stream, Stream) | Удаляет все цифровые подписи из документа в исходном потоке и записывает неподписанный документ в целевой поток. |
| static [RemoveAllSignatures](../../aspose.words.digitalsignatures/digitalsignatureutil/removeallsignatures/#removeallsignatures_1)(string, string) | Удаляет все цифровые подписи из исходного файла и записывает неподписанный файл в файл назначения. |
| static [Sign](../../aspose.words.digitalsignatures/digitalsignatureutil/sign/#sign)(Stream, Stream, CertificateHolder) | Подписывает исходный документ, используя заданные[`CertificateHolder`](../certificateholder/)с цифровой подписью и записывает подписанный документ в поток назначения. |
| static [Sign](../../aspose.words.digitalsignatures/digitalsignatureutil/sign/#sign_2)(string, string, CertificateHolder) | Подписывает исходный документ, используя заданные[`CertificateHolder`](../certificateholder/) с цифровой подписью и записывает подписанный документ в файл назначения. |
| static [Sign](../../aspose.words.digitalsignatures/digitalsignatureutil/sign/#sign_1)(Stream, Stream, CertificateHolder, SignOptions) | Подписывает исходный документ, используя заданные[`CertificateHolder`](../certificateholder/) и[`SignOptions`](../signoptions/) с цифровой подписью и записывает подписанный документ в поток назначения. |
| static [Sign](../../aspose.words.digitalsignatures/digitalsignatureutil/sign/#sign_3)(string, string, CertificateHolder, SignOptions) | Подписывает исходный документ, используя заданные[`CertificateHolder`](../certificateholder/) и[`SignOptions`](../signoptions/) с цифровой подписью и записывает подписанный документ в файл назначения. |

### Примечания

Поскольку цифровая подпись работает с содержимым файла, а не с объектной моделью документа, эти методы вынесены в отдельный класс.

Поддерживаемые форматы:Doc иDocx.

### Примеры

Показывает, как загрузить подписи из документа с цифровой подписью.

```csharp
// Существует два способа загрузки коллекции цифровых подписей подписанного документа с помощью класса DigitalSignatureUtil.
// 1 - Загрузка из документа из локальной файловой системы с именем файла:
DigitalSignatureCollection digitalSignatures = 
    DigitalSignatureUtil.LoadSignatures(MyDir + "Digitally signed.docx");

// Если эта коллекция непуста, мы можем проверить, что документ имеет цифровую подпись.
Assert.AreEqual(1, digitalSignatures.Count);

// 2 - Загрузка документа из FileStream:
using (Stream stream = new FileStream(MyDir + "Digitally signed.docx", FileMode.Open))
{
    digitalSignatures = DigitalSignatureUtil.LoadSignatures(stream);
    Assert.AreEqual(1, digitalSignatures.Count);
}
```

Показывает, как удалить цифровые подписи из документа с цифровой подписью.

```csharp
// Существует два способа использования класса DigitalSignatureUtil для удаления цифровых подписей.
// из подписанного документа, сохранив его неподписанную копию где-нибудь в другом месте локальной файловой системы.
// 1 - Определить местоположение как подписанного документа, так и неподписанной копии по строкам имен файлов:
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

// Убедитесь, что оба наших выходных документа не имеют цифровых подписей.
Assert.That(DigitalSignatureUtil.LoadSignatures(ArtifactsDir + "DigitalSignatureUtil.LoadAndRemove.FromString.docx"), Is.Empty);
Assert.That(DigitalSignatureUtil.LoadSignatures(ArtifactsDir + "DigitalSignatureUtil.LoadAndRemove.FromStream.docx"), Is.Empty);
```

### Смотрите также

* пространство имен [Aspose.Words.DigitalSignatures](../../aspose.words.digitalsignatures/)
* сборка [Aspose.Words](../../)


