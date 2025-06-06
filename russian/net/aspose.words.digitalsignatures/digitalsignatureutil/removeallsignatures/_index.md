---
title: DigitalSignatureUtil.RemoveAllSignatures
linktitle: RemoveAllSignatures
articleTitle: RemoveAllSignatures
second_title: Aspose.Words для .NET
description: Легко удалите все цифровые подписи с помощью метода RemoveAllSignatures от DigitalSignatureUtil. Преобразуйте ваши подписанные файлы в чистые, неподписанные версии легко!
type: docs
weight: 20
url: /ru/net/aspose.words.digitalsignatures/digitalsignatureutil/removeallsignatures/
---
## RemoveAllSignatures(*string, string*) {#removeallsignatures_1}

Удаляет все цифровые подписи из исходного файла и записывает неподписанный файл в целевой файл.

Для удаления цифровой подписи совместимы следующие форматы: Doc , Dot , Docx , Dotx , Docm , Dotm , Odt , Ott.

```csharp
public static void RemoveAllSignatures(string srcFileName, string dstFileName)
```

## Примеры

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

* class [DigitalSignatureUtil](../)
* пространство имен [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* сборка [Aspose.Words](../../../)

---

## RemoveAllSignatures(*Stream, Stream*) {#removeallsignatures}

Удаляет все цифровые подписи из документа в исходном потоке и записывает неподписанный документ в целевой поток.

**Вывод будет записан в начало потока, а размер потока будет обновлен в соответствии с длиной содержимого.**

Для удаления цифровой подписи совместимы следующие форматы: Doc , Dot , Docx , Dotx , Docm , Dotm , Odt , Ott.

```csharp
public static void RemoveAllSignatures(Stream srcStream, Stream dstStream)
```

## Примеры

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

* class [DigitalSignatureUtil](../)
* пространство имен [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* сборка [Aspose.Words](../../../)
