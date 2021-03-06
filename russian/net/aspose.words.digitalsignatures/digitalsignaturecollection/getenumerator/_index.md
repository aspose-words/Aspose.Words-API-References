---
title: GetEnumerator
second_title: Справочник по API Aspose.Words для .NET
description: Возвращает объект перечислителя словаря который можно использовать для перебора всех элементов в коллекции.
type: docs
weight: 50
url: /ru/net/aspose.words.digitalsignatures/digitalsignaturecollection/getenumerator/
---
## DigitalSignatureCollection.GetEnumerator method

Возвращает объект перечислителя словаря, который можно использовать для перебора всех элементов в коллекции.

```csharp
public IEnumerator<DigitalSignature> GetEnumerator()
```

### Примеры

Показывает, как напечатать все цифровые подписи подписанного документа.

```csharp
DigitalSignatureCollection digitalSignatures =
    DigitalSignatureUtil.LoadSignatures(MyDir + "Digitally signed.docx");

using (IEnumerator<DigitalSignature> enumerator = digitalSignatures.GetEnumerator())
{
    while (enumerator.MoveNext())
    {
        DigitalSignature ds = enumerator.Current;

        if (ds != null)
            Console.WriteLine(ds.ToString());
    }
}
```

### Смотрите также

* class [DigitalSignature](../../digitalsignature)
* class [DigitalSignatureCollection](../../digitalsignaturecollection)
* пространство имен [Aspose.Words.DigitalSignatures](../../digitalsignaturecollection)
* сборка [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
