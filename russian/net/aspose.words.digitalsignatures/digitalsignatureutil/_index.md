---
title: DigitalSignatureUtil Class
linktitle: DigitalSignatureUtil
articleTitle: DigitalSignatureUtil
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.DigitalSignatures.DigitalSignatureUtil для легкой подписи документов с помощью безопасных цифровых подписей. Улучшите целостность документов сегодня!
type: docs
weight: 610
url: /ru/net/aspose.words.digitalsignatures/digitalsignatureutil/
---
## DigitalSignatureUtil class

Предоставляет методы для подписания документа.

Чтобы узнать больше, посетите[Работа с цифровыми подписями](https://docs.aspose.com/words/net/working-with-digital-signatures/) документальная статья.

```csharp
public static class DigitalSignatureUtil
```

## Методы

| Имя | Описание |
| --- | --- |
| static [LoadSignatures](../../aspose.words.digitalsignatures/digitalsignatureutil/loadsignatures/#loadsignatures)(*Stream*) | Загружает цифровые подписи из документа с помощью stream. |
| static [LoadSignatures](../../aspose.words.digitalsignatures/digitalsignatureutil/loadsignatures/#loadsignatures_1)(*string*) | Загружает цифровые подписи из документа. |
| static [RemoveAllSignatures](../../aspose.words.digitalsignatures/digitalsignatureutil/removeallsignatures/#removeallsignatures)(*Stream, Stream*) | Удаляет все цифровые подписи из документа в исходном потоке и записывает неподписанный документ в целевой поток. |
| static [RemoveAllSignatures](../../aspose.words.digitalsignatures/digitalsignatureutil/removeallsignatures/#removeallsignatures_1)(*string, string*) | Удаляет все цифровые подписи из исходного файла и записывает неподписанный файл в целевой файл. |
| static [Sign](../../aspose.words.digitalsignatures/digitalsignatureutil/sign/#sign)(*Stream, Stream, [CertificateHolder](../certificateholder/)*) | Подписывает исходный документ, используя заданный[`CertificateHolder`](../certificateholder/) с цифровой подписью и записывает подписанный документ в целевой поток. |
| static [Sign](../../aspose.words.digitalsignatures/digitalsignatureutil/sign/#sign_2)(*string, string, [CertificateHolder](../certificateholder/)*) | Подписывает исходный документ, используя заданный[`CertificateHolder`](../certificateholder/) с цифровой подписью и записывает подписанный документ в целевой файл. |
| static [Sign](../../aspose.words.digitalsignatures/digitalsignatureutil/sign/#sign_1)(*Stream, Stream, [CertificateHolder](../certificateholder/), [SignOptions](../signoptions/)*) | Подписывает исходный документ, используя заданный[`CertificateHolder`](../certificateholder/) и[`SignOptions`](../signoptions/) с цифровой подписью и записывает подписанный документ в целевой поток. |
| static [Sign](../../aspose.words.digitalsignatures/digitalsignatureutil/sign/#sign_3)(*string, string, [CertificateHolder](../certificateholder/), [SignOptions](../signoptions/)*) | Подписывает исходный документ, используя заданный[`CertificateHolder`](../certificateholder/) и[`SignOptions`](../signoptions/) с цифровой подписью и записывает подписанный документ в целевой файл. |

## Примечания

Поскольку цифровая подпись работает с содержимым файла, а не с объектной моделью документа, эти методы выделены в отдельный класс.

Поддерживаемые форматы: Doc , Dot , Docx , Dotx , Docm , Dotm , Odt , Ott.

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

* пространство имен [Aspose.Words.DigitalSignatures](../../aspose.words.digitalsignatures/)
* сборка [Aspose.Words](../../)
