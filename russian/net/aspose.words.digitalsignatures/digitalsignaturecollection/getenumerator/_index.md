---
title: DigitalSignatureCollection.GetEnumerator
linktitle: GetEnumerator
articleTitle: GetEnumerator
second_title: Aspose.Words для .NET
description: DigitalSignatureCollection GetEnumerator метод. Возвращает объект перечислителя словаря который можно использовать для перебора всех элементов коллекции на С#.
type: docs
weight: 50
url: /ru/net/aspose.words.digitalsignatures/digitalsignaturecollection/getenumerator/
---
## DigitalSignatureCollection.GetEnumerator method

Возвращает объект перечислителя словаря, который можно использовать для перебора всех элементов коллекции.

```csharp
public IEnumerator<DigitalSignature> GetEnumerator()
```

## Примеры

Показывает, как распечатать все цифровые подписи подписанного документа.

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

* class [DigitalSignature](../../digitalsignature/)
* class [DigitalSignatureCollection](../)
* пространство имен [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* сборка [Aspose.Words](../../../)
