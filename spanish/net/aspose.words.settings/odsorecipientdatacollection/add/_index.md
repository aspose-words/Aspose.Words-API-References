---
title: OdsoRecipientDataCollection.Add
second_title: Referencia de API de Aspose.Words para .NET
description: OdsoRecipientDataCollection método. Agrega un objeto al final de esta colección.
type: docs
weight: 40
url: /es/net/aspose.words.settings/odsorecipientdatacollection/add/
---
## OdsoRecipientDataCollection.Add method

Agrega un objeto al final de esta colección.

```csharp
public int Add(OdsoRecipientData value)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| value | OdsoRecipientData | El objeto a agregar. No puede ser nulo. |

### Ejemplos

Muestra cómo acceder a la colección de datos que designa qué registros de origen de datos combinados excluirá una combinación de correspondencia.

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

* class [OdsoRecipientData](../../odsorecipientdata/)
* class [OdsoRecipientDataCollection](../)
* espacio de nombres [Aspose.Words.Settings](../../odsorecipientdatacollection/)
* asamblea [Aspose.Words](../../../)


