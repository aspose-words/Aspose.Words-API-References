---
title: OdsoRecipientDataCollection.GetEnumerator
linktitle: GetEnumerator
articleTitle: GetEnumerator
second_title: Aspose.Words para .NET
description: Descubra el método GetEnumerator de OdsoRecipientDataCollection itere de manera eficiente a través de los elementos de la colección con facilidad y mejore sus capacidades de manejo de datos.
type: docs
weight: 60
url: /es/net/aspose.words.settings/odsorecipientdatacollection/getenumerator/
---
## OdsoRecipientDataCollection.GetEnumerator method

Devuelve un objeto enumerador que se puede utilizar para iterar sobre todos los elementos de la colección.

```csharp
public IEnumerator<OdsoRecipientData> GetEnumerator()
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

//Podemos clonar los elementos de esta colección.
Assert.AreNotEqual(dataCollection[0], dataCollection[0].Clone());

// También podemos eliminar elementos individualmente o borrar toda la colección de una vez.
dataCollection.RemoveAt(0);

Assert.AreEqual(69, dataCollection.Count);

dataCollection.Clear();

Assert.AreEqual(0, dataCollection.Count);
```

### Ver también

* class [OdsoRecipientData](../../odsorecipientdata/)
* class [OdsoRecipientDataCollection](../)
* espacio de nombres [Aspose.Words.Settings](../../../aspose.words.settings/)
* asamblea [Aspose.Words](../../../)
