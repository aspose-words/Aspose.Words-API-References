---
title: DigitalSignatureUtil.RemoveAllSignatures
second_title: Справочник по API Aspose.Words для .NET
description: DigitalSignatureUtil метод. Удаляет все цифровые подписи из исходного файла и записывает неподписанный файл в файл назначения.
type: docs
weight: 20
url: /ru/net/aspose.words.digitalsignatures/digitalsignatureutil/removeallsignatures/
---
## RemoveAllSignatures(string, string) {#removeallsignatures_1}

Удаляет все цифровые подписи из исходного файла и записывает неподписанный файл в файл назначения.

Для удаления цифровой подписи совместимы следующие форматы: Doc , Dot , Docx , Dotx , Docm , Odt , Ott.

```csharp
public static void RemoveAllSignatures(string srcFileName, string dstFileName)
```

### Примеры

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

* class [DigitalSignatureUtil](../)
* пространство имен [Aspose.Words.DigitalSignatures](../../digitalsignatureutil/)
* сборка [Aspose.Words](../../../)

---

## RemoveAllSignatures(Stream, Stream) {#removeallsignatures}

Удаляет все цифровые подписи из документа в исходном потоке и записывает неподписанный документ в целевой поток.

**Вывод будет записан в начало потока, а размер потока будет обновляться в зависимости от длины контента.**

Для удаления цифровой подписи совместимы следующие форматы: Doc , Dot , Docx , Dotx , Docm , Odt , Ott.

```csharp
public static void RemoveAllSignatures(Stream srcStream, Stream dstStream)
```

### Примеры

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

* class [DigitalSignatureUtil](../)
* пространство имен [Aspose.Words.DigitalSignatures](../../digitalsignatureutil/)
* сборка [Aspose.Words](../../../)


