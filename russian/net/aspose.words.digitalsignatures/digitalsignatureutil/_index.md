---
title: DigitalSignatureUtil
second_title: Справочник по API Aspose.Words для .NET
description: Предоставляет методы для подписания документа.
type: docs
weight: 400
url: /ru/net/aspose.words.digitalsignatures/digitalsignatureutil/
---
## DigitalSignatureUtil class

Предоставляет методы для подписания документа.

```csharp
public static class DigitalSignatureUtil
```

## Методы

| Имя | Описание |
| --- | --- |
| static [LoadSignatures](../../aspose.words.digitalsignatures/digitalsignatureutil/loadsignatures#loadsignatures)(Stream) | Загружает цифровые подписи из документа, используя поток. |
| static [LoadSignatures](../../aspose.words.digitalsignatures/digitalsignatureutil/loadsignatures#loadsignatures_1)(string) | Загружает цифровые подписи из документа. |
| static [RemoveAllSignatures](../../aspose.words.digitalsignatures/digitalsignatureutil/removeallsignatures#removeallsignatures)(Stream, Stream) | Удаляет все цифровые подписи из документа в исходном потоке и записывает неподписанный документ в целевой поток. |
| static [RemoveAllSignatures](../../aspose.words.digitalsignatures/digitalsignatureutil/removeallsignatures#removeallsignatures_1)(string, string) | Удаляет все цифровые подписи из исходного файла и записывает неподписанный файл в целевой файл. |
| static [Sign](../../aspose.words.digitalsignatures/digitalsignatureutil/sign#sign)(Stream, Stream, CertificateHolder) | Подписывает исходный документ с использованием данного[`CertificateHolder`](../certificateholder)цифровой подписью и записывает подписанный документ в поток назначения. |
| static [Sign](../../aspose.words.digitalsignatures/digitalsignatureutil/sign#sign_2)(string, string, CertificateHolder) | Подписывает исходный документ с использованием данного[`CertificateHolder`](../certificateholder)цифровой подписью и записывает подписанный документ в файл назначения. |
| static [Sign](../../aspose.words.digitalsignatures/digitalsignatureutil/sign#sign_1)(Stream, Stream, CertificateHolder, SignOptions) | Подписывает исходный документ, используя данные[`CertificateHolder`](../certificateholder)и[`SignOptions`](../signoptions) с цифровой подписью и записывает подписанный документ в поток назначения. |
| static [Sign](../../aspose.words.digitalsignatures/digitalsignatureutil/sign#sign_3)(string, string, CertificateHolder, SignOptions) | Подписывает исходный документ, используя данные[`CertificateHolder`](../certificateholder)и[`SignOptions`](../signoptions) с цифровой подписью и записывает подписанный документ в файл назначения. |

### Примечания

Поскольку цифровая подпись работает с содержимым файла, а не с объектной моделью документа, эти методы вынесены в отдельный учебный класс.

Поддерживаемые форматы:DocиДок.

### Примеры

Показывает, как загружать подписи из документа с цифровой подписью.

```csharp
 // Существует два способа использования класса DigitalSignatureUtil для удаления цифровых подписей
 // из подписанного документа, сохранив его неподписанную копию где-то еще в локальной файловой системе.
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

 // Проверяем, что оба наших выходных документа не имеют цифровых подписей.
Assert.That(DigitalSignatureUtil.LoadSignatures(ArtifactsDir + "DigitalSignatureUtil.LoadAndRemove.FromString.docx"), Is.Empty);
Assert.That(DigitalSignatureUtil.LoadSignatures(ArtifactsDir + "DigitalSignatureUtil.LoadAndRemove.FromStream.docx"), Is.Empty);
```

Показывает, как удалить цифровые подписи из документа с цифровой подписью.

```csharp
 // Существует два способа использования класса DigitalSignatureUtil для удаления цифровых подписей
 // из подписанного документа, сохранив его неподписанную копию где-то еще в локальной файловой системе.
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

 // Проверяем, что оба наших выходных документа не имеют цифровых подписей.
Assert.That(DigitalSignatureUtil.LoadSignatures(ArtifactsDir + "DigitalSignatureUtil.LoadAndRemove.FromString.docx"), Is.Empty);
Assert.That(DigitalSignatureUtil.LoadSignatures(ArtifactsDir + "DigitalSignatureUtil.LoadAndRemove.FromStream.docx"), Is.Empty);
```

### Смотрите также

* пространство имен [Aspose.Words.DigitalSignatures](../../aspose.words.digitalsignatures)
* сборка [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
