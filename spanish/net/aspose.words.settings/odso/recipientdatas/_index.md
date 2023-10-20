---
title: Odso.RecipientDatas
linktitle: RecipientDatas
articleTitle: RecipientDatas
second_title: Aspose.Words para .NET
description: Odso RecipientDatas propiedad. Obtiene o establece una colección de objetos que especifican la inclusión/exclusión de registros individuales en la combinación de correspondencia. Este objeto nuncanulo  en C#.
type: docs
weight: 70
url: /es/net/aspose.words.settings/odso/recipientdatas/
---
## Odso.RecipientDatas property

Obtiene o establece una colección de objetos que especifican la inclusión/exclusión de registros individuales en la combinación de correspondencia. Este objeto nunca`nulo` .

```csharp
public OdsoRecipientDataCollection RecipientDatas { get; set; }
```

## Ejemplos

Muestra cómo acceder a la colección de datos que designa qué registros de origen de datos de combinación excluirá una combinación de correspondencia.

```csharp
Document doc = new Document(MyDir + "Odso data.docx");

OdsoRecipientDataCollection dataCollection = doc.MailMergeSettings.Odso.RecipientDatas;

Assert.AreEqual(70, dataCollection.Count);

using (IEnumerator<OdsoRecipientData> enumerator = dataCollection.GetEnumerator())
{
    int index = 0;
    while (enumerator.MoveNext())
    {
        Console.WriteLine(
            $"Odso recipient data index {index++} will {(enumerator.Current.Active ? "" : "not ")}be imported upon mail merge.");
        Console.WriteLine($"\tColumn #{enumerator.Current.Column}");
        Console.WriteLine($"\tHash code: {enumerator.Current.Hash}");
        Console.WriteLine($"\tContents array length: {enumerator.Current.UniqueTag.Length}");
    }
}

// Podemos clonar los elementos de esta colección.
Assert.AreNotEqual(dataCollection[0], dataCollection[0].Clone());

// También podemos eliminar elementos individualmente o borrar toda la colección a la vez.
dataCollection.RemoveAt(0);

Assert.AreEqual(69, dataCollection.Count);

dataCollection.Clear();

Assert.AreEqual(0, dataCollection.Count);
```

### Ver también

* class [OdsoRecipientDataCollection](../../odsorecipientdatacollection/)
* class [Odso](../)
* espacio de nombres [Aspose.Words.Settings](../../../aspose.words.settings/)
* asamblea [Aspose.Words](../../../)
