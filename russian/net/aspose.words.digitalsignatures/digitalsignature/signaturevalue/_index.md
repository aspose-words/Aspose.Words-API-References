---
title: DigitalSignature.SignatureValue
second_title: Справочник по API Aspose.Words для .NET
description: DigitalSignature свойство. Получает массив байтов представляющий значение подписи.
type: docs
weight: 60
url: /ru/net/aspose.words.digitalsignatures/digitalsignature/signaturevalue/
---
## DigitalSignature.SignatureValue property

Получает массив байтов, представляющий значение подписи.

```csharp
public byte[] SignatureValue { get; }
```

### Примеры

Показывает, как получить значение цифровой подписи из документа с цифровой подписью.

```csharp
Document doc = new Document(MyDir + "Digitally signed.docx");

foreach (DigitalSignature digitalSignature in doc.DigitalSignatures)
{
    string signatureValue = Convert.ToBase64String(digitalSignature.SignatureValue);
    Assert.AreEqual("K1cVLLg2kbJRAzT5WK+m++G8eEO+l7S+5ENdjMxxTXkFzGUfvwxREuJdSFj9AbD" +
        "MhnGvDURv9KEhC25DDF1al8NRVR71TF3CjHVZXpYu7edQS5/yLw/k5CiFZzCp1+MmhOdYPcVO+Fm" +
        "+9fKr2iNLeyYB+fgEeZHfTqTFM2WwAqo=", signatureValue);
}
```

### Смотрите также

* class [DigitalSignature](../)
* пространство имен [Aspose.Words.DigitalSignatures](../../digitalsignature/)
* сборка [Aspose.Words](../../../)


